# xen-api [![Build Status](https://travis-ci.org/js-xen-api.png?branch=master)](https://travis-ci.org/js-xen-api)

> ${pkg.description}

## Install

Installation of the [npm package](https://npmjs.org/package/xen-api):

```
> npm install --save xen-api
```

## Usage

```javascript
var createClient = require('xen-api').createClient

var xapi = createClient({
  url: 'https://xen1.company.net',
  auth: {
    user: 'root',
    password: 'important secret password'
  }
})

// Force connection.
xapi.connect().catch(error => {
  console.error(error)
})

// Watch objects.
xapi.objects.on('add', function (objects) {
  console.log('new objects:', objects)
})
```

## Development

### Installing dependencies

```
> npm install
```

### Compilation

The sources files are watched and automatically recompiled on changes.

```
> npm run dev
```

### Tests

```
> npm run test-dev
```

## Contributions

Contributions are *very* welcomed, either on the documentation or on
the code.

You may:

- report any [issue](https://github.com/julien-f/js-xen-api/issues)
  you've encountered;
- fork and create a pull request.

## License

ISC © [Julien Fontanet](https://github.com/julien-f)
