# api documentation for  [happypack (v3.0.3)](https://github.com/amireh/happypack#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-happypack.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-happypack) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-happypack.svg)](https://travis-ci.org/npmdoc/node-npmdoc-happypack)
#### webpack speed booster, makes you happy!

[![NPM](https://nodei.co/npm/happypack.png?downloads=true)](https://www.npmjs.com/package/happypack)

[![apidoc](https://npmdoc.github.io/node-npmdoc-happypack/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-happypack_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-happypack/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-happypack/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-happypack/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ahmad Amireh"
    },
    "bugs": {
        "url": "https://github.com/amireh/happypack/issues"
    },
    "dependencies": {
        "async": "1.5.0",
        "json-stringify-safe": "5.0.1",
        "loader-utils": "0.2.16",
        "mkdirp": "0.5.1"
    },
    "description": "webpack speed booster, makes you happy!",
    "devDependencies": {
        "chai": "3.5.0",
        "codecov": "1.0.1",
        "eslint": "2.13.1",
        "fs-extra": "0.30.0",
        "mocha": "3.0.1",
        "multiline-slash": "2.0.0",
        "nyc": "7.1.0",
        "sinon": "1.17.5",
        "webpack": "1.13.1",
        "webpack-dev-server": "1.14.1"
    },
    "directories": {},
    "dist": {
        "shasum": "22f78c87a325cdb798c958cf4ec383fcd4d6fdc7",
        "tarball": "https://registry.npmjs.org/happypack/-/happypack-3.0.3.tgz"
    },
    "gitHead": "17410b95b8e21fcb51ea4de43d091e178ea843f5",
    "homepage": "https://github.com/amireh/happypack#readme",
    "keywords": [
        "webpack",
        "plugin",
        "fast",
        "speed",
        "performance",
        "compilation",
        "transformer",
        "loader",
        "happiness",
        "happy"
    ],
    "license": "MIT",
    "main": "./lib/HappyPlugin.js",
    "maintainers": [
        {
            "name": "amireh",
            "email": "ahmad@amireh.net"
        }
    ],
    "name": "happypack",
    "nyc": {
        "include": [
            "lib/*.js"
        ],
        "exclude": [
            "lib/**/*.test.js",
            "lib/HappyTestUtils.js"
        ]
    },
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/amireh/happypack.git"
    },
    "scripts": {
        "coverage": "nyc report",
        "coverage:ci": "nyc report --reporter=text-lcov > tmp/coverage.lcov && codecov --disable search -f tmp/coverage.lcov",
        "coverage:html": "nyc report --reporter html",
        "lint": "eslint lib",
        "prepublish": "npm run lint && npm run test && npm run test-examples",
        "test": "mocha 'lib/**/*.test.js'",
        "test-examples": "./examples/build-all.sh",
        "test:coverage": "nyc npm test"
    },
    "version": "3.0.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module happypack](#apidoc.module.happypack)
1.  [function <span class="apidocSignatureSpan">happypack.</span>HappyFakeCompiler (params)](#apidoc.element.happypack.HappyFakeCompiler)
1.  [function <span class="apidocSignatureSpan">happypack.</span>HappyRPCHandler ()](#apidoc.element.happypack.HappyRPCHandler)
1.  [function <span class="apidocSignatureSpan">happypack.</span>HappyWorker (params)](#apidoc.element.happypack.HappyWorker)
1.  [function <span class="apidocSignatureSpan">happypack.</span>SharedPtr (value)](#apidoc.element.happypack.SharedPtr)
1.  [function <span class="apidocSignatureSpan">happypack.</span>SharedPtrMap ()](#apidoc.element.happypack.SharedPtrMap)
1.  [function <span class="apidocSignatureSpan">happypack.</span>ThreadPool (config)](#apidoc.element.happypack.ThreadPool)
1.  [function <span class="apidocSignatureSpan">happypack.</span>extractCompilerOptions (options)](#apidoc.element.happypack.extractCompilerOptions)
1.  object <span class="apidocSignatureSpan">happypack.</span>HappyFakeCompiler.prototype
1.  object <span class="apidocSignatureSpan">happypack.</span>HappyRPCHandler.prototype
1.  object <span class="apidocSignatureSpan">happypack.</span>HappyUtils
1.  object <span class="apidocSignatureSpan">happypack.</span>HappyWorker.prototype
1.  object <span class="apidocSignatureSpan">happypack.</span>JSONSerializer
1.  object <span class="apidocSignatureSpan">happypack.</span>SERIALIZABLE_OPTIONS
1.  object <span class="apidocSignatureSpan">happypack.</span>SharedPtr.prototype
1.  object <span class="apidocSignatureSpan">happypack.</span>SharedPtrMap.prototype
1.  object <span class="apidocSignatureSpan">happypack.</span>SourceMapSerializer
1.  object <span class="apidocSignatureSpan">happypack.</span>WebpackUtils

#### [module happypack.HappyFakeCompiler](#apidoc.module.happypack.HappyFakeCompiler)
1.  [function <span class="apidocSignatureSpan">happypack.</span>HappyFakeCompiler (params)](#apidoc.element.happypack.HappyFakeCompiler.HappyFakeCompiler)

#### [module happypack.HappyFakeCompiler.prototype](#apidoc.module.happypack.HappyFakeCompiler.prototype)
1.  [function <span class="apidocSignatureSpan">happypack.HappyFakeCompiler.prototype.</span>_handleResponse (id, message)](#apidoc.element.happypack.HappyFakeCompiler.prototype._handleResponse)
1.  [function <span class="apidocSignatureSpan">happypack.HappyFakeCompiler.prototype.</span>_sendMessage (type, payload, done)](#apidoc.element.happypack.HappyFakeCompiler.prototype._sendMessage)
1.  [function <span class="apidocSignatureSpan">happypack.HappyFakeCompiler.prototype.</span>configure (compilerOptions)](#apidoc.element.happypack.HappyFakeCompiler.prototype.configure)
1.  [function <span class="apidocSignatureSpan">happypack.HappyFakeCompiler.prototype.</span>resolve (context, resource, done)](#apidoc.element.happypack.HappyFakeCompiler.prototype.resolve)

#### [module happypack.HappyRPCHandler](#apidoc.module.happypack.HappyRPCHandler)
1.  [function <span class="apidocSignatureSpan">happypack.</span>HappyRPCHandler ()](#apidoc.element.happypack.HappyRPCHandler.HappyRPCHandler)

#### [module happypack.HappyRPCHandler.prototype](#apidoc.module.happypack.HappyRPCHandler.prototype)
1.  [function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>execute (type, payload, done)](#apidoc.element.happypack.HappyRPCHandler.prototype.execute)
1.  [function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>isActive ()](#apidoc.element.happypack.HappyRPCHandler.prototype.isActive)
1.  [function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>registerActiveCompiler (id, compiler)](#apidoc.element.happypack.HappyRPCHandler.prototype.registerActiveCompiler)
1.  [function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>registerActiveLoader (id, instance)](#apidoc.element.happypack.HappyRPCHandler.prototype.registerActiveLoader)
1.  [function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>unregisterActiveCompiler (id)](#apidoc.element.happypack.HappyRPCHandler.prototype.unregisterActiveCompiler)
1.  [function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>unregisterActiveLoader (id)](#apidoc.element.happypack.HappyRPCHandler.prototype.unregisterActiveLoader)

#### [module happypack.HappyUtils](#apidoc.module.happypack.HappyUtils)
1.  [function <span class="apidocSignatureSpan">happypack.HappyUtils.</span>generateCompiledPath (filePath)](#apidoc.element.happypack.HappyUtils.generateCompiledPath)
1.  [function <span class="apidocSignatureSpan">happypack.HappyUtils.</span>isReadable (filePath)](#apidoc.element.happypack.HappyUtils.isReadable)
1.  [function <span class="apidocSignatureSpan">happypack.HappyUtils.</span>mkdirSync (dirPath)](#apidoc.element.happypack.HappyUtils.mkdirSync)

#### [module happypack.HappyWorker](#apidoc.module.happypack.HappyWorker)
1.  [function <span class="apidocSignatureSpan">happypack.</span>HappyWorker (params)](#apidoc.element.happypack.HappyWorker.HappyWorker)

#### [module happypack.HappyWorker.prototype](#apidoc.module.happypack.HappyWorker.prototype)
1.  [function <span class="apidocSignatureSpan">happypack.HappyWorker.prototype.</span>compile (params, done)](#apidoc.element.happypack.HappyWorker.prototype.compile)

#### [module happypack.JSONSerializer](#apidoc.module.happypack.JSONSerializer)
1.  [function <span class="apidocSignatureSpan">happypack.JSONSerializer.</span>deserialize (string)](#apidoc.element.happypack.JSONSerializer.deserialize)
1.  [function <span class="apidocSignatureSpan">happypack.JSONSerializer.</span>serialize (obj)](#apidoc.element.happypack.JSONSerializer.serialize)

#### [module happypack.SharedPtr](#apidoc.module.happypack.SharedPtr)
1.  [function <span class="apidocSignatureSpan">happypack.</span>SharedPtr (value)](#apidoc.element.happypack.SharedPtr.SharedPtr)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtr.</span>safeGet (ptr)](#apidoc.element.happypack.SharedPtr.safeGet)

#### [module happypack.SharedPtr.prototype](#apidoc.module.happypack.SharedPtr.prototype)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtr.prototype.</span>acquire ()](#apidoc.element.happypack.SharedPtr.prototype.acquire)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtr.prototype.</span>get ()](#apidoc.element.happypack.SharedPtr.prototype.get)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtr.prototype.</span>isDead ()](#apidoc.element.happypack.SharedPtr.prototype.isDead)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtr.prototype.</span>release ()](#apidoc.element.happypack.SharedPtr.prototype.release)

#### [module happypack.SharedPtrMap](#apidoc.module.happypack.SharedPtrMap)
1.  [function <span class="apidocSignatureSpan">happypack.</span>SharedPtrMap ()](#apidoc.element.happypack.SharedPtrMap.SharedPtrMap)

#### [module happypack.SharedPtrMap.prototype](#apidoc.module.happypack.SharedPtrMap.prototype)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtrMap.prototype.</span>delete (key)](#apidoc.element.happypack.SharedPtrMap.prototype.delete)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtrMap.prototype.</span>get (key)](#apidoc.element.happypack.SharedPtrMap.prototype.get)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtrMap.prototype.</span>getSize ()](#apidoc.element.happypack.SharedPtrMap.prototype.getSize)
1.  [function <span class="apidocSignatureSpan">happypack.SharedPtrMap.prototype.</span>set (key, value)](#apidoc.element.happypack.SharedPtrMap.prototype.set)

#### [module happypack.SourceMapSerializer](#apidoc.module.happypack.SourceMapSerializer)
1.  [function <span class="apidocSignatureSpan">happypack.SourceMapSerializer.</span>deserialize (x)](#apidoc.element.happypack.SourceMapSerializer.deserialize)
1.  [function <span class="apidocSignatureSpan">happypack.SourceMapSerializer.</span>serialize (x)](#apidoc.element.happypack.SourceMapSerializer.serialize)

#### [module happypack.WebpackUtils](#apidoc.module.happypack.WebpackUtils)
1.  [function <span class="apidocSignatureSpan">happypack.WebpackUtils.</span>applyLoaders (runContext, sourceCode, sourceMap, done)](#apidoc.element.happypack.WebpackUtils.applyLoaders)
1.  [function <span class="apidocSignatureSpan">happypack.WebpackUtils.</span>extractLoaders (entry)](#apidoc.element.happypack.WebpackUtils.extractLoaders)
1.  [function <span class="apidocSignatureSpan">happypack.WebpackUtils.</span>normalizeLoader (input)](#apidoc.element.happypack.WebpackUtils.normalizeLoader)
1.  [function <span class="apidocSignatureSpan">happypack.WebpackUtils.</span>resolveLoaders (compiler, loaders, done)](#apidoc.element.happypack.WebpackUtils.resolveLoaders)



# <a name="apidoc.module.happypack"></a>[module happypack](#apidoc.module.happypack)

#### <a name="apidoc.element.happypack.HappyFakeCompiler"></a>[function <span class="apidocSignatureSpan">happypack.</span>HappyFakeCompiler (params)](#apidoc.element.happypack.HappyFakeCompiler)
- description and source-code
```javascript
function HappyFakeCompiler(params) {
  assert(typeof params.id === 'string',
    "id must be assigned to a HappyFakeCompiler.");

  assert(typeof params.compilerId === 'string',
    "compilerId must be assigned to a HappyFakeCompiler.");

  assert(typeof params.send === 'function',
    "send implementation must be assigned to a HappyFakeCompiler.");

  this._id = 'FakeCompiler::' + params.id.toString() + '-' + params.compilerId.toString();
  this._compilerId = params.compilerId;
  this._sendMessageImpl = params.send;
  this._requests = {};
  this._messageId = 0;
  this.options = {};
  this.context = null;
  this.inputFileSystem = fs;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.HappyRPCHandler"></a>[function <span class="apidocSignatureSpan">happypack.</span>HappyRPCHandler ()](#apidoc.element.happypack.HappyRPCHandler)
- description and source-code
```javascript
function HappyRPCHandler() {
  this.activeLoaders = new SharedPtrMap();
  this.activeCompilers = new SharedPtrMap();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.HappyWorker"></a>[function <span class="apidocSignatureSpan">happypack.</span>HappyWorker (params)](#apidoc.element.happypack.HappyWorker)
- description and source-code
```javascript
function HappyWorker(params) {
  this._compiler = params.compiler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.SharedPtr"></a>[function <span class="apidocSignatureSpan">happypack.</span>SharedPtr (value)](#apidoc.element.happypack.SharedPtr)
- description and source-code
```javascript
function SharedPtr(value) {
  this._refs = 1;
  this._value = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.SharedPtrMap"></a>[function <span class="apidocSignatureSpan">happypack.</span>SharedPtrMap ()](#apidoc.element.happypack.SharedPtrMap)
- description and source-code
```javascript
function SharedPtrMap() {
  this.map = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.ThreadPool"></a>[function <span class="apidocSignatureSpan">happypack.</span>ThreadPool (config)](#apidoc.element.happypack.ThreadPool)
- description and source-code
```javascript
function HappyThreadPool(config) {
  var rpcHandler = new HappyRPCHandler();

  assert(!isNaN(config.size),
    "ArgumentError: HappyThreadPool requires a valid integer for its size, but got NaN."
  );

  assert(config.size > 0,
    "ArgumentError: HappyThreadPool requires a positive integer for its size " +
    ", but got {" + config.size + "}."
  );

  var threads = createThreads(config.size, rpcHandler, {
    id: config.id,
    verbose: config.verbose,
    debug: config.debug,
  });

  var getThread = RoundRobinThreadPool(threads);

  return {
    size: config.size,

    start: function(compilerId, compiler, compilerOptions, done) {
      rpcHandler.registerActiveCompiler(compilerId, compiler);

      async.parallel(threads.filter(not(send('isOpen'))).map(get('open')), function(err) {
        if (err) {
          return done(err);
        }

        async.parallel(threads.map(function(thread) {
          return function(callback) {
            thread.configure(compilerId, compilerOptions, callback);
          }
        }), done);
      });
    },

    isRunning: function() {
      return !threads.some(not(send('isOpen')));
    },

    compile: function(loaderId, loader, params, done) {
      var worker = getThread();

      rpcHandler.registerActiveLoader(loaderId, loader);

      worker.compile(params, function() {
        rpcHandler.unregisterActiveLoader(loaderId);

        done.apply(null, arguments);
      });
    },

    stop: function(compilerId) {
      rpcHandler.unregisterActiveCompiler(compilerId);

      if (!rpcHandler.isActive()) {
        threads.filter(send('isOpen')).map(send('close'));
      }
    },
  };
}
```
- example usage
```shell
...

Here's an example of using a custom pool of 5 threads that will be shared
between loaders for both JS and SCSS/LESS/whatever sources:

'''javascript
// @file: webpack.config.js
var HappyPack = require('happypack');
var happyThreadPool = HappyPack.ThreadPool({ size: 5 });

module.exports = {
// ...
plugins: [
  new HappyPack({
    id: 'js',
    threadPool: happyThreadPool
...
```

#### <a name="apidoc.element.happypack.extractCompilerOptions"></a>[function <span class="apidocSignatureSpan">happypack.</span>extractCompilerOptions (options)](#apidoc.element.happypack.extractCompilerOptions)
- description and source-code
```javascript
extractCompilerOptions = function (options) {
  var ALLOWED_KEYS = HappyPlugin.SERIALIZABLE_OPTIONS;

  return Object.keys(options).reduce(function(hsh, key) {
    if (ALLOWED_KEYS.indexOf(key) > -1) {
      hsh[key] = options[key];
    }

    return hsh;
  }, {});
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.happypack.HappyFakeCompiler"></a>[module happypack.HappyFakeCompiler](#apidoc.module.happypack.HappyFakeCompiler)

#### <a name="apidoc.element.happypack.HappyFakeCompiler.HappyFakeCompiler"></a>[function <span class="apidocSignatureSpan">happypack.</span>HappyFakeCompiler (params)](#apidoc.element.happypack.HappyFakeCompiler.HappyFakeCompiler)
- description and source-code
```javascript
function HappyFakeCompiler(params) {
  assert(typeof params.id === 'string',
    "id must be assigned to a HappyFakeCompiler.");

  assert(typeof params.compilerId === 'string',
    "compilerId must be assigned to a HappyFakeCompiler.");

  assert(typeof params.send === 'function',
    "send implementation must be assigned to a HappyFakeCompiler.");

  this._id = 'FakeCompiler::' + params.id.toString() + '-' + params.compilerId.toString();
  this._compilerId = params.compilerId;
  this._sendMessageImpl = params.send;
  this._requests = {};
  this._messageId = 0;
  this.options = {};
  this.context = null;
  this.inputFileSystem = fs;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.happypack.HappyFakeCompiler.prototype"></a>[module happypack.HappyFakeCompiler.prototype](#apidoc.module.happypack.HappyFakeCompiler.prototype)

#### <a name="apidoc.element.happypack.HappyFakeCompiler.prototype._handleResponse"></a>[function <span class="apidocSignatureSpan">happypack.HappyFakeCompiler.prototype.</span>_handleResponse (id, message)](#apidoc.element.happypack.HappyFakeCompiler.prototype._handleResponse)
- description and source-code
```javascript
_handleResponse = function (id, message) {
  var callback;

  if (!this._requests[id]) return; // not for us

  assert(message.payload.hasOwnProperty('error'),
    "Compiler message payload must contain an @error field!");

  assert(message.payload.hasOwnProperty('result'),
    "Compiler message payload must contain a @result field!");

  callback = this._requests[id];
  delete this._requests[id];

  callback(message.payload.error, message.payload.result);
}
```
- example usage
```shell
...
    start: function(compilerId, compiler, compilerOptions, done) {
var fakeCompiler = new HappyFakeCompiler({
  id: 'foreground',
  compilerId: compilerId,
  send: function executeCompilerRPC(message) {
    // TODO: DRY alert, see HappyThread.js
    rpcHandler.execute(message.data.type, message.data.payload, function serveRPCResult(error, result) {
      fakeCompiler._handleResponse(message.id, {
        payload: {
          error: error || null,
          result: result || null
        }
      });
    });
  }
...
```

#### <a name="apidoc.element.happypack.HappyFakeCompiler.prototype._sendMessage"></a>[function <span class="apidocSignatureSpan">happypack.HappyFakeCompiler.prototype.</span>_sendMessage (type, payload, done)](#apidoc.element.happypack.HappyFakeCompiler.prototype._sendMessage)
- description and source-code
```javascript
_sendMessage = function (type, payload, done) {
  var messageId = this._id + ':' + (++this._messageId).toString();

  this._requests[messageId] = done;
  this._sendMessageImpl({
    id: messageId,
    name: 'COMPILER_REQUEST',
    data: {
      type: type,
      compilerId: this._compilerId,
      payload: payload,
    }
  });
}
```
- example usage
```shell
...
 * @param {String} [done.error=null]
 *        A resolving error, if any.
 *
 * @param {String} done.filePath
 *        The resolved file path.
 */
HFCPt.resolve = function(context, resource, done) {
  this._sendMessage('resolve', {
    context: context,
    resource: resource
  }, done);
};

// @private
HFCPt._handleResponse = function(id, message) {
...
```

#### <a name="apidoc.element.happypack.HappyFakeCompiler.prototype.configure"></a>[function <span class="apidocSignatureSpan">happypack.HappyFakeCompiler.prototype.</span>configure (compilerOptions)](#apidoc.element.happypack.HappyFakeCompiler.prototype.configure)
- description and source-code
```javascript
configure = function (compilerOptions) {
  assert(compilerOptions && typeof compilerOptions === 'object');

  this.options = compilerOptions;
  this.context = compilerOptions.context;
}
```
- example usage
```shell
...
          result: result || null
        }
      });
    });
  }
});

fakeCompiler.configure(compiler.options);

rpcHandler = new HappyRPCHandler();
rpcHandler.registerActiveCompiler(compilerId, compiler);

worker = new HappyWorker({
  compiler: fakeCompiler,
  loaders: config.loaders
...
```

#### <a name="apidoc.element.happypack.HappyFakeCompiler.prototype.resolve"></a>[function <span class="apidocSignatureSpan">happypack.HappyFakeCompiler.prototype.</span>resolve (context, resource, done)](#apidoc.element.happypack.HappyFakeCompiler.prototype.resolve)
- description and source-code
```javascript
resolve = function (context, resource, done) {
  this._sendMessage('resolve', {
    context: context,
    resource: resource
  }, done);
}
```
- example usage
```shell
...

var resolveSyncNotSupported = NotSupported('this.resolveSync()');
var execNotSupported = NotSupported('this.exec()');

function HappyFakeLoaderContext(initialValues) {
var loader = {};

// for compiler RPCs, like this.resolve()
loader._compiler = null;

// for loader RPCs, like this.emitWarning()
loader._remoteLoaderId = null;

loader.version = 1; // https://webpack.github.io/docs/loaders.html#version
loader.webpack = false;
...
```



# <a name="apidoc.module.happypack.HappyRPCHandler"></a>[module happypack.HappyRPCHandler](#apidoc.module.happypack.HappyRPCHandler)

#### <a name="apidoc.element.happypack.HappyRPCHandler.HappyRPCHandler"></a>[function <span class="apidocSignatureSpan">happypack.</span>HappyRPCHandler ()](#apidoc.element.happypack.HappyRPCHandler.HappyRPCHandler)
- description and source-code
```javascript
function HappyRPCHandler() {
  this.activeLoaders = new SharedPtrMap();
  this.activeCompilers = new SharedPtrMap();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.happypack.HappyRPCHandler.prototype"></a>[module happypack.HappyRPCHandler.prototype](#apidoc.module.happypack.HappyRPCHandler.prototype)

#### <a name="apidoc.element.happypack.HappyRPCHandler.prototype.execute"></a>[function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>execute (type, payload, done)](#apidoc.element.happypack.HappyRPCHandler.prototype.execute)
- description and source-code
```javascript
execute = function (type, payload, done) {
  var compiler, loader;

  if (COMPILER_RPCs.hasOwnProperty(type)) {
    if (payload.compilerId) {
      compiler = this.activeCompilers.get(payload.compilerId);
    }
    else {
      compiler = this.activeCompilers.get('default');
    }

    assert(!!compiler,
      "A compiler RPC was dispatched, but no compiler instance was registered!"
    );

    COMPILER_RPCs[type](compiler, payload, done);
  }
  else if (LOADER_RPCS.hasOwnProperty(type)) {
    loader = this.activeLoaders.get(payload.remoteLoaderId);

    assert(!!loader,
      "A loader RPC was dispatched to HappyLoader[" + payload.remoteLoaderId +
      "] but no such loader is active!"
    );

    LOADER_RPCS[type](loader, payload, done);
  }
  else {
    assert(false, "Unrecognized loader RPC '" + type + '"');
  }
}
```
- example usage
```shell
...

    start: function(compilerId, compiler, compilerOptions, done) {
var fakeCompiler = new HappyFakeCompiler({
  id: 'foreground',
  compilerId: compilerId,
  send: function executeCompilerRPC(message) {
    // TODO: DRY alert, see HappyThread.js
    rpcHandler.execute(message.data.type, message.data.payload, function serveRPCResult(error, result) {
      fakeCompiler._handleResponse(message.id, {
        payload: {
          error: error || null,
          result: result || null
        }
      });
    });
...
```

#### <a name="apidoc.element.happypack.HappyRPCHandler.prototype.isActive"></a>[function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>isActive ()](#apidoc.element.happypack.HappyRPCHandler.prototype.isActive)
- description and source-code
```javascript
isActive = function () {
  return this.activeCompilers.getSize() > 0;
}
```
- example usage
```shell
...
        done.apply(null, arguments);
      });
    },

    stop: function(compilerId) {
      rpcHandler.unregisterActiveCompiler(compilerId);

      if (!rpcHandler.isActive()) {
        threads.filter(send('isOpen')).map(send('close'));
      }
    },
  };
}

function createThreads(count, rpcHandler, config) {
...
```

#### <a name="apidoc.element.happypack.HappyRPCHandler.prototype.registerActiveCompiler"></a>[function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>registerActiveCompiler (id, compiler)](#apidoc.element.happypack.HappyRPCHandler.prototype.registerActiveCompiler)
- description and source-code
```javascript
registerActiveCompiler = function (id, compiler) {
  this.activeCompilers.set(id || 'default', compiler);
}
```
- example usage
```shell
...
    });
  }
});

fakeCompiler.configure(compiler.options);

rpcHandler = new HappyRPCHandler();
rpcHandler.registerActiveCompiler(compilerId, compiler);

worker = new HappyWorker({
  compiler: fakeCompiler,
  loaders: config.loaders
});

done();
...
```

#### <a name="apidoc.element.happypack.HappyRPCHandler.prototype.registerActiveLoader"></a>[function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>registerActiveLoader (id, instance)](#apidoc.element.happypack.HappyRPCHandler.prototype.registerActiveLoader)
- description and source-code
```javascript
registerActiveLoader = function (id, instance) {
  this.activeLoaders.set(id || '1', instance);
}
```
- example usage
```shell
...

stop: function(/*compilerId*/) {
  worker = null;
  rpcHandler = null;
},

compile: function(loaderId, loader, params, done) {
  rpcHandler.registerActiveLoader(loaderId, loader);

  worker.compile(params, function() {
    rpcHandler.unregisterActiveLoader(loaderId);

    done.apply(null, arguments);
  });
},
...
```

#### <a name="apidoc.element.happypack.HappyRPCHandler.prototype.unregisterActiveCompiler"></a>[function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>unregisterActiveCompiler (id)](#apidoc.element.happypack.HappyRPCHandler.prototype.unregisterActiveCompiler)
- description and source-code
```javascript
unregisterActiveCompiler = function (id) {
  this.activeCompilers.delete(id || 'default');
}
```
- example usage
```shell
...
        rpcHandler.unregisterActiveLoader(loaderId);

        done.apply(null, arguments);
      });
    },

    stop: function(compilerId) {
      rpcHandler.unregisterActiveCompiler(compilerId);

      if (!rpcHandler.isActive()) {
        threads.filter(send('isOpen')).map(send('close'));
      }
    },
  };
}
...
```

#### <a name="apidoc.element.happypack.HappyRPCHandler.prototype.unregisterActiveLoader"></a>[function <span class="apidocSignatureSpan">happypack.HappyRPCHandler.prototype.</span>unregisterActiveLoader (id)](#apidoc.element.happypack.HappyRPCHandler.prototype.unregisterActiveLoader)
- description and source-code
```javascript
unregisterActiveLoader = function (id) {
  this.activeLoaders.delete(id || '1');
}
```
- example usage
```shell
...
      rpcHandler = null;
    },

    compile: function(loaderId, loader, params, done) {
      rpcHandler.registerActiveLoader(loaderId, loader);

      worker.compile(params, function() {
        rpcHandler.unregisterActiveLoader(loaderId);

        done.apply(null, arguments);
      });
    },
  };
}
...
```



# <a name="apidoc.module.happypack.HappyUtils"></a>[module happypack.HappyUtils](#apidoc.module.happypack.HappyUtils)

#### <a name="apidoc.element.happypack.HappyUtils.generateCompiledPath"></a>[function <span class="apidocSignatureSpan">happypack.HappyUtils.</span>generateCompiledPath (filePath)](#apidoc.element.happypack.HappyUtils.generateCompiledPath)
- description and source-code
```javascript
generateCompiledPath = function (filePath) {
  return 's-' + hashString(filePath + Math.random().toString(36).substr(2));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.HappyUtils.isReadable"></a>[function <span class="apidocSignatureSpan">happypack.HappyUtils.</span>isReadable (filePath)](#apidoc.element.happypack.HappyUtils.isReadable)
- description and source-code
```javascript
isReadable = function (filePath) {
  try {
    var ret = accessFile(filePath, fs.R_OK);
    if (ret !== undefined) {
      return ret;
    }
    return true;
  }
  catch(e) {
    return false;
  }
}
```
- example usage
```shell
...
var oldCache, staleEntryCount;

cache.context = currentContext;

assert(typeof currentContext === 'object' && !!currentContext,
  "HappyFSCache requires a @context parameter to work.");

if (!Utils.isReadable(cachePath)) {
  if (config.verbose) {
    console.log('Happy[%s]: No cache was found, starting fresh.', id);
  }

  return false;
}
...
```

#### <a name="apidoc.element.happypack.HappyUtils.mkdirSync"></a>[function <span class="apidocSignatureSpan">happypack.HappyUtils.</span>mkdirSync (dirPath)](#apidoc.element.happypack.HappyUtils.mkdirSync)
- description and source-code
```javascript
mkdirSync = function (dirPath) {
  try {
    mkdirp.sync(dirPath);
  }
  catch (e) {
    if (!e.message.match('EEXIST')) {
      throw e;
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.happypack.HappyWorker"></a>[module happypack.HappyWorker](#apidoc.module.happypack.HappyWorker)

#### <a name="apidoc.element.happypack.HappyWorker.HappyWorker"></a>[function <span class="apidocSignatureSpan">happypack.</span>HappyWorker (params)](#apidoc.element.happypack.HappyWorker.HappyWorker)
- description and source-code
```javascript
function HappyWorker(params) {
  this._compiler = params.compiler;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.happypack.HappyWorker.prototype"></a>[module happypack.HappyWorker.prototype](#apidoc.module.happypack.HappyWorker.prototype)

#### <a name="apidoc.element.happypack.HappyWorker.prototype.compile"></a>[function <span class="apidocSignatureSpan">happypack.HappyWorker.prototype.</span>compile (params, done)](#apidoc.element.happypack.HappyWorker.prototype.compile)
- description and source-code
```javascript
compile = function (params, done) {
  assert(typeof params.loaderContext.resourcePath === 'string',
    "ArgumentError: expected params.sourcePath to contain path to the source file."
  );

  assert(typeof params.compiledPath === 'string',
    "ArgumentError: expected params.compiledPath to contain path to the compiled file."
  );

  assert(Array.isArray(params.loaders),
    "ArgumentError: expected params.loaders to contain a list of loaders."
  );

  applyLoaders({
    compiler: this._compiler,
    loaders: params.loaders,
    loaderContext: params.loaderContext,
  }, params.loaderContext.sourceCode, params.loaderContext.sourceMap, function(err, source, sourceMap) {
    var compiledPath = params.compiledPath;
    var success = false;

    if (err) {
      console.error(err);
      fs.writeFileSync(compiledPath, serializeError(err), 'utf-8');
    }
    else {
      fs.writeFileSync(compiledPath, source);
      fs.writeFileSync(compiledPath + '.map', SourceMapSerializer.serialize(sourceMap));

      success = true;
    }

    done({
      sourcePath: params.loaderContext.resourcePath,
      compiledPath: compiledPath,
      success: success
    });
  });
}
```
- example usage
```shell
...
      worker = null;
      rpcHandler = null;
    },

    compile: function(loaderId, loader, params, done) {
      rpcHandler.registerActiveLoader(loaderId, loader);

      worker.compile(params, function() {
        rpcHandler.unregisterActiveLoader(loaderId);

        done.apply(null, arguments);
      });
    },
  };
}
...
```



# <a name="apidoc.module.happypack.JSONSerializer"></a>[module happypack.JSONSerializer](#apidoc.module.happypack.JSONSerializer)

#### <a name="apidoc.element.happypack.JSONSerializer.deserialize"></a>[function <span class="apidocSignatureSpan">happypack.JSONSerializer.</span>deserialize (string)](#apidoc.element.happypack.JSONSerializer.deserialize)
- description and source-code
```javascript
deserialize = function (string) {
  return JSON.parse(string, function(key, value) {
    if (Array.isArray(value) && value.length === 3 && value[0] === '@__REGEXP') {
      return new RegExp(value[1], value[2]);
    }

    return value;
  });
}
```
- example usage
```shell
...
  loader.emitError(payload.message);
},

emitFile: function(loader, payload) {
  loader.emitFile(
    payload.name,
    payload.contents,
    SourceMapSerializer.deserialize(payload.sourceMap)
  );
},

addDependency: function(loader, payload) {
  loader.addDependency(payload.file);
},
...
```

#### <a name="apidoc.element.happypack.JSONSerializer.serialize"></a>[function <span class="apidocSignatureSpan">happypack.JSONSerializer.</span>serialize (obj)](#apidoc.element.happypack.JSONSerializer.serialize)
- description and source-code
```javascript
serialize = function (obj) {
  var regexps   = [];
  var str;

  // Creates a JSON string representation of the object and uses placeholders
  // for functions and regexps (identified by index) which are later
  // replaced.
  str = stringify(obj, function (key, value) {
    if (typeof value === 'object' && isRegExp(value)) {
      return '@__REGEXP{' + (regexps.push(value) - 1) + '}@';
    }

    return value;
  });

  // Protects against 'JSON.stringify()' returning 'undefined', by serializing
  // to the literal string: "undefined".
  if (typeof str !== 'string') {
    return String(str);
  }

  // Replace unsafe HTML and invalid JavaScript line terminator chars with
  // their safe Unicode char counterpart. This _must_ happen before the
  // regexps and functions are serialized and added back to the string.
  str = str.replace(UNSAFE_CHARS_REGEXP, function (unsafeChar) {
    return UNICODE_CHARS[unsafeChar];
  });

  if (regexps.length === 0) {
    return str;
  }

  // Replaces all occurrences of function and regexp placeholders in the JSON
  // string with their string representations. If the original value can not
  // be found, then 'undefined' is used.
  return str.replace(PLACE_HOLDER_REGEXP, function (match, type, valueIndex) {
    if (type === 'REGEXP') {
      return JSON.stringify(serializeRegExp(regexps[valueIndex]));
    }

    return match;
  }, 0, function() {});
}
```
- example usage
```shell
...

if (err) {
  console.error(err);
  fs.writeFileSync(compiledPath, serializeError(err), 'utf-8');
}
else {
  fs.writeFileSync(compiledPath, source);
  fs.writeFileSync(compiledPath + '.map', SourceMapSerializer.serialize(sourceMap));

  success = true;
}

done({
  sourcePath: params.loaderContext.resourcePath,
  compiledPath: compiledPath,
...
```



# <a name="apidoc.module.happypack.SharedPtr"></a>[module happypack.SharedPtr](#apidoc.module.happypack.SharedPtr)

#### <a name="apidoc.element.happypack.SharedPtr.SharedPtr"></a>[function <span class="apidocSignatureSpan">happypack.</span>SharedPtr (value)](#apidoc.element.happypack.SharedPtr.SharedPtr)
- description and source-code
```javascript
function SharedPtr(value) {
  this._refs = 1;
  this._value = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.SharedPtr.safeGet"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtr.</span>safeGet (ptr)](#apidoc.element.happypack.SharedPtr.safeGet)
- description and source-code
```javascript
safeGet = function (ptr) {
  return ptr && ptr.get() || null;
}
```
- example usage
```shell
...
  }
  else {
    this.map[key].acquire();
  }
};

SharedPtrMap.prototype.get = function(key) {
  return SharedPtr.safeGet(this.map[key]);
};

SharedPtrMap.prototype.getSize = function() {
  return Object.keys(this.map).length;
};

SharedPtrMap.prototype.delete = function(key) {
...
```



# <a name="apidoc.module.happypack.SharedPtr.prototype"></a>[module happypack.SharedPtr.prototype](#apidoc.module.happypack.SharedPtr.prototype)

#### <a name="apidoc.element.happypack.SharedPtr.prototype.acquire"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtr.prototype.</span>acquire ()](#apidoc.element.happypack.SharedPtr.prototype.acquire)
- description and source-code
```javascript
acquire = function () {
  assert(this.hasOwnProperty('_value'), "Invalid attempt to acquire a dangling pointer!");

  this._refs += 1;
}
```
- example usage
```shell
...
}

SharedPtrMap.prototype.set = function(key, value) {
  if (!this.map.hasOwnProperty(key)) {
    this.map[key] = new SharedPtr(value);
  }
  else {
    this.map[key].acquire();
  }
};

SharedPtrMap.prototype.get = function(key) {
  return SharedPtr.safeGet(this.map[key]);
};
...
```

#### <a name="apidoc.element.happypack.SharedPtr.prototype.get"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtr.prototype.</span>get ()](#apidoc.element.happypack.SharedPtr.prototype.get)
- description and source-code
```javascript
get = function () {
  return this._value;
}
```
- example usage
```shell
...
};

HappyRPCHandler.prototype.execute = function(type, payload, done) {
  var compiler, loader;

  if (COMPILER_RPCs.hasOwnProperty(type)) {
if (payload.compilerId) {
  compiler = this.activeCompilers.get(payload.compilerId);
}
else {
  compiler = this.activeCompilers.get('default');
}

assert(!!compiler,
  "A compiler RPC was dispatched, but no compiler instance was registered!"
...
```

#### <a name="apidoc.element.happypack.SharedPtr.prototype.isDead"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtr.prototype.</span>isDead ()](#apidoc.element.happypack.SharedPtr.prototype.isDead)
- description and source-code
```javascript
isDead = function () {
  return this._refs === 0;
}
```
- example usage
```shell
...
  return Object.keys(this.map).length;
};

SharedPtrMap.prototype.delete = function(key) {
  if (this.map[key]) {
    this.map[key].release();

    if (this.map[key].isDead()) {
      delete this.map[key];
    }
  }
};

module.exports = SharedPtrMap;
...
```

#### <a name="apidoc.element.happypack.SharedPtr.prototype.release"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtr.prototype.</span>release ()](#apidoc.element.happypack.SharedPtr.prototype.release)
- description and source-code
```javascript
release = function () {
  this._refs -= 1;

  assert(this._refs >= 0,
    "Potential race condition or memory leak; shared pointer reference count " +
    "has gone below zero! (" + this._refs + ")"
  );

  if (this._refs === 0) {
    delete this._value;
  }
}
```
- example usage
```shell
...

SharedPtrMap.prototype.getSize = function() {
  return Object.keys(this.map).length;
};

SharedPtrMap.prototype.delete = function(key) {
  if (this.map[key]) {
    this.map[key].release();

    if (this.map[key].isDead()) {
      delete this.map[key];
    }
  }
};
...
```



# <a name="apidoc.module.happypack.SharedPtrMap"></a>[module happypack.SharedPtrMap](#apidoc.module.happypack.SharedPtrMap)

#### <a name="apidoc.element.happypack.SharedPtrMap.SharedPtrMap"></a>[function <span class="apidocSignatureSpan">happypack.</span>SharedPtrMap ()](#apidoc.element.happypack.SharedPtrMap.SharedPtrMap)
- description and source-code
```javascript
function SharedPtrMap() {
  this.map = {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.happypack.SharedPtrMap.prototype"></a>[module happypack.SharedPtrMap.prototype](#apidoc.module.happypack.SharedPtrMap.prototype)

#### <a name="apidoc.element.happypack.SharedPtrMap.prototype.delete"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtrMap.prototype.</span>delete (key)](#apidoc.element.happypack.SharedPtrMap.prototype.delete)
- description and source-code
```javascript
delete = function (key) {
  if (this.map[key]) {
    this.map[key].release();

    if (this.map[key].isDead()) {
      delete this.map[key];
    }
  }
}
```
- example usage
```shell
...
};

HappyRPCHandler.prototype.isActive = function() {
  return this.activeCompilers.getSize() > 0;
};

HappyRPCHandler.prototype.unregisterActiveCompiler = function(id) {
  this.activeCompilers.delete(id || 'default');
};

HappyRPCHandler.prototype.registerActiveLoader = function(id, instance) {
  this.activeLoaders.set(id || '1', instance);
};

HappyRPCHandler.prototype.unregisterActiveLoader = function(id) {
...
```

#### <a name="apidoc.element.happypack.SharedPtrMap.prototype.get"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtrMap.prototype.</span>get (key)](#apidoc.element.happypack.SharedPtrMap.prototype.get)
- description and source-code
```javascript
get = function (key) {
  return SharedPtr.safeGet(this.map[key]);
}
```
- example usage
```shell
...
};

HappyRPCHandler.prototype.execute = function(type, payload, done) {
  var compiler, loader;

  if (COMPILER_RPCs.hasOwnProperty(type)) {
if (payload.compilerId) {
  compiler = this.activeCompilers.get(payload.compilerId);
}
else {
  compiler = this.activeCompilers.get('default');
}

assert(!!compiler,
  "A compiler RPC was dispatched, but no compiler instance was registered!"
...
```

#### <a name="apidoc.element.happypack.SharedPtrMap.prototype.getSize"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtrMap.prototype.</span>getSize ()](#apidoc.element.happypack.SharedPtrMap.prototype.getSize)
- description and source-code
```javascript
getSize = function () {
  return Object.keys(this.map).length;
}
```
- example usage
```shell
...
}

HappyRPCHandler.prototype.registerActiveCompiler = function(id, compiler) {
  this.activeCompilers.set(id || 'default', compiler);
};

HappyRPCHandler.prototype.isActive = function() {
  return this.activeCompilers.getSize() > 0;
};

HappyRPCHandler.prototype.unregisterActiveCompiler = function(id) {
  this.activeCompilers.delete(id || 'default');
};

HappyRPCHandler.prototype.registerActiveLoader = function(id, instance) {
...
```

#### <a name="apidoc.element.happypack.SharedPtrMap.prototype.set"></a>[function <span class="apidocSignatureSpan">happypack.SharedPtrMap.prototype.</span>set (key, value)](#apidoc.element.happypack.SharedPtrMap.prototype.set)
- description and source-code
```javascript
set = function (key, value) {
  if (!this.map.hasOwnProperty(key)) {
    this.map[key] = new SharedPtr(value);
  }
  else {
    this.map[key].acquire();
  }
}
```
- example usage
```shell
...

function HappyRPCHandler() {
  this.activeLoaders = new SharedPtrMap();
  this.activeCompilers = new SharedPtrMap();
}

HappyRPCHandler.prototype.registerActiveCompiler = function(id, compiler) {
  this.activeCompilers.set(id || 'default', compiler);
};

HappyRPCHandler.prototype.isActive = function() {
  return this.activeCompilers.getSize() > 0;
};

HappyRPCHandler.prototype.unregisterActiveCompiler = function(id) {
...
```



# <a name="apidoc.module.happypack.SourceMapSerializer"></a>[module happypack.SourceMapSerializer](#apidoc.module.happypack.SourceMapSerializer)

#### <a name="apidoc.element.happypack.SourceMapSerializer.deserialize"></a>[function <span class="apidocSignatureSpan">happypack.SourceMapSerializer.</span>deserialize (x)](#apidoc.element.happypack.SourceMapSerializer.deserialize)
- description and source-code
```javascript
deserialize = function (x) {
  if (typeof x === 'string') {
    try {
      return JSON.parse(x);
    } catch (e) {
      return null;
    }
  }
  return x || null;
}
```
- example usage
```shell
...
  loader.emitError(payload.message);
},

emitFile: function(loader, payload) {
  loader.emitFile(
    payload.name,
    payload.contents,
    SourceMapSerializer.deserialize(payload.sourceMap)
  );
},

addDependency: function(loader, payload) {
  loader.addDependency(payload.file);
},
...
```

#### <a name="apidoc.element.happypack.SourceMapSerializer.serialize"></a>[function <span class="apidocSignatureSpan">happypack.SourceMapSerializer.</span>serialize (x)](#apidoc.element.happypack.SourceMapSerializer.serialize)
- description and source-code
```javascript
serialize = function (x) {
  if (typeof x === 'string') {
    return x;
  }
  else {
    return JSON.stringify(x || null);
  }
}
```
- example usage
```shell
...

if (err) {
  console.error(err);
  fs.writeFileSync(compiledPath, serializeError(err), 'utf-8');
}
else {
  fs.writeFileSync(compiledPath, source);
  fs.writeFileSync(compiledPath + '.map', SourceMapSerializer.serialize(sourceMap));

  success = true;
}

done({
  sourcePath: params.loaderContext.resourcePath,
  compiledPath: compiledPath,
...
```



# <a name="apidoc.module.happypack.WebpackUtils"></a>[module happypack.WebpackUtils](#apidoc.module.happypack.WebpackUtils)

#### <a name="apidoc.element.happypack.WebpackUtils.applyLoaders"></a>[function <span class="apidocSignatureSpan">happypack.WebpackUtils.</span>applyLoaders (runContext, sourceCode, sourceMap, done)](#apidoc.element.happypack.WebpackUtils.applyLoaders)
- description and source-code
```javascript
function applyLoaders(runContext, sourceCode, sourceMap, done) {
  assert(runContext.compiler, "Missing webpack compiler instance!");

  // we start out by creating fake loader contexts for every loader
  var loaders = runContext.loaders.map(function(loader) {
    return {
      request: loader.request,
      path: loader.path,
      query: loader.query,
      module: require(loader.path),

      // TODO: this is probably not the best place to create the context, and it
      // also should be cached at some layer
      context: HappyFakeLoaderContext({
        _compiler: runContext.compiler, // for compiler RPCs
        _remoteLoaderId: runContext.loaderContext.remoteLoaderId, // for loader RPCs
        fs: runContext.compiler.inputFileSystem,

        query: loader.query,
        options: runContext.compiler.options,

        request: runContext.loaderContext.request,
        resource: runContext.loaderContext.resource,
        resourcePath: runContext.loaderContext.resourcePath,
        resourceQuery: runContext.loaderContext.resourceQuery,
        context: runContext.loaderContext.context,

        sourceMap: Boolean(runContext.loaderContext.useSourceMap),
        target: runContext.loaderContext.target,
      })
    };
  });

  loaders.forEach(function exposeLoaderSetToEachLoader(loader, index) {
    loader.context.loaders = loaders;
    loader.context.loaderIndex = index;
  });

  // Go through the pitching phase. This might affect the loader contexts.
  applyPitchLoaders(runContext.loaderContext.request, loaders, function(err, pitchResult) {
    if (err) {
      return done(err);
    }

    var apply = NormalLoaderApplier(loaders, pitchResult.dataMap, done);

    // pitching phase did yield something so we skip the loaders to the right
    // and use the yielded code as the starting sourceCode
    if (pitchResult.sourceCode) {
      apply(pitchResult.cursor - 1, pitchResult.sourceCode, pitchResult.sourceMap);
    }
    // otherwise, we just start from the right-most loader using the input
    // source code and map:
    else {
      apply(loaders.length - 1, sourceCode, sourceMap);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.WebpackUtils.extractLoaders"></a>[function <span class="apidocSignatureSpan">happypack.WebpackUtils.</span>extractLoaders (entry)](#apidoc.element.happypack.WebpackUtils.extractLoaders)
- description and source-code
```javascript
function extractLoaders(entry) {
  if (typeof entry === 'object' && entry.loaders) {
    return entry.loaders.reduce(function(list, loader) {
      return list.concat(extractLoaders(loader));
    }, []);
  }
  else if (typeof entry === 'string') {
    return extractPathAndQueryFromString(entry);
  }
  else if (typeof entry.loader === 'string' && entry.query) {
    return { path: entry.loader, query: entry.query };
  }
  else if (typeof entry.loader === 'string' && entry.options) {
    return { path: entry.loader, query: '?' + JSON.stringify(entry.options) };
  }
  else if (typeof entry.loader === 'string') {
    return extractPathAndQueryFromString(entry.loader);
  }
  else {
    console.error(entry);
    assert(false, "HappyPack: Unrecognized loader configuration variant!");
  }
}
```
- example usage
```shell
...

// happypack variant:
if (typeof input === 'object' && input.hasOwnProperty('path')) {
  normals = [ objectAssign({}, input) ];
}
// webpack object variant:
else if (typeof input === 'object') {
  normals = [].concat(exports.extractLoaders(input));
}
// webpack/happypack string loader(s):
else if (typeof input === 'string') {
  normals = [].concat(extractPathAndQueryFromString(input));
}

return normals.map(function(loader) {
...
```

#### <a name="apidoc.element.happypack.WebpackUtils.normalizeLoader"></a>[function <span class="apidocSignatureSpan">happypack.WebpackUtils.</span>normalizeLoader (input)](#apidoc.element.happypack.WebpackUtils.normalizeLoader)
- description and source-code
```javascript
normalizeLoader = function (input) {
  var normals;

  // happypack variant:
  if (typeof input === 'object' && input.hasOwnProperty('path')) {
    normals = [ objectAssign({}, input) ];
  }
  // webpack object variant:
  else if (typeof input === 'object') {
    normals = [].concat(exports.extractLoaders(input));
  }
  // webpack/happypack string loader(s):
  else if (typeof input === 'string') {
    normals = [].concat(extractPathAndQueryFromString(input));
  }

  return normals.map(function(loader) {
    // normalize the query so that it is always a string prefixed by '?'
    if (loader.query) {
      if (typeof loader.query === 'object') {
        loader.query = '?' + JSON.stringify(loader.query);
      }
      else if (typeof loader.query === 'string') {
        loader.query = ensureHasLeadingMarker(loader.query);
      }
    }

    // be compatible with webpack's syntax within our own: if they specify
    // a loader's path using a "loader" attribute, map it to the "path" one
    if (loader.loader) {
      loader.path = loader.loader;
      delete loader.loader;
    }

    return loader;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.happypack.WebpackUtils.resolveLoaders"></a>[function <span class="apidocSignatureSpan">happypack.WebpackUtils.</span>resolveLoaders (compiler, loaders, done)](#apidoc.element.happypack.WebpackUtils.resolveLoaders)
- description and source-code
```javascript
resolveLoaders = function (compiler, loaders, done) {
  var resolve = compiler.resolvers.loader.resolve;
  var resolveContext = compiler.resolvers.loader;

  // webpack2 has changed the signature for the resolve method where it accepts
  // a fourth argument (context), so we need to sniff and support both versions
  //
  // fixes #23
  var isWebpack2 = resolve.length === 4;

  async.parallel(loaders.map(function(loader) {
    assert(!!loader, "Invalid loader string to resolve!!! " + JSON.stringify(loaders));

    return function(callback) {
      var callArgs = [ compiler.context, loader, function(err, result) {
        if (err) {
          return callback(err);
        }

        callback(null, result);
      }];

      if (isWebpack2) {
        resolve.apply(resolveContext, [ compiler.context ].concat(callArgs));
      }
      else {
        resolve.apply(resolveContext, callArgs);
      }
    };
  }), done);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
