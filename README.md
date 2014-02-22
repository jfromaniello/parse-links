Parse a [Links header](http://www.w3.org/Protocols/9707-link-header.html) into a javascript object.

__I'll no longer maintain this repository. [li](https://github.com/jfromaniello/li) is a fork from this repository and allows parse and stringify.__

## Install

    npm install parse-links

## Usage

~~~javascript
var parseLinks = require('parse-links');
var someLinksHeader = '</api/users?page=0&per_page=2>; rel="first", ' +
                      '</api/users?page=1&per_page=2>; rel="next", ' +
                      '</api/users?page=3&per_page=2>; rel="last"';

console.log(parseLinks(someLinksHeader));

// This will print:
// { 
//   first: '/api/users?page=0&per_page=2',
//   next: '/api/users?page=1&per_page=2',
//   last: '/api/users?page=3&per_page=2' 
// }
~~~

## License

MIT!
