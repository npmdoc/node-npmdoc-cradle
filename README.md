# api documentation for  [cradle (v0.7.1)](https://github.com/flatiron/cradle#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-cradle.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-cradle) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-cradle.svg)](https://travis-ci.org/npmdoc/node-npmdoc-cradle)
#### the high-level, caching, CouchDB library

[![NPM](https://nodei.co/npm/cradle.png?downloads=true)](https://www.npmjs.com/package/cradle)

[![apidoc](https://npmdoc.github.io/node-npmdoc-cradle/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-cradle_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-cradle/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-cradle/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-cradle/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Alexis Sellier",
        "email": "self@cloudhead.net"
    },
    "bugs": {
        "url": "https://github.com/flatiron/cradle/issues"
    },
    "contributors": [
        {
            "name": "Charlie Robbins",
            "email": "charlie@nodejitsu.com"
        },
        {
            "name": "Maciej Malecki",
            "email": "maciej@nodejitsu.com"
        }
    ],
    "dependencies": {
        "follow": "0.11.x",
        "request": "2.x.x",
        "vargs": "0.1.0"
    },
    "description": "the high-level, caching, CouchDB library",
    "devDependencies": {
        "async": "~0.9.0",
        "proxyquire": "^1.7.3",
        "sinon": "^1.17.2",
        "vows": "0.8.x"
    },
    "directories": {},
    "dist": {
        "shasum": "4c0b354aadfb7d4ae2a8f5cdbbfd63a345061044",
        "tarball": "https://registry.npmjs.org/cradle/-/cradle-0.7.1.tgz"
    },
    "engines": {
        "node": ">=0.8.0"
    },
    "gitHead": "20534493ae3aa0e6d80201a24b48acf19a27e4ac",
    "homepage": "https://github.com/flatiron/cradle#readme",
    "keywords": [
        "couchdb",
        "database",
        "couch"
    ],
    "license": "MIT",
    "main": "./lib/cradle",
    "maintainers": [
        {
            "name": "cloudhead",
            "email": "self@cloudhead.net"
        },
        {
            "name": "indexzero",
            "email": "charlie.robbins@gmail.com"
        },
        {
            "name": "nawitus",
            "email": "panu.horsmalahti@iki.fi"
        }
    ],
    "name": "cradle",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/flatiron/cradle.git"
    },
    "scripts": {
        "test": "node test/helpers/seed.js && vows --spec"
    },
    "url": "http://cloudhead.io/cradle",
    "version": "0.7.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module cradle](#apidoc.module.cradle)
1.  [function <span class="apidocSignatureSpan">cradle.</span>Cache (options)](#apidoc.element.cradle.Cache)
1.  [function <span class="apidocSignatureSpan">cradle.</span>Connection ()](#apidoc.element.cradle.Connection)
1.  [function <span class="apidocSignatureSpan">cradle.</span>CouchError (err)](#apidoc.element.cradle.CouchError)
1.  [function <span class="apidocSignatureSpan">cradle.</span>CouchError.super_ ()](#apidoc.element.cradle.CouchError.super_)
1.  [function <span class="apidocSignatureSpan">cradle.</span>Database (name, connection)](#apidoc.element.cradle.Database)
1.  [function <span class="apidocSignatureSpan">cradle.</span>Response (json, response)](#apidoc.element.cradle.Response)
1.  [function <span class="apidocSignatureSpan">cradle.</span>escape (id)](#apidoc.element.cradle.escape)
1.  [function <span class="apidocSignatureSpan">cradle.</span>extend (obj, properties)](#apidoc.element.cradle.extend)
1.  [function <span class="apidocSignatureSpan">cradle.</span>merge (target)](#apidoc.element.cradle.merge)
1.  [function <span class="apidocSignatureSpan">cradle.</span>setup (settings)](#apidoc.element.cradle.setup)
1.  number <span class="apidocSignatureSpan">cradle.</span>port
1.  object <span class="apidocSignatureSpan">cradle.</span>Cache.prototype
1.  object <span class="apidocSignatureSpan">cradle.</span>Connection.prototype
1.  object <span class="apidocSignatureSpan">cradle.</span>Database.prototype
1.  object <span class="apidocSignatureSpan">cradle.</span>auth
1.  object <span class="apidocSignatureSpan">cradle.</span>ca
1.  object <span class="apidocSignatureSpan">cradle.</span>options
1.  string <span class="apidocSignatureSpan">cradle.</span>host

#### [module cradle.Cache](#apidoc.module.cradle.Cache)
1.  [function <span class="apidocSignatureSpan">cradle.</span>Cache (options)](#apidoc.element.cradle.Cache.Cache)

#### [module cradle.Cache.prototype](#apidoc.module.cradle.Cache.prototype)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>_get (id)](#apidoc.element.cradle.Cache.prototype._get)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>_has (id)](#apidoc.element.cradle.Cache.prototype._has)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>_purge (id)](#apidoc.element.cradle.Cache.prototype._purge)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>_save (id, doc)](#apidoc.element.cradle.Cache.prototype._save)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>get (id)](#apidoc.element.cradle.Cache.prototype.get)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>has (id)](#apidoc.element.cradle.Cache.prototype.has)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>prune ()](#apidoc.element.cradle.Cache.prototype.prune)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>purge (id)](#apidoc.element.cradle.Cache.prototype.purge)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>query (op, id, doc)](#apidoc.element.cradle.Cache.prototype.query)
1.  [function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>save (id, doc)](#apidoc.element.cradle.Cache.prototype.save)

#### [module cradle.Connection](#apidoc.module.cradle.Connection)
1.  [function <span class="apidocSignatureSpan">cradle.</span>Connection ()](#apidoc.element.cradle.Connection.Connection)

#### [module cradle.Connection.prototype](#apidoc.module.cradle.Connection.prototype)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>_url (path)](#apidoc.element.cradle.Connection.prototype._url)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>activeTasks (callback)](#apidoc.element.cradle.Connection.prototype.activeTasks)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>close ()](#apidoc.element.cradle.Connection.prototype.close)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>config (callback)](#apidoc.element.cradle.Connection.prototype.config)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>database (name)](#apidoc.element.cradle.Connection.prototype.database)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>databases (callback)](#apidoc.element.cradle.Connection.prototype.databases)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>info (callback)](#apidoc.element.cradle.Connection.prototype.info)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>rawRequest (options, callback)](#apidoc.element.cradle.Connection.prototype.rawRequest)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>replicate (options, callback)](#apidoc.element.cradle.Connection.prototype.replicate)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>request (options, callback)](#apidoc.element.cradle.Connection.prototype.request)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>stats (callback)](#apidoc.element.cradle.Connection.prototype.stats)
1.  [function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>uuids (count, callback)](#apidoc.element.cradle.Connection.prototype.uuids)

#### [module cradle.CouchError](#apidoc.module.cradle.CouchError)
1.  [function <span class="apidocSignatureSpan">cradle.</span>CouchError (err)](#apidoc.element.cradle.CouchError.CouchError)
1.  [function <span class="apidocSignatureSpan">cradle.CouchError.</span>super_ ()](#apidoc.element.cradle.CouchError.super_)

#### [module cradle.CouchError.super_](#apidoc.module.cradle.CouchError.super_)
1.  [function <span class="apidocSignatureSpan">cradle.CouchError.</span>super_ ()](#apidoc.element.cradle.CouchError.super_.super_)
1.  [function <span class="apidocSignatureSpan">cradle.CouchError.super_.</span>captureStackTrace ()](#apidoc.element.cradle.CouchError.super_.captureStackTrace)
1.  number <span class="apidocSignatureSpan">cradle.CouchError.super_.</span>stackTraceLimit

#### [module cradle.Database](#apidoc.module.cradle.Database)
1.  [function <span class="apidocSignatureSpan">cradle.</span>Database (name, connection)](#apidoc.element.cradle.Database.Database)

#### [module cradle.Database.prototype](#apidoc.module.cradle.Database.prototype)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>_getOrPostView (path, options, callback)](#apidoc.element.cradle.Database.prototype._getOrPostView)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>_merge (id, doc, callback)](#apidoc.element.cradle.Database.prototype._merge)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>_save (id, rev, doc, callback)](#apidoc.element.cradle.Database.prototype._save)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>addAttachment (doc, attachment, callback)](#apidoc.element.cradle.Database.prototype.addAttachment)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>all (options, callback)](#apidoc.element.cradle.Database.prototype.all)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>changes (options, callback)](#apidoc.element.cradle.Database.prototype.changes)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>compact (design)](#apidoc.element.cradle.Database.prototype.compact)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>create (callback)](#apidoc.element.cradle.Database.prototype.create)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>destroy (callback)](#apidoc.element.cradle.Database.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>exists (callback)](#apidoc.element.cradle.Database.prototype.exists)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>fti (path, options, callback)](#apidoc.element.cradle.Database.prototype.fti)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>get (id, rev)](#apidoc.element.cradle.Database.prototype.get)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>getAttachment (id, attachmentName, callback)](#apidoc.element.cradle.Database.prototype.getAttachment)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>head (id, callback)](#apidoc.element.cradle.Database.prototype.head)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>info (callback)](#apidoc.element.cradle.Database.prototype.info)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>insert ()](#apidoc.element.cradle.Database.prototype.insert)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>list (path, options)](#apidoc.element.cradle.Database.prototype.list)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>merge ()](#apidoc.element.cradle.Database.prototype.merge)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>post (doc, callback)](#apidoc.element.cradle.Database.prototype.post)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>put (id, doc, callback)](#apidoc.element.cradle.Database.prototype.put)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>query (options, callback)](#apidoc.element.cradle.Database.prototype.query)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>remove (id, rev)](#apidoc.element.cradle.Database.prototype.remove)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>removeAttachment (doc, attachmentName, callback)](#apidoc.element.cradle.Database.prototype.removeAttachment)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>replicate (target, options, callback)](#apidoc.element.cradle.Database.prototype.replicate)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>save ()](#apidoc.element.cradle.Database.prototype.save)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>saveAttachment (doc, attachment, callback)](#apidoc.element.cradle.Database.prototype.saveAttachment)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>temporaryView (doc, options, callback)](#apidoc.element.cradle.Database.prototype.temporaryView)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>update (path, id, options, body)](#apidoc.element.cradle.Database.prototype.update)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>view (path, options, callback)](#apidoc.element.cradle.Database.prototype.view)
1.  [function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>viewCleanup (callback)](#apidoc.element.cradle.Database.prototype.viewCleanup)



# <a name="apidoc.module.cradle"></a>[module cradle](#apidoc.module.cradle)

#### <a name="apidoc.element.cradle.Cache"></a>[function <span class="apidocSignatureSpan">cradle.</span>Cache (options)](#apidoc.element.cradle.Cache)
- description and source-code
```javascript
Cache = function (options) {
    var that = this;

    this.store   = {};
    this.options = options;
    this.size = options.cacheSize || 0;
    this.keys = 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection"></a>[function <span class="apidocSignatureSpan">cradle.</span>Connection ()](#apidoc.element.cradle.Connection)
- description and source-code
```javascript
function Connection() {
    var args = Array.prototype.slice.call(arguments),
        options = {},
        remote,
        match,
        host,
        port,
        ca,
        agentOptions = {},
        auth;

    args.forEach(function (a) {
        if (typeof(a) === 'number' || (typeof(a) === 'string' && /^\d{2,5}$/.test(a))) {
            port = parseInt(a);
        } else if (typeof(a) === 'object') {
            options = a;
            host = host || options.hostname || options.host;
            port = port || options.port;
            auth = options.auth;
            ca = options.ca;
        } else {
            host = a;

            if (match = host.match(/^(.+)\:(\d{2,5})$/)) {
                host = match[1];
                port = parseInt(match[2]);
            }
        }
    });

    if (typeof auth == "string") {
        // probaby via a url.parse()
        var userpass = auth.split(":");
        auth = {};
        auth.username = userpass[0];
        auth.password = userpass[1] || null;
    }

    this.host    = host || cradle.host;
    this.port    = port || cradle.port;
    this.auth    = auth || cradle.auth;
    this.ca      = ca   || cradle.ca;
    this.options = cradle.merge({}, cradle.options, options);

    this.options.maxSockets = this.options.maxSockets || 20;
    this.options.secure     = this.options.secure     || this.options.ssl;

    if (protocolPattern.test(this.host)) {
        this.protocol = this.host.match(protocolPattern)[1];
        this.host     = this.host.replace(protocolPattern, '');
    }

    if (this.protocol === 'https') this.options.secure = true;

    if (!this.protocol) {
        this.protocol = (this.options.secure) ? 'https' : 'http';
    }

    if (this.options.ssl) { // Deprecation warning
        console.log('Warning: "ssl" option is deprecated. Use "secure" instead.');
    }

    agentOptions.host = this.host;
    agentOptions.port = this.port;
    if (this.options.secure) {
        this.transport = https;
        if (this.ca) {
            agentOptions.ca = this.ca;
        }
    } else {
        this.transport = http;
    }
    this.agent = new (this.transport.Agent)(agentOptions);

    this.agent.maxSockets = this.options.maxSockets;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.CouchError"></a>[function <span class="apidocSignatureSpan">cradle.</span>CouchError (err)](#apidoc.element.cradle.CouchError)
- description and source-code
```javascript
function CouchError(err) {
	// ensure proper stack trace
	Error.call(this);
	Error.captureStackTrace(this, this.constructor);

	this.name = this.constructor.name;
	this.message = err.error + ': ' + err.reason;

	// add properties from CouchDB error response to Error object
	for (var k in err) {
		if (err.hasOwnProperty(k)) {
			this[k] = err[k];
		}
	}
    this.headers = err.headers;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.CouchError.super_"></a>[function <span class="apidocSignatureSpan">cradle.</span>CouchError.super_ ()](#apidoc.element.cradle.CouchError.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database"></a>[function <span class="apidocSignatureSpan">cradle.</span>Database (name, connection)](#apidoc.element.cradle.Database)
- description and source-code
```javascript
Database = function (name, connection) {
    this.connection = connection;
    this.name = encodeURIComponent(name);
    this.cache = new (cradle.Cache)(connection.options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Response"></a>[function <span class="apidocSignatureSpan">cradle.</span>Response (json, response)](#apidoc.element.cradle.Response)
- description and source-code
```javascript
function Response(json, response) {
    var obj, headers;

    // If there's an _id key, it's the result
    // of a document retrieval.
    // Avoid potential key collisions.
    if (!json._id) {
        // If there's rows, this is the result
        // of a view function.
        // We want to return this as an Array.
        if (json.rows) {
            obj           = json.rows.slice(0);
            obj.__proto__ = new(Array);
            if (json && typeof json === 'object') {
                Object.keys(json).forEach(function (k) {
                    Object.defineProperty(obj.__proto__, k, {
                        value:      json[k],
                        enumerable: false
                    });
                });
            }
        } else if (json.results) {
            obj = json.results.slice(0);
            obj.__proto__ = new(Array);
            obj.last_seq  = json.last_seq;
        } else if (json.uuids) {
            obj           = json.uuids;
            obj.__proto__ = new(Array);
        } else if (Array.isArray(json)) {
            obj           = json.slice(0);
            obj.__proto__ = new(Array);
        }
    }

    if (!obj) {
        obj           = {};
        obj.__proto__ = new(Object);
        if (json && typeof json === 'object') {
            Object.keys(json).forEach(function (k) {
                obj[k] = json[k];
            });
        }
    }

    // If the response was originally a document,
    // give access to it via the 'json' getter.
    if (!Array.isArray(json) && !obj.json) {
        Object.defineProperty(obj, 'json', {
            value: json,
            enumerable: false
        });
    }

    if (response) {
        headers = { status: response.statusCode };
        Object.keys(response.headers).forEach(function (k) {
            headers[k] = response.headers[k];
        });

        // Set the 'headers' special field, with the response's status code.
        exports.extend(obj, 'headers' in obj ? { _headers: headers }
                                             : {  headers: headers });
    }

    // Alias '_rev' and '_id'
    if (obj.id && obj.rev) {
        exports.extend(obj, { _id:  obj.id, _rev: obj.rev });
    } else if (obj._id && obj._rev) {
        exports.extend(obj, { id:  obj._id, rev: obj._rev });
    }

    if (Array.isArray(obj) && json.rows) {
        exports.extend(obj, exports.collectionPrototype);
    }
    exports.extend(obj, exports.basePrototype);

    // Set the constructor to be this function
    Object.defineProperty(obj, 'constructor', {
        value: arguments.callee
    });

    return obj;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.escape"></a>[function <span class="apidocSignatureSpan">cradle.</span>escape (id)](#apidoc.element.cradle.escape)
- description and source-code
```javascript
escape = function (id) {
    return ['_design', '_changes', '_temp_view'].indexOf(id.split('/')[0]) === -1
        ? querystring.escape(id)
        : id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.extend"></a>[function <span class="apidocSignatureSpan">cradle.</span>extend (obj, properties)](#apidoc.element.cradle.extend)
- description and source-code
```javascript
extend = function (obj, properties) {
    var descriptor = Object.keys(properties).reduce(function (hash, k) {
        hash[k] = {
            value: properties[k],
            enumerable: false
        };
        return hash;
    }, {});
    return Object.defineProperties(obj, descriptor);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.merge"></a>[function <span class="apidocSignatureSpan">cradle.</span>merge (target)](#apidoc.element.cradle.merge)
- description and source-code
```javascript
merge = function (target) {
    var objs = Array.prototype.slice.call(arguments, 1);
    objs.forEach(function (o) {
        Object.keys(o).forEach(function (attr) {
            if (! o.__lookupGetter__(attr)) {
                target[attr] = o[attr];
            }
        });
    });
    return target;
}
```
- example usage
```shell
...
'''

Note that when saving a document this way, CouchDB overwrites the existing document with the new one. If you want to update only
 certain fields of the document, you have to fetch it first (with 'get'), make your changes, then resave the modified document with
 the above method.

If you only want to update one or more attributes, and leave the others untouched, you can use the 'merge()' method:

''' js
  db.merge('luke', {jedi: true}, function (err, res) {
      // Luke is now a jedi,
      // but remains on the dark side of the force.
  });
'''

Note that we didn't pass a '_rev', this only works because we previously saved a full version of 'luke', and the 'cache' option
is enabled.
...
```

#### <a name="apidoc.element.cradle.setup"></a>[function <span class="apidocSignatureSpan">cradle.</span>setup (settings)](#apidoc.element.cradle.setup)
- description and source-code
```javascript
setup = function (settings) {
    this.host = settings.host;
    this.auth = settings.auth;
    if (settings.port) {
        this.port = parseInt(settings.port, 10);
    }
    cradle.merge(this.options, settings);

    return this;
}
```
- example usage
```shell
...
'''

_Defaults to '127.0.0.1:5984'_

Note that you can also use 'cradle.setup' to set a global configuration:

''' js
cradle.setup({
  host: 'living-room.couch',
  cache: true,
  raw: false,
  forceSave: true
});

var c = new(cradle.Connection),
...
```



# <a name="apidoc.module.cradle.Cache"></a>[module cradle.Cache](#apidoc.module.cradle.Cache)

#### <a name="apidoc.element.cradle.Cache.Cache"></a>[function <span class="apidocSignatureSpan">cradle.</span>Cache (options)](#apidoc.element.cradle.Cache.Cache)
- description and source-code
```javascript
Cache = function (options) {
    var that = this;

    this.store   = {};
    this.options = options;
    this.size = options.cacheSize || 0;
    this.keys = 0;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cradle.Cache.prototype"></a>[module cradle.Cache.prototype](#apidoc.module.cradle.Cache.prototype)

#### <a name="apidoc.element.cradle.Cache.prototype._get"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>_get (id)](#apidoc.element.cradle.Cache.prototype._get)
- description and source-code
```javascript
_get = function (id) {
    var entry;

    if (id in this.store) {
        entry = this.store[id];
        entry.atime = Date.now();

        if (this.options.raw) {
            return entry.document;
        } else {
            // If the document is already wrapped in a 'Response',
            // just return it. Else, wrap it first. We clone the documents
            // before returning them, to protect them from modification.
            if (entry.document.toJSON) {
                return clone(entry.document);
            } else {
                return new(Response)(clone(entry.document));
            }
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Cache.prototype._has"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>_has (id)](#apidoc.element.cradle.Cache.prototype._has)
- description and source-code
```javascript
_has = function (id) {
    return id in this.store;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Cache.prototype._purge"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>_purge (id)](#apidoc.element.cradle.Cache.prototype._purge)
- description and source-code
```javascript
_purge = function (id) {
    if (id) {
        delete(this.store[id]);
        this.keys --;
    } else {
        this.store = {};
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Cache.prototype._save"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>_save (id, doc)](#apidoc.element.cradle.Cache.prototype._save)
- description and source-code
```javascript
_save = function (id, doc) {
    if (! this._has(id)) {
        this.keys ++;
        this.prune();
    }

    this.store[id] = {
        atime:    Date.now(),
        document: doc
    };

    return this.store[id];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Cache.prototype.get"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>get (id)](#apidoc.element.cradle.Cache.prototype.get)
- description and source-code
```javascript
get = function (id)      { return this.query('get',   id); }
```
- example usage
```shell
...
synopsis
--------

''' js
var cradle = require('cradle');
var db = new(cradle.Connection)().database('starwars');

db.get('vader', function (err, doc) {
    doc.name; // 'Darth Vader'
    assert.equal(doc.force, 'dark');
});

db.save('skywalker', {
    force: 'light',
    name: 'Luke Skywalker'
...
```

#### <a name="apidoc.element.cradle.Cache.prototype.has"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>has (id)](#apidoc.element.cradle.Cache.prototype.has)
- description and source-code
```javascript
has = function (id)      { return this.query('has',   id); }
```
- example usage
```shell
...

### cache API ###

When cache is enabled (default is true), a document is loaded into cradle's cache when it's retrieved or saved. In the event you
 wish to keep caching enabled, but invalidate specific items - such as those which may have been updated elsewhere. You can use
the API below.

**HAS**
'''js
db.cache.has('docid');  //returns true if exists, false if not
'''

**GET**
'''js
db.cache.get('docid');  //returns the document from the cache
'''
...
```

#### <a name="apidoc.element.cradle.Cache.prototype.prune"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>prune ()](#apidoc.element.cradle.Cache.prototype.prune)
- description and source-code
```javascript
prune = function () {
    var that = this;
    if (this.size && this.keys > this.size) {
        process.nextTick(function () {
            var store  = that.store,
                keys   = Object.keys(store),
                pruned = Math.ceil(that.size / 8);

            keys.sort(function (a, b) {
                return store[a].atime > store[b].atime ? 1 : -1;
            });

            for (var i = 0; i < pruned; i++) {
                delete(store[keys[i]]);
            }
            that.keys -= pruned;
        });
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Cache.prototype.purge"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>purge (id)](#apidoc.element.cradle.Cache.prototype.purge)
- description and source-code
```javascript
purge = function (id)      { return this.query('purge', id); }
```
- example usage
```shell
...
**GET**
'''js
db.cache.get('docid');  //returns the document from the cache
'''

**PURGE**
'''js
db.cache.purge('docid');  //remove this item from the cache
'''

**SAVE**
'''js
db.cache.save('docid', doc);  //saves the provided document into the cache
'''
...
```

#### <a name="apidoc.element.cradle.Cache.prototype.query"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>query (op, id, doc)](#apidoc.element.cradle.Cache.prototype.query)
- description and source-code
```javascript
query = function (op, id, doc) {
    if (this.options.cache) {
        return this['_' + op](id, doc);
    } else {
        return false;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Cache.prototype.save"></a>[function <span class="apidocSignatureSpan">cradle.Cache.prototype.</span>save (id, doc)](#apidoc.element.cradle.Cache.prototype.save)
- description and source-code
```javascript
save = function (id, doc) { return this.query('save',  id, doc); }
```
- example usage
```shell
...
var db = new(cradle.Connection)().database('starwars');

db.get('vader', function (err, doc) {
    doc.name; // 'Darth Vader'
    assert.equal(doc.force, 'dark');
});

db.save('skywalker', {
    force: 'light',
    name: 'Luke Skywalker'
}, function (err, res) {
    if (err) {
        // Handle error
    } else {
        // Handle success
...
```



# <a name="apidoc.module.cradle.Connection"></a>[module cradle.Connection](#apidoc.module.cradle.Connection)

#### <a name="apidoc.element.cradle.Connection.Connection"></a>[function <span class="apidocSignatureSpan">cradle.</span>Connection ()](#apidoc.element.cradle.Connection.Connection)
- description and source-code
```javascript
function Connection() {
    var args = Array.prototype.slice.call(arguments),
        options = {},
        remote,
        match,
        host,
        port,
        ca,
        agentOptions = {},
        auth;

    args.forEach(function (a) {
        if (typeof(a) === 'number' || (typeof(a) === 'string' && /^\d{2,5}$/.test(a))) {
            port = parseInt(a);
        } else if (typeof(a) === 'object') {
            options = a;
            host = host || options.hostname || options.host;
            port = port || options.port;
            auth = options.auth;
            ca = options.ca;
        } else {
            host = a;

            if (match = host.match(/^(.+)\:(\d{2,5})$/)) {
                host = match[1];
                port = parseInt(match[2]);
            }
        }
    });

    if (typeof auth == "string") {
        // probaby via a url.parse()
        var userpass = auth.split(":");
        auth = {};
        auth.username = userpass[0];
        auth.password = userpass[1] || null;
    }

    this.host    = host || cradle.host;
    this.port    = port || cradle.port;
    this.auth    = auth || cradle.auth;
    this.ca      = ca   || cradle.ca;
    this.options = cradle.merge({}, cradle.options, options);

    this.options.maxSockets = this.options.maxSockets || 20;
    this.options.secure     = this.options.secure     || this.options.ssl;

    if (protocolPattern.test(this.host)) {
        this.protocol = this.host.match(protocolPattern)[1];
        this.host     = this.host.replace(protocolPattern, '');
    }

    if (this.protocol === 'https') this.options.secure = true;

    if (!this.protocol) {
        this.protocol = (this.options.secure) ? 'https' : 'http';
    }

    if (this.options.ssl) { // Deprecation warning
        console.log('Warning: "ssl" option is deprecated. Use "secure" instead.');
    }

    agentOptions.host = this.host;
    agentOptions.port = this.port;
    if (this.options.secure) {
        this.transport = https;
        if (this.ca) {
            agentOptions.ca = this.ca;
        }
    } else {
        this.transport = http;
    }
    this.agent = new (this.transport.Agent)(agentOptions);

    this.agent.maxSockets = this.options.maxSockets;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cradle.Connection.prototype"></a>[module cradle.Connection.prototype](#apidoc.module.cradle.Connection.prototype)

#### <a name="apidoc.element.cradle.Connection.prototype._url"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>_url (path)](#apidoc.element.cradle.Connection.prototype._url)
- description and source-code
```javascript
_url = function (path) {
    var url = (this.protocol || 'http') + '://' + this.host;
    if (this.port !== 443 && this.port !== 80) {
        url += ':' + this.port;
    }

    url += path[0] === '/' ? path : ('/' + path);
    return url;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.activeTasks"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>activeTasks (callback)](#apidoc.element.cradle.Connection.prototype.activeTasks)
- description and source-code
```javascript
activeTasks = function (callback) {
    this.request({ path: '/_active_tasks' }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.close"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>close ()](#apidoc.element.cradle.Connection.prototype.close)
- description and source-code
```javascript
close = function () {
  this.agent.sockets.forEach(function (socket) {
      socket.end();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.config"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>config (callback)](#apidoc.element.cradle.Connection.prototype.config)
- description and source-code
```javascript
config = function (callback) {
    this.request({ path: '/_config' }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.database"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>database (name)](#apidoc.element.cradle.Connection.prototype.database)
- description and source-code
```javascript
database = function (name) {
    return new cradle.Database(name, this)
}
```
- example usage
```shell
...
Cradle's API, although closely knit with CouchDB's, isn't overly so. Whenever the API can be abstracted in a friendlier, simpler
 way, that's the route it takes. So even though a large part of the 'Cradle <--> CouchDB' mappings are one to one, some Cradle functions
, such as 'save()', can perform more than one operation, depending on how they are used.

synopsis
--------

''' js
var cradle = require('cradle');
var db = new(cradle.Connection)().database('starwars');

db.get('vader', function (err, doc) {
    doc.name; // 'Darth Vader'
    assert.equal(doc.force, 'dark');
});

db.save('skywalker', {
...
```

#### <a name="apidoc.element.cradle.Connection.prototype.databases"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>databases (callback)](#apidoc.element.cradle.Connection.prototype.databases)
- description and source-code
```javascript
databases = function (callback) {
    this.request({ path: '/_all_dbs' }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.info"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>info (callback)](#apidoc.element.cradle.Connection.prototype.info)
- description and source-code
```javascript
info = function (callback) {
    this.request({ path: '/' }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.rawRequest"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>rawRequest (options, callback)](#apidoc.element.cradle.Connection.prototype.rawRequest)
- description and source-code
```javascript
rawRequest = function (options, callback) {
    var promise = new(events.EventEmitter),
        self = this;

    // HTTP Headers
    options.headers = options.headers || {};

    // Set HTTP Basic Auth
    if (this.auth) {
        options.auth = this.auth;
    }

    // Set client-wide headers
    Object.keys(this.options.headers).forEach(function (header) {
        options.headers[header] = self.options.headers[header];
    });

    if (options.query && Object.keys(options.query).length) {
        for (var k in options.query) {
            if (typeof(options.query[k]) === 'boolean') {
                options.query[k] = String(options.query[k]);
            }
        }
        options.path += '?' + querystring.stringify(options.query);
    }

    options.headers['Connection'] = options.headers['Connection'] || 'keep-alive';
    options.agent = this.agent;
    options.uri = this._url(options.path);
    delete options.path;
    options = cradle.merge(this.options.request || {}, options);

    return request(options, callback || function () { });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.replicate"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>replicate (options, callback)](#apidoc.element.cradle.Connection.prototype.replicate)
- description and source-code
```javascript
replicate = function (options, callback) {
    this.request({
        method: 'POST',
        path: '/_replicate',
        body: options
    }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.request"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>request (options, callback)](#apidoc.element.cradle.Connection.prototype.request)
- description and source-code
```javascript
request = function (options, callback) {
    var headers = cradle.merge({ host: this.host }, options.headers || {}),
        self = this;

    callback = callback || function () {};

    // HTTP Headers
    options.headers = options.headers || {};

    //
    // Handle POST/PUT data. We also convert functions to strings,
    // so they can be used in _design documents.
    //
    if (options.body) {
        options.body = JSON.stringify(options.body, function (k, val) {
            if (typeof(val) === 'function') {
                return val.toString();
            } else { return val }
        });
        options.headers["Content-Length"] = Buffer.byteLength(options.body);
        options.headers["Content-Type"]   = "application/json";
    }

    if (options.method === "DELETE" && !options.headers["Content-Length"]) {
        options.headers["Content-Length"] = 0;
    }

    var attempts = 0;
    return this.rawRequest(options, function _onResponse(err, res, body) {
        attempts++;
        if (err) {
            if (self.options.retries &&
              (!options.method || options.method.toLowerCase() === 'get' || options.body) &&
              String(err.code).indexOf('ECONN') === 0 && attempts <= self.options.retries
            ) {
              return setTimeout(
                  self.rawRequest.bind(self, options, _onResponse),
                  self.options.retryTimeout
              );
            }
            return callback(err);
        }
        else if (options.method === 'HEAD') {
            return callback(null, res.headers, res.statusCode);
        }
        else if (body && body.error) {
            cradle.extend(body, { headers: res.headers });
            body.headers.status = res.statusCode;
            return callback(new cradle.CouchError(body));
        }

        try { body = JSON.parse(body) }
        catch (err) { }

        if (body && body.error) {
            cradle.extend(body, { headers: res.headers });
            body.headers.status = res.statusCode;
            return callback(new cradle.CouchError(body));
        }

        callback(null, self.options.raw ? body : new cradle.Response(body, res));
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.stats"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>stats (callback)](#apidoc.element.cradle.Connection.prototype.stats)
- description and source-code
```javascript
stats = function (callback) {
    this.request({ path: '/_stats' }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Connection.prototype.uuids"></a>[function <span class="apidocSignatureSpan">cradle.Connection.prototype.</span>uuids (count, callback)](#apidoc.element.cradle.Connection.prototype.uuids)
- description and source-code
```javascript
uuids = function (count, callback) {
    if (typeof(count) === 'function') {
        callback = count;
        count = null;
    }

    this.request({
        method: 'GET',
        path: '/_uuids',
        query: count ? { count: count } : {}
    }, callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cradle.CouchError"></a>[module cradle.CouchError](#apidoc.module.cradle.CouchError)

#### <a name="apidoc.element.cradle.CouchError.CouchError"></a>[function <span class="apidocSignatureSpan">cradle.</span>CouchError (err)](#apidoc.element.cradle.CouchError.CouchError)
- description and source-code
```javascript
function CouchError(err) {
	// ensure proper stack trace
	Error.call(this);
	Error.captureStackTrace(this, this.constructor);

	this.name = this.constructor.name;
	this.message = err.error + ': ' + err.reason;

	// add properties from CouchDB error response to Error object
	for (var k in err) {
		if (err.hasOwnProperty(k)) {
			this[k] = err[k];
		}
	}
    this.headers = err.headers;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.CouchError.super_"></a>[function <span class="apidocSignatureSpan">cradle.CouchError.</span>super_ ()](#apidoc.element.cradle.CouchError.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cradle.CouchError.super_"></a>[module cradle.CouchError.super_](#apidoc.module.cradle.CouchError.super_)

#### <a name="apidoc.element.cradle.CouchError.super_.super_"></a>[function <span class="apidocSignatureSpan">cradle.CouchError.</span>super_ ()](#apidoc.element.cradle.CouchError.super_.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.CouchError.super_.captureStackTrace"></a>[function <span class="apidocSignatureSpan">cradle.CouchError.super_.</span>captureStackTrace ()](#apidoc.element.cradle.CouchError.super_.captureStackTrace)
- description and source-code
```javascript
function captureStackTrace() { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cradle.Database"></a>[module cradle.Database](#apidoc.module.cradle.Database)

#### <a name="apidoc.element.cradle.Database.Database"></a>[function <span class="apidocSignatureSpan">cradle.</span>Database (name, connection)](#apidoc.element.cradle.Database.Database)
- description and source-code
```javascript
Database = function (name, connection) {
    this.connection = connection;
    this.name = encodeURIComponent(name);
    this.cache = new (cradle.Cache)(connection.options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cradle.Database.prototype"></a>[module cradle.Database.prototype](#apidoc.module.cradle.Database.prototype)

#### <a name="apidoc.element.cradle.Database.prototype._getOrPostView"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>_getOrPostView (path, options, callback)](#apidoc.element.cradle.Database.prototype._getOrPostView)
- description and source-code
```javascript
_getOrPostView = function (path, options, callback) {
    options = parseOptions(options);

    if (options && options.body) {
        var body = options.body;
        delete options.body;

        return this.query({
            method: 'POST',
            path: path,
            query: options,
            body: body
        }, callback);
    }

    return this.query({
        method: 'GET',
        path: path,
        query: options
    }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype._merge"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>_merge (id, doc, callback)](#apidoc.element.cradle.Database.prototype._merge)
- description and source-code
```javascript
_merge = function (id, doc, callback) {
    var that = this;
    this.get(id, function (e, res) {
        if (e) {
            return callback(e);
        }
        doc = cradle.merge({}, res.json || res, doc);
        that.save(id, res._rev, doc, callback);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype._save"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>_save (id, rev, doc, callback)](#apidoc.element.cradle.Database.prototype._save)
- description and source-code
```javascript
_save = function (id, rev, doc, callback) {
    var options = this.connection.options;
    var document = {}, that = this;

    // Bulk Insert
    if (Array.isArray(doc)) {
        document.docs = doc;
        if (options.allOrNothing) {
            document.all_or_nothing = true;
        }
        this.query({
            method: 'POST',
            path: '/_bulk_docs',
            body: document
        }, callback);
    } else {
        if (!id && doc._id) {
            id = doc._id;
        }

        // PUT a single document, with an id (Create or Update)
        if (id) {
            // Design document
            if (/^_design\/(\w|%|\-)+$/.test(id) && !('views' in doc)) {
                document.language = "javascript";
                document.views    =  doc;
            } else {
                document = doc;
            }
            // Try to set the '_rev' attribute of the document.
            // If it wasn't passed, attempt to retrieve it from the cache.
            rev && (document._rev = rev);

            if (document._rev) {
                this.put(id, document, callback);
            } else if (this.cache.has(id)) {
                document._rev = this.cache.get(id)._rev;
                this.put(id, document, callback);
            } else {
                // Attempt to create a new document. If it fails,
                // because an existing document with that _id exists (409),
                // perform a HEAD, to get the _rev, and try to re-save.
                this.put(id, document, function (e, res) {
                    if (e && e.headers && e.headers.status === 409 && options.forceSave) { // Conflict
                        that.head(id, function (e, headers, res) {
                            if (res === 404 || !headers.etag) {
                                return callback({ reason: 'not_found' });
                            }

                            document._rev = headers.etag.slice(1, -1);
                            that.put(id, document, callback);
                        });
                    } else {
                        callback(e, res);
                    }
                });
            }
        // POST a single document, without an id (Create)
        } else {
            this.post(doc, callback);
        }
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.addAttachment"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>addAttachment (doc, attachment, callback)](#apidoc.element.cradle.Database.prototype.addAttachment)
- description and source-code
```javascript
addAttachment = function (doc, attachment, callback) {
    var attachmentName,
        options = {},
        self = this,
        params,
        error,
        rev,
        id;

    if (typeof doc === 'string') {
        id = doc;
    } else {
        id  = doc.id  || doc._id;
        rev = doc.rev || doc._rev;
    }

    if (!id) {
        error = new(TypeError)("Missing document id.");
        if (!callback) {
            throw error;
        }
        return callback(error);
    }

    attachmentName = typeof attachment !== 'string' ? attachment.name : attachment;

    if (!rev && this.cache.has(id)) {
        params = { rev: this.cache.get(id)._rev };
    } else if (rev) {
        params = { rev: rev.replace(/\"/g, '') };
    }

    options.method = 'PUT';
    options.path = '/' + [this.name, querystring.escape(id), attachmentName].join('/');
    options.headers = {
        'Content-Type': attachment['content-type'] ||
            attachment.contentType ||
            attachment['Content-Type'] ||
            'text/plain'
    };

    if (attachment.contentLength) {
        options.headers['Content-Length'] = attachment.contentLength;
    }

    if (attachment.body) {
        options.body = attachment.body;
    }

    if (params) {
        options.path += ('?' + querystring.stringify(params));
    }

    return this.connection.rawRequest(options, function (err, res, body) {
        if (err) {
            return callback(err);
        }

        var result = JSON.parse(body);
        result.headers = res.headers;
        result.headers.status = res.statusCode;

        if (result.headers.status == 201) {
            if (self.cache.has(id)) {
                // FIXME: Is this supposed to be this.cached?
                cached = self.cache.store[id].document;
                cached._rev = result.rev;
                cached._attachments = cached._attachments || {};
                cached._attachments[attachmentName] = { stub: true };
            }

            return callback(null, result);
        }

        callback(result);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.all"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>all (options, callback)](#apidoc.element.cradle.Database.prototype.all)
- description and source-code
```javascript
all = function (options, callback) {
    if (arguments.length === 1) {
      callback = options;
      options = {};
    }

    return this._getOrPostView('/_all_docs', options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.changes"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>changes (options, callback)](#apidoc.element.cradle.Database.prototype.changes)
- description and source-code
```javascript
changes = function (options, callback) {
    if (typeof(options) === 'function') {
        callback = options;
        options = {};
    }

    options = options || {};

    if (callback) {
        return this.query({
            method: 'GET',
            path: '_changes',
            query: options
        }, callback);
    }

    var response = new events.EventEmitter(),
        responded = false,
        protocol,
        auth = '',
        feed;

    if (!options.db) {
        protocol = this.connection.protocol || 'http';

        if (this.connection.auth && this.connection.auth.username && this.connection.auth.password) {
            auth = this.connection.auth.username + ':' + this.connection.auth.password + '@';
        }

        options.db = protocol + '://' + auth + this.connection.host + ':' + this.connection.port + '/' + this.name;
    }

    feed = new follow.Feed(options);
    feed.on('change', function () {
        //
        // Remark: Support the legacy 'data' events.
        //
        if (!responded) {
            responded = true;
            feed.emit('response', response);
        }

        response.emit.apply(response, ['data'].concat(Array.prototype.slice.call(arguments)));
    });

    if (options.follow !== false) {
        feed.follow();
    }

    return feed;
}
```
- example usage
```shell
...

Changes API
-----------

For a one-time '_changes' query, simply call 'db.changes' with a callback:

''' js
  db.changes(function (err, list) {
      list.forEach(function (change) { console.log(change) });
  });
'''

Or if you want to see changes since a specific sequence number:

''' js
...
```

#### <a name="apidoc.element.cradle.Database.prototype.compact"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>compact (design)](#apidoc.element.cradle.Database.prototype.compact)
- description and source-code
```javascript
compact = function (design) {
    this.query({
        method: 'POST',
        path: '/_compact' + (typeof(design) === 'string' ? '/' + querystring.escape(design) : ''),
        headers: {
            'Content-Type': 'application/json'
        }
    }, Args.last(arguments));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.create"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>create (callback)](#apidoc.element.cradle.Database.prototype.create)
- description and source-code
```javascript
create = function (callback) {
    this.query({ method: 'PUT' }, callback);
}
```
- example usage
```shell
...
     cc = new(cradle.Connection)('173.45.66.92');
'''

### creating a database ###

''' js
  var db = c.database('starwars');
  db.create(function(err){
    /* do something if there's an error */
  });
'''

#### checking for database existence ####

You can check if a database exists with the 'exists()' method.
...
```

#### <a name="apidoc.element.cradle.Database.prototype.destroy"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>destroy (callback)](#apidoc.element.cradle.Database.prototype.destroy)
- description and source-code
```javascript
destroy = function (callback) {
    if (arguments.length > 1) {
        throw new(Error)("destroy() doesn't take any additional arguments");
    }

    this.query({
        method: 'DELETE',
        path: '/',
    }, callback);
}
```
- example usage
```shell
...
  }
});
'''

### destroy a database ###

''' js
db.destroy(cb);
'''

### fetching a document _(GET)_ ###

''' js
db.get('vader', function (err, doc) {
    console.log(doc);
...
```

#### <a name="apidoc.element.cradle.Database.prototype.exists"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>exists (callback)](#apidoc.element.cradle.Database.prototype.exists)
- description and source-code
```javascript
exists = function (callback) {
    this.query({ method: 'HEAD' }, function (err, res, status) {
        if (err) {
            callback(err);
        } else {
            if (status < 200 || status > 300) {
                callback(null, false);
            } else {
                callback(null, true);
            }
        }
    });
}
```
- example usage
```shell
...
'''

#### checking for database existence ####

You can check if a database exists with the 'exists()' method.

''' js
db.exists(function (err, exists) {
  if (err) {
    console.log('error', err);
  } else if (exists) {
    console.log('the force is with you.');
  } else {
    console.log('database does not exists.');
    db.create();
...
```

#### <a name="apidoc.element.cradle.Database.prototype.fti"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>fti (path, options, callback)](#apidoc.element.cradle.Database.prototype.fti)
- description and source-code
```javascript
fti = function (path, options, callback) {
    if (typeof options === 'function') {
        callback = options;
        options = {};
    }

    path = path.split('/');
    path = ['_fti', 'local', this.name, '_design', path[0], path[1]].map(querystring.escape).join('/');

    options = parseOptions(options);

    this.connection.request({method: 'GET', path: path, query: options}, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.get"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>get (id, rev)](#apidoc.element.cradle.Database.prototype.get)
- description and source-code
```javascript
get = function (id, rev) {
    var args = new (Args)(arguments),
        options = null,
        that = this;

    if (Array.isArray(id)) { // Bulk GET
        this.query({
            method: 'POST',
            path: '/_all_docs',
            query: { include_docs: true },
            body: { keys: id },
        }, function (err, res) {
            args.callback(err, res);
        });
    } else {
        if (rev && args.length === 2) {
            if (typeof(rev) === 'string') {
                options = {
                    rev: rev
                };
            } else if (typeof(rev) === 'object') {
                options = rev;
            }
        } else if (this.cache.has(id)) {
            return args.callback(null, this.cache.get(id));
        }
        this.query({
            path: cradle.escape(id),
            query: options
        }, function (err, res) {
            if (! err) that.cache.save(res.id, res.json);
            args.callback(err, res);
        });
    }
}
```
- example usage
```shell
...
synopsis
--------

''' js
var cradle = require('cradle');
var db = new(cradle.Connection)().database('starwars');

db.get('vader', function (err, doc) {
    doc.name; // 'Darth Vader'
    assert.equal(doc.force, 'dark');
});

db.save('skywalker', {
    force: 'light',
    name: 'Luke Skywalker'
...
```

#### <a name="apidoc.element.cradle.Database.prototype.getAttachment"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>getAttachment (id, attachmentName, callback)](#apidoc.element.cradle.Database.prototype.getAttachment)
- description and source-code
```javascript
getAttachment = function (id, attachmentName, callback) {
    //
    // TODO: Update cache?
    //
    return this.connection.rawRequest({
        method: 'GET',
        path: '/' + [this.name, querystring.escape(id), attachmentName].join('/'),
        encoding: null
    }, callback);
}
```
- example usage
```shell
...


### Buffered
You can buffer the entire attachment and receive it all at once. The callback function will fire after the download is complete
or an error occurs. The second parameter in the callback will be the binary data of the attachment

**Syntax**
'''js
db.getAttachment(documentID, attachmentName, callbackFunction)
'''
**Example**
 Say you want to read back an attachment that was saved with the name 'foo.txt'
'''js
var doc = <some saved document that has an attachment with name *foo.txt*>
var id = doc._id
var attachmentName = 'foo.txt'
...
```

#### <a name="apidoc.element.cradle.Database.prototype.head"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>head (id, callback)](#apidoc.element.cradle.Database.prototype.head)
- description and source-code
```javascript
head = function (id, callback) {
    this.query({
        method: 'HEAD',
        path: cradle.escape(id)
    }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.info"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>info (callback)](#apidoc.element.cradle.Database.prototype.info)
- description and source-code
```javascript
info = function (callback) {
    this.query({ method: 'GET' }, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.insert"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>insert ()](#apidoc.element.cradle.Database.prototype.insert)
- description and source-code
```javascript
insert = function () {
    throw new Error("'insert' is deprecated, use 'save' instead");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.list"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>list (path, options)](#apidoc.element.cradle.Database.prototype.list)
- description and source-code
```javascript
list = function (path, options) {
    var callback = new(Args)(arguments).callback;
        path = path.split('/');

    this._getOrPostView(
        ['_design', path[0], '_list', path[1], path[2]].map(querystring.escape).join('/'),
        options,
        callback
    );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.merge"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>merge ()](#apidoc.element.cradle.Database.prototype.merge)
- description and source-code
```javascript
merge = function () {
    var args     = Array.prototype.slice.call(arguments),
        callback = args.pop(),
        doc      = args.pop(),
        id       = args.pop() || doc._id;

    this._merge(id, doc, callback);
}
```
- example usage
```shell
...
'''

Note that when saving a document this way, CouchDB overwrites the existing document with the new one. If you want to update only
 certain fields of the document, you have to fetch it first (with 'get'), make your changes, then resave the modified document with
 the above method.

If you only want to update one or more attributes, and leave the others untouched, you can use the 'merge()' method:

''' js
  db.merge('luke', {jedi: true}, function (err, res) {
      // Luke is now a jedi,
      // but remains on the dark side of the force.
  });
'''

Note that we didn't pass a '_rev', this only works because we previously saved a full version of 'luke', and the 'cache' option
is enabled.
...
```

#### <a name="apidoc.element.cradle.Database.prototype.post"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>post (doc, callback)](#apidoc.element.cradle.Database.prototype.post)
- description and source-code
```javascript
post = function (doc, callback) {
    var cache = this.cache;
    this.query({
        method: 'POST',
        path: '/',
        body: doc
    }, function (e, res) {
        if (! e) {
            cache.save(res.id, cradle.merge({}, doc, { _id: res.id, _rev: res.rev }));
        }
        callback && callback(e, res);
    });
}
```
- example usage
```shell
...
'''js
db.cache.save('docid', doc);  //saves the provided document into the cache
'''

**Example**
This is an example from an application using express to receive a post request when a documentid has been updated.
'''js
app.post('/dbcache/:id', function (req, res) {
if(db.cache.has(req.params.id)) {
    db.cache.purge(req.params.id);
  res.send({ status:"ok", id: req.params.id, action: 'deleted'});
}
else {
  res.send({ status:"not found", id: req.params.id, action: "none"}, 404);
}
...
```

#### <a name="apidoc.element.cradle.Database.prototype.put"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>put (id, doc, callback)](#apidoc.element.cradle.Database.prototype.put)
- description and source-code
```javascript
put = function (id, doc, callback) {
    var cache = this.cache;
    if (typeof(id) !== 'string') {
        throw new(TypeError)("id must be a string");
    }
    this.query({
        method: 'PUT',
        path: cradle.escape(id),
        body: doc
    }, function (e, res) {
        if (! e) {
            cache.save(id, cradle.merge({}, doc, { _id: id, _rev: res.rev }));
        }
        callback && callback(e, res);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.query"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>query (options, callback)](#apidoc.element.cradle.Database.prototype.query)
- description and source-code
```javascript
query = function (options, callback) {
    options.path = [this.name, options.path].filter(Boolean).join('/');
    return this.connection.request(options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.remove"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>remove (id, rev)](#apidoc.element.cradle.Database.prototype.remove)
- description and source-code
```javascript
remove = function (id, rev) {
    var that = this, doc, args = new(Args)(arguments);

    //
    // Removes the document with 'id' at 'rev'.
    //
    function remove() {
        that.query({
            method: 'DELETE',
            path: cradle.escape(id),
            query: { rev: rev }
        }, function (err, res) {
            if (! err) {
                that.cache.purge(id);
            }
            args.callback(err, res);
        });
    }

    if (typeof(rev) !== 'string') {
        if (doc = this.cache.get(id)) {
            rev = doc._rev;
        }
        else {
            return this.get(id, function (err, _doc) {
                if (err) {
                    return args.callback(err);
                }
                else if (!_doc._rev) {
                    return args.callback(new Error('No _rev found for ' + id));
                }

                rev = _doc._rev;
                remove();
            });
        }
    }

    remove();
}
```
- example usage
```shell
...
'''

### removing documents _(DELETE)_ ###

To remove a document, you call the 'remove()' method, passing the latest document revision.

''' js
  db.remove('luke', '1-94B6F82', function (err, res) {
      // Handle response
  });
'''

If 'remove' is called without a revision, and the document was recently fetched from the database, it will attempt to use the cached
 document's revision, providing caching is enabled.

### update handlers ###
...
```

#### <a name="apidoc.element.cradle.Database.prototype.removeAttachment"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>removeAttachment (doc, attachmentName, callback)](#apidoc.element.cradle.Database.prototype.removeAttachment)
- description and source-code
```javascript
removeAttachment = function (doc, attachmentName, callback) {
    var params,
        rev,
        id,
        error;

    if (typeof doc === 'string') {
        id = doc;
    } else {
        id  = doc.id  || doc._id;
        rev = doc.rev || doc._rev;
    }

    if (!id) {
        error = new(TypeError)("first argument must be a document id");
        if (!callback) {
            throw error;
        }
        return callback(error);
    }

    if (!rev && this.cache.has(id)) {
        rev = this.cache.get(id)._rev;
    } else if (rev) {
        rev = rev.replace(/\"/g, '');
    }

    this.query({
        method: 'DELETE',
        path: [querystring.escape(id), attachmentName].join('/'),
        query: { rev: rev }
    }, callback);
}
```
- example usage
```shell
...
readStream.pipe(writeStream)
'''
## Removing
You can remove uploaded attachments with a _id and an attachment name

**Syntax**
'''js
db.removeAttachment(documentID, attachmentName, callbackFunction)
'''
**Example**
 Say you want to remove an attachment that was saved with the name 'foo.txt'
'''js
var doc = <some saved document that has an attachment with name *foo.txt*>
var id = doc._id
var attachmentName = 'foo.txt'
...
```

#### <a name="apidoc.element.cradle.Database.prototype.replicate"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>replicate (target, options, callback)](#apidoc.element.cradle.Database.prototype.replicate)
- description and source-code
```javascript
replicate = function (target, options, callback) {
    if (typeof(options) === 'function') {
        callback = options;
        options = {};
    }
    this.connection.replicate(cradle.merge({ source: this.name, target: target }, options), callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.cradle.Database.prototype.save"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>save ()](#apidoc.element.cradle.Database.prototype.save)
- description and source-code
```javascript
save = function () {
    var args = new(Args)(arguments),
        array = args.all.slice(0), doc, id, rev;

    if (Array.isArray(args.first)) {
        doc = args.first;
    } else {
        doc = array.pop();
        id  = array.shift();
        rev = array.shift();
    }
    this._save(id, rev, doc, args.callback);
}
```
- example usage
```shell
...
var db = new(cradle.Connection)().database('starwars');

db.get('vader', function (err, doc) {
    doc.name; // 'Darth Vader'
    assert.equal(doc.force, 'dark');
});

db.save('skywalker', {
    force: 'light',
    name: 'Luke Skywalker'
}, function (err, res) {
    if (err) {
        // Handle error
    } else {
        // Handle success
...
```

#### <a name="apidoc.element.cradle.Database.prototype.saveAttachment"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>saveAttachment (doc, attachment, callback)](#apidoc.element.cradle.Database.prototype.saveAttachment)
- description and source-code
```javascript
saveAttachment = function (doc, attachment, callback) {
    var attachmentName,
        options = {},
        self = this,
        params,
        error,
        rev,
        id;

    if (typeof doc === 'string') {
        id = doc;
    } else {
        id  = doc.id  || doc._id;
        rev = doc.rev || doc._rev;
    }

    if (!id) {
        error = new(TypeError)("Missing document id.");
        if (!callback) {
            throw error;
        }
        return callback(error);
    }

    attachmentName = typeof attachment !== 'string' ? attachment.name : attachment;

    if (!rev && this.cache.has(id)) {
        params = { rev: this.cache.get(id)._rev };
    } else if (rev) {
        params = { rev: rev.replace(/\"/g, '') };
    }

    options.method = 'PUT';
    options.path = '/' + [this.name, querystring.escape(id), attachmentName].join('/');
    options.headers = {
        'Content-Type': attachment['content-type'] ||
            attachment.contentType ||
            attachment['Content-Type'] ||
            'text/plain'
    };

    if (attachment.contentLength) {
        options.headers['Content-Length'] = attachment.contentLength;
    }

    if (attachment.body) {
        options.body = attachment.body;
    }

    if (params) {
        options.path += ('?' + querystring.stringify(params));
    }

    return this.connection.rawRequest(options, function (err, res, body) {
        if (err) {
            return callback(err);
        }

        var result = JSON.parse(body);
        result.headers = res.headers;
        result.headers.status = res.statusCode;

        if (result.headers.status == 201) {
            if (self.cache.has(id)) {
                // FIXME: Is this supposed to be this.cached?
                cached = self.cache.store[id].document;
                cached._rev = result.rev;
                cached._attachments = cached._attachments || {};
                cached._attachments[attachmentName] = { stub: true };
            }

            return callback(null, result);
        }

        callback(result);
    });
}
```
- example usage
```shell
...
-----------
Cradle supports writing, reading, and removing attachments. The read and write operations can be either buffered or streaming
## Writing ##
You can buffer the entire attachment body and send it all at once as a single request. The callback function will fire after the
 attachment upload is complete or an error occurs

**Syntax**
'''js
db.saveAttachment(idData, attachmentData, callbackFunction)
'''
**Example**
Say you want to save a text document as an attachment with the name 'fooAttachment.txt' and the content 'Foo document text'
''' js
var doc = <some existing document>
var id = doc._id
var rev = doc._rev
...
```

#### <a name="apidoc.element.cradle.Database.prototype.temporaryView"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>temporaryView (doc, options, callback)](#apidoc.element.cradle.Database.prototype.temporaryView)
- description and source-code
```javascript
temporaryView = function (doc, options, callback) {
    if (!callback && typeof options === 'function') {
        callback = options;
        options = null;
    }

    if (options && typeof options === 'object') {
        ['key', 'keys', 'startkey', 'endkey'].forEach(function (k) {
            if (k in options) {
                options[k] = JSON.stringify(options[k]);
            }
        });
    }

    return this.query({
        method: 'POST',
        path: '_temp_view',
        query: options,
        body: doc
    }, callback);
}
```
- example usage
```shell
...

These views can later be queried with 'db.view('characters/all')', for example.

Here we create a temporary view. WARNING: do not use this in production as it is
extremely slow (use it to test views).

''' js
db.temporaryView({
    map: function (doc) {
      if (doc.color) emit(doc._id, doc);
    }
  }, function (err, res) {
    if (err) console.log(err);
    console.log(res);
});
...
```

#### <a name="apidoc.element.cradle.Database.prototype.update"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>update (path, id, options, body)](#apidoc.element.cradle.Database.prototype.update)
- description and source-code
```javascript
update = function (path, id, options, body) {
    var args = new(Args)(arguments);
    path = path.split('/');

    if (id) {
      return this.query({
        method: 'PUT',
        path: ['_design', path[0], '_update', path[1], id].map(querystring.escape).join('/'),
        query: options,
        body: body
      }, args.callback);
    }

    return this.query({
        method: 'POST',
        path: ['_design', path[0], '_update', path[1]].map(querystring.escape).join('/'),
        query: options,
        body: body
    }, args.callback);
}
```
- example usage
```shell
...
If 'remove' is called without a revision, and the document was recently fetched from the database, it will attempt to use the cached
 document's revision, providing caching is enabled.

### update handlers ###

Update handlers can be used by calling the 'update()' method, specifying the update handler name, and optionally the document id
, the query object and the document body object. Only the update handler name is a required function parameter. Note that CouchDB
 is able to parse query options only if the URI-encoded length is less than 8197 characters. Use the body parameter for larger objects
.

''' js
  db.update('my_designdoc/update_handler_name', 'luke', undefined, { my_param: false }, function (err, res) {
      // Handle the response, specified by the update handler
  });
'''

Connecting with authentication and SSL
--------------------------------------
...
```

#### <a name="apidoc.element.cradle.Database.prototype.view"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>view (path, options, callback)](#apidoc.element.cradle.Database.prototype.view)
- description and source-code
```javascript
view = function (path, options, callback) {
    if (typeof options === 'function') {
        callback = options;
        options = {};
    }

    path = path.split('/');
    path = ['_design', path[0], '_view', path[1]].map(querystring.escape).join('/');

    return this._getOrPostView(path, options, callback);
}
```
- example usage
```shell
...
''' js
  db.get(['luke', 'vader'], function (err, doc) { ... });
'''

### Querying a view ###

''' js
  db.view('characters/all', function (err, res) {
      res.forEach(function (row) {
          console.log("%s is on the %s side of the force.", row.name, row.force);
      });
  });
'''

You can access the key and value of the response with forEach using two parameters. An optional third parameter will return the
id like this example.
...
```

#### <a name="apidoc.element.cradle.Database.prototype.viewCleanup"></a>[function <span class="apidocSignatureSpan">cradle.Database.prototype.</span>viewCleanup (callback)](#apidoc.element.cradle.Database.prototype.viewCleanup)
- description and source-code
```javascript
viewCleanup = function (callback) {
    this.query({
        method: 'POST',
        path: '/_view_cleanup',
        headers: {
            'Content-Type': 'application/json'
        }
    }, callback);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
