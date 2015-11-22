[![Build Status](https://travis-ci.org/neuron-js/neuron-combo-server.svg?branch=master)](https://travis-ci.org/neuron-js/neuron-combo-server)
<!-- optional npm version
[![NPM version](https://badge.fury.io/js/neuron-combo-server.svg)](http://badge.fury.io/js/neuron-combo-server)
-->
<!-- optional npm downloads
[![npm module downloads per month](http://img.shields.io/npm/dm/neuron-combo-server.svg)](https://www.npmjs.org/package/neuron-combo-server)
-->
<!-- optional dependency status
[![Dependency Status](https://david-dm.org/neuron-js/neuron-combo-server.svg)](https://david-dm.org/neuron-js/neuron-combo-server)
-->

# neuron-combo-server

Combo server for neuron.js

## CLI

### Install
```sh
$ npm i -g neuron-combo-server
$ neuron-combo-server -p 8000
```

### Argv

```
-p <port>, --port <port>     server port, default to 8000
-d <dir>, --root <dir>       document root, default to process.cwd()
-l <path>, --location <path> root path, default to 'concat'             
```

```sh
curl http://localhost:8000/combo/jquery/underscore
curl http://localhost:8000/combo/jquery/1.9.2,underscore/*
curl http://localhost:8000/combo/form/1.0.0/style.css,home/0.2.0/index.css
```

```
/<location>/<module_id>,<module_id>
```

## Express middleware

```js
var middleware = require('neuron-combo-server');
var app = express();
app.use(middleware({
  location: location,
  root: root
}));

app.listen(port);
```

## License

MIT
