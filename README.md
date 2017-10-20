# Beer-Web-App

## Table of Contents
- [Project](#project)
- [API](#api)
- [Getting Started](#getting-started)
   - [Installing](#installing)
   - [Running the test](#running-the-test)
- [Folder Structure](#folder-structure)
- [Features](#featureS)

## Project
E-commerce Web Site for Beer Lovers!! You can search beers with an abv(Alcohol by volume) of more than 4% and find beer that pairs with food. It will help users to choose right beers that suit for their personal taste and the menu of the day.

## API
The [Punk API](https://punkapi.com/documentation/v2) takes Brewdog's DIY Dog (A craft beer company from Scotland) and turns it into a searchable, filterable API that's completely free and open source.


## Technologies
** React, JSX, Ajax, Material-UI, CSS **

## Getting Started
#### Installing
`npm install`
#### Running the test
`npm start`

## Folder Structure
```
beerLover/
    static/                        
        Index.html          # Main browser entry point
        favicon.ico
    src/
        components/
            app.js
            elements/    
                beerCard.js
                FavoritButton.js
                shoppingcartButton.js
                strongBeerButton.js
            modals/
            pages/     
                home.js    
                login.js
                signup.js
                favoritePage.js
                shoppingcartPage.js
                notFoundPage.js
        api.js                       # Superagent file
        auth.js
        config.js                    
        index.js                     # Main entry point
        
        style/
            index.css/scss                
     README.md
     node_modules
     package.json
     .gitignore
```
## Features

![Imgur](https://i.imgur.com/jsGV4sb.png)

![Imgur](https://i.imgur.com/KcwF3lX.png)

### LogIn/ SignUp 
`Api POST request`

### List of beers in Home.js
`Api GET request -> data.map -> pass data to <beercard.js>`

### List of beers Sorted by abv > 4% or abv < 4%
```
Api GET request
.then(data => {
    var strongBeers = data.filter(beer => {
        return beer.abv > 4%;
        })
    })
strongBeers.map -> pass data to <beercard.js> -> List of beer (> 4%)
```

### Search beer bar by beer name or food
Search Text input ->
`Api GET request(query) -> data.map -> pass data to <beercard.js>`

### Add to Favorite/Shopping cart Page
```
Api PATCH request 
default value  0: false
               1: true
```

### Shopping Cart 
Check box :
```
default value  0: false
Button Click -> Api PATCH request -> 1: true
Button Click -> Api PATCH request -> 0: false
```

Quantity :
```
default value  1
Button Click -> Api PATCH request -> Get new QYT & Price & Total Price from server 
```





