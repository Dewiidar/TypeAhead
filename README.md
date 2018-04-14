# 06 - Type Ahead - JavaScript30 Challenge

## This project aims to instantly showing the search results with a filtered city and state names showing all matched data.

## Notes:

### Fetching data from file.json & parsing it & converting it to array items :
```javascript
const cities = [];
fetch(jsonLink)
    .then(data => data.json())
    .then(myJson => cities.push(...myJson));
```

### Using .match(regex) method :
```javascript
cities.filter(place => {
        var regex = new RegExp(wordToMatch, 'gi');
        return place.city.match(regex) || place.state.match(regex);
      });
```
### Replacing a particular part of a word with another one 
(or with a span that have different css styles as highlights) 
### and repeating the process using map() method to make a new array contains the inline html to be viewed.

```javascript
const html = matchArray.map(place => {
    const regex = new RegExp(this.value, 'gi');
    const cityName = place.city.replace(regex, 
    `<span class="hl">${this.value}</span>`);
        return `
        <li>
            <span class="name">${cityName}</span>
        </li>
        `
}).join('');
```

## Getting Started

Clone or download the repository to your local drive.

### Prerequisites

What you need to install:

This project was created using Gulp automation tool, you can run the following command to the local repo directory to install all the dev dependencies 

```
npm install
```

### Write gulp in the terminal / command line to run the live server.

## Authors

* **Mohamed Dewidar** - *practising the mentioned methods* - [Linkedin](https://www.linkedin.com/in/mohamed-dewidar-331252153/)

## License

This project is licensed under the MIT License. (open-source)

## Acknowledgments

* Wesbos - *creator of the challenge* - (https://github.com/wesbos/JavaScript30)