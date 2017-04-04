# api documentation for  [wordpress-rest-api (v0.8.0)](https://github.com/kadamwhite/wordpress-rest-api)  [![npm package](https://img.shields.io/npm/v/npmdoc-wordpress-rest-api.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-wordpress-rest-api) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-wordpress-rest-api.svg)](https://travis-ci.org/npmdoc/node-npmdoc-wordpress-rest-api)
#### A client for interacting with the WordPress REST API

[![NPM](https://nodei.co/npm/wordpress-rest-api.png?downloads=true)](https://www.npmjs.com/package/wordpress-rest-api)

[![apidoc](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-wordpress-rest-api_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-wordpress-rest-api/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "K.Adam White",
        "url": "http://www.kadamwhite.com"
    },
    "bugs": {
        "url": "https://github.com/kadamwhite/wordpress-rest-api/issues"
    },
    "dependencies": {
        "bluebird": "^3.4.1",
        "li": "^1.0.1",
        "lodash": "^2.4.2",
        "node.extend": "^1.1.5",
        "parse-link-header": "^0.4.1",
        "qs": "^6.2.0",
        "route-parser": "0.0.4",
        "superagent": "^1.8.3"
    },
    "deprecated": "MODULE RENAMED: This module has been renamed to \"wpapi\"",
    "description": "A client for interacting with the WordPress REST API",
    "devDependencies": {
        "chai": "^3.5.0",
        "chai-as-promised": "^5.3.0",
        "grunt": "^1.0.1",
        "grunt-cli": "^1.2.0",
        "grunt-contrib-jshint": "^1.0.0",
        "grunt-contrib-yuidoc": "^1.0.0",
        "istanbul": "^0.4.4",
        "jscs": "^3.0.5",
        "jscs-stylish": "^0.3.1",
        "jshint": "^2.9.2",
        "jshint-stylish": "^2.2.0",
        "load-grunt-tasks": "^3.5.0",
        "minimist": "^1.2.0",
        "mocha": "^2.5.3",
        "sandboxed-module": "^2.0.3",
        "sinon": "^1.17.4",
        "sinon-chai": "^2.8.0"
    },
    "directories": {},
    "dist": {
        "shasum": "819a0d0999a1253df078b4fc662eb4a22452049f",
        "tarball": "https://registry.npmjs.org/wordpress-rest-api/-/wordpress-rest-api-0.8.0.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "042fa899d0a1ba1d6260b48b2c62758c9d4b9294",
    "homepage": "https://github.com/kadamwhite/wordpress-rest-api",
    "keywords": [
        "api",
        "client",
        "cms",
        "wordpress"
    ],
    "license": "MIT",
    "main": "wp.js",
    "maintainers": [
        {
            "name": "kadamwhite",
            "email": "adam@kadamwhite.com"
        }
    ],
    "name": "wordpress-rest-api",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/kadamwhite/wordpress-rest-api.git"
    },
    "scripts": {
        "docs": "grunt yuidoc",
        "download-endpoint-json": "node ./lib/data/generate-endpoint-response-json",
        "jscs": "jscs Gruntfile.js wp.js lib tests --reporter node_modules/jscs-stylish/jscs-stylish.js",
        "jshint": "jshint --reporter=node_modules/jshint-stylish/index.js Gruntfile.js wp.js lib tests",
        "lint": "npm run jshint && npm run jscs || true",
        "mocha": "_mocha tests --recursive --reporter=nyan",
        "pretest": "npm run lint",
        "test": "istanbul cover _mocha -- tests --recursive --reporter=nyan",
        "test:all": "_mocha tests --recursive --reporter=nyan",
        "test:ci": "npm run lint && istanbul cover _mocha -- tests/unit --recursive --reporter=list",
        "test:integration": "_mocha tests/integration --recursive --reporter=nyan",
        "test:unit": "_mocha tests/unit --recursive --reporter=nyan",
        "watch": "grunt watch"
    },
    "version": "0.8.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module wordpress-rest-api](#apidoc.module.wordpress-rest-api)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.</span>discover ( url )](#apidoc.element.wordpress-rest-api.discover)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.</span>site ( endpoint, routes )](#apidoc.element.wordpress-rest-api.site)
1.  object <span class="apidocSignatureSpan">wordpress-rest-api.</span>autodiscovery
1.  object <span class="apidocSignatureSpan">wordpress-rest-api.</span>endpoint_factories
1.  object <span class="apidocSignatureSpan">wordpress-rest-api.</span>endpoint_request
1.  object <span class="apidocSignatureSpan">wordpress-rest-api.</span>path_part_setter
1.  object <span class="apidocSignatureSpan">wordpress-rest-api.</span>resource_handler_spec
1.  object <span class="apidocSignatureSpan">wordpress-rest-api.</span>route_tree

#### [module wordpress-rest-api.autodiscovery](#apidoc.module.wordpress-rest-api.autodiscovery)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.autodiscovery.</span>getAPIRootFromURL ( url, useGET )](#apidoc.element.wordpress-rest-api.autodiscovery.getAPIRootFromURL)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.autodiscovery.</span>getRootResponseJSON ( apiRootURL )](#apidoc.element.wordpress-rest-api.autodiscovery.getRootResponseJSON)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.autodiscovery.</span>locateAPIRootHeader ( response )](#apidoc.element.wordpress-rest-api.autodiscovery.locateAPIRootHeader)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.autodiscovery.</span>resolveAsPromise ( superagentReq )](#apidoc.element.wordpress-rest-api.autodiscovery.resolveAsPromise)

#### [module wordpress-rest-api.endpoint_factories](#apidoc.module.wordpress-rest-api.endpoint_factories)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.endpoint_factories.</span>generate ( routesByNamespace )](#apidoc.element.wordpress-rest-api.endpoint_factories.generate)

#### [module wordpress-rest-api.endpoint_request](#apidoc.module.wordpress-rest-api.endpoint_request)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.endpoint_request.</span>create ( handlerSpec, resource, namespace )](#apidoc.element.wordpress-rest-api.endpoint_request.create)

#### [module wordpress-rest-api.path_part_setter](#apidoc.module.wordpress-rest-api.path_part_setter)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.path_part_setter.</span>create ( node )](#apidoc.element.wordpress-rest-api.path_part_setter.create)

#### [module wordpress-rest-api.resource_handler_spec](#apidoc.module.wordpress-rest-api.resource_handler_spec)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.resource_handler_spec.</span>create ( routeDefinition, resource )](#apidoc.element.wordpress-rest-api.resource_handler_spec.create)

#### [module wordpress-rest-api.route_tree](#apidoc.module.wordpress-rest-api.route_tree)
1.  [function <span class="apidocSignatureSpan">wordpress-rest-api.route_tree.</span>build ( routes )](#apidoc.element.wordpress-rest-api.route_tree.build)



# <a name="apidoc.module.wordpress-rest-api"></a>[module wordpress-rest-api](#apidoc.module.wordpress-rest-api)

#### <a name="apidoc.element.wordpress-rest-api.discover"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.</span>discover ( url )](#apidoc.element.wordpress-rest-api.discover)
- description and source-code
```javascript
discover = function ( url ) {
	// local placeholder for API root URL
	var endpoint;

	return autodiscovery.getAPIRootFromURL( url )
		.then( autodiscovery.locateAPIRootHeader )
		.then(function( apiRootURL ) {
			// Set the function-scope variable that will be used to instantiate
			// the bound WP instance, then pass the URL on
			endpoint = apiRootURL;
			return apiRootURL;
		})
		.then( autodiscovery.getRootResponseJSON )
		.then(function( apiRootJSON ) {
			// Instantiate & bootstrap with the discovered methods
			return new WP({
				endpoint: endpoint,
				routes: apiRootJSON.routes
			});
		})
		.catch(function( err ) {
			console.error( 'Autodiscovery failed' );
			console.error( err );
			if ( endpoint ) {
				console.warn( 'Endpoint detected, proceeding despite error...' );
				console.warn( 'Binding to ' + endpoint + ' and assuming default routes' );
				return new WP.site( endpoint );
			}
			return null;
		});
}
```
- example usage
```shell
...
'''
The 'wp' object will have endpoint handler methods for every endpoint that ships with the default WordPress REST API plugin.

### Auto-Discovery

It is also possible to leverage the [capability discovery](http://v2.wp-api.org/guide/discovery/) features of the API to automatically
 detect and add setter methods for your custom routes, or routes added by plugins.

To utilize the auto-discovery functionality, call 'WP.discover()' with a URL within a WordPress REST API-enabled site:
'''js
var apiPromise = WP.discover( 'http://my-site.com' );
'''
If auto-discovery succeeds this method returns a promise that will be resolved with a WP client instance object configured specifically
 for your site. You can use that promise as the queue that your client instance is ready, then use the client normally within the
 '.then' callback.

**Custom Routes** will be detected by this process, and registered on the client. To prevent name conflicts, only routes in the '
wp/v2' namespace will be bound to your instance object itself. The rest can be accessed through the '.namespace' method on the WP
 instance, as demonstrated below.
...
```

#### <a name="apidoc.element.wordpress-rest-api.site"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.</span>site ( endpoint, routes )](#apidoc.element.wordpress-rest-api.site)
- description and source-code
```javascript
site = function ( endpoint, routes ) {
	return new WP({
		endpoint: endpoint,
		routes: routes
	});
}
```
- example usage
```shell
...
/**
* Convenience method for making a new WP instance
*
* @example
* These are equivalent:
*
*     var wp = new WP({ endpoint: 'http://my.blog.url/wp-json' });
*     var wp = WP.site( 'http://my.blog.url/wp-json' );
*
* 'WP.site' can take an optional API root response JSON object to use when
* bootstrapping the client's endpoint handler methods: if no second parameter
* is provided, the client instance is assumed to be using the default API
* with no additional plugins and is initialized with handlers for only those
* default API routes.
*
...
```



# <a name="apidoc.module.wordpress-rest-api.autodiscovery"></a>[module wordpress-rest-api.autodiscovery](#apidoc.module.wordpress-rest-api.autodiscovery)

#### <a name="apidoc.element.wordpress-rest-api.autodiscovery.getAPIRootFromURL"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.autodiscovery.</span>getAPIRootFromURL ( url, useGET )](#apidoc.element.wordpress-rest-api.autodiscovery.getAPIRootFromURL)
- description and source-code
```javascript
function getAPIRootFromURL( url, useGET ) {

	// If useGET is specified and truthy, .get the url; otherwise use .head
	// because we only care about the HTTP headers, not the response body.
	var request = useGET ? agent.get( url ) : agent.head( url );

	return resolveAsPromise( request )
		.catch(function( err ) {
			// If this wasn't already a GET request, then on the hypothesis that an
			// error arises from an unaccepted HEAD request, try again using GET
			if ( ! useGET ) {
				return getAPIRootFromURL( url, true );
			}

			// Otherwise re-throw the error
			throw err;
		});
}
```
- example usage
```shell
...
 * to the deduced endpoint, or rejected if an endpoint is not found or the
 * library is unable to parse the provided endpoint.
 */
WP.discover = function( url ) {
	// local placeholder for API root URL
	var endpoint;

	return autodiscovery.getAPIRootFromURL( url )
		.then( autodiscovery.locateAPIRootHeader )
		.then(function( apiRootURL ) {
			// Set the function-scope variable that will be used to instantiate
			// the bound WP instance, then pass the URL on
			endpoint = apiRootURL;
			return apiRootURL;
		})
...
```

#### <a name="apidoc.element.wordpress-rest-api.autodiscovery.getRootResponseJSON"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.autodiscovery.</span>getRootResponseJSON ( apiRootURL )](#apidoc.element.wordpress-rest-api.autodiscovery.getRootResponseJSON)
- description and source-code
```javascript
function getRootResponseJSON( apiRootURL ) {
	return resolveAsPromise( agent.get( apiRootURL ).set( 'Accept', 'application/json' ) )
		.then(function( response ) {
			return response.body;
		});
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wordpress-rest-api.autodiscovery.locateAPIRootHeader"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.autodiscovery.</span>locateAPIRootHeader ( response )](#apidoc.element.wordpress-rest-api.autodiscovery.locateAPIRootHeader)
- description and source-code
```javascript
function locateAPIRootHeader( response ) {
	var rel = 'https://api.w.org/';

	// Extract & parse the response link headers
	var headers = parseLinkHeader( response.headers.link );
	var apiHeader = headers && headers[ rel ];

	if ( apiHeader && apiHeader.url ) {
		return apiHeader.url;
	}

	throw new Error( 'No header link found with rel="https://api.w.org/"' );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wordpress-rest-api.autodiscovery.resolveAsPromise"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.autodiscovery.</span>resolveAsPromise ( superagentReq )](#apidoc.element.wordpress-rest-api.autodiscovery.resolveAsPromise)
- description and source-code
```javascript
function resolveAsPromise( superagentReq ) {
	return new Promise(function( resolve, reject ) {
		superagentReq.end(function( err, res ) {
			if ( err ) {
				// If err.response is present, the request succeeded but we got an
				// error from the server: surface & return that error
				if ( err.response && err.response.error ) {
					return reject( err.response.error );
				}
				// If err.response is not present, the request could not connect
				return reject( err );
			}
			resolve( res );
		});
	});
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.wordpress-rest-api.endpoint_factories"></a>[module wordpress-rest-api.endpoint_factories](#apidoc.module.wordpress-rest-api.endpoint_factories)

#### <a name="apidoc.element.wordpress-rest-api.endpoint_factories.generate"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.endpoint_factories.</span>generate ( routesByNamespace )](#apidoc.element.wordpress-rest-api.endpoint_factories.generate)
- description and source-code
```javascript
function generateEndpointFactories( routesByNamespace ) {

	return Object.keys( routesByNamespace ).reduce(function( namespaces, namespace ) {
		var routeDefinitions = routesByNamespace[ namespace ];

		// Create
		namespaces[ namespace ] = Object.keys( routeDefinitions ).reduce(function( handlers, resource ) {

			var handlerSpec = createResourceHandlerSpec( routeDefinitions[ resource ], resource );

			var EndpointRequest = createEndpointRequest( handlerSpec, resource, namespace );

			// "handler" object is now fully prepared; create the factory method that
			// will instantiate and return a handler instance
			handlers[ resource ] = function( options ) {
				options = options || {};
				options = extend( options, this._options );
				return new EndpointRequest( options );
			};

			// Expose the constructor as a property on the factory function, so that
			// auto-generated endpoint request constructors may be further customized
			// when needed
			handlers[ resource ].Ctor = EndpointRequest;

			return handlers;
		}, {} );

		return namespaces;
	}, {} );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.wordpress-rest-api.endpoint_request"></a>[module wordpress-rest-api.endpoint_request](#apidoc.module.wordpress-rest-api.endpoint_request)

#### <a name="apidoc.element.wordpress-rest-api.endpoint_request.create"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.endpoint_request.</span>create ( handlerSpec, resource, namespace )](#apidoc.element.wordpress-rest-api.endpoint_request.create)
- description and source-code
```javascript
function createEndpointRequest( handlerSpec, resource, namespace ) {

	// Create the constructor function for this endpoint
	function EndpointRequest( options ) {
		WPRequest.call( this, options );

		<span class="apidocCodeCommentSpan">/**
		 * Semi-private instance property specifying the available URL path options
		 * for this endpoint request handler, keyed by ascending whole numbers.
		 *
		 * @property _levels
		 * @type {object}
		 * @private
		 */
</span>		this._levels = handlerSpec._levels;

		// Configure handler for this endpoint's root URL path & set namespace
		this
			.setPathPart( 0, resource )
			.namespace( namespace );
	}

	inherit( EndpointRequest, WPRequest );

	// Mix in all available shortcut methods for GET request query parameters that
	// are valid within this endpoint tree
	if ( typeof handlerSpec._getArgs === 'object' ) {
		Object.keys( handlerSpec._getArgs ).forEach(function( supportedQueryParam ) {
			var mixinsForParam = mixins[ supportedQueryParam ];

			// Only proceed if there is a mixin available AND the specified mixins will
			// not overwrite any previously-set prototype method
			if ( mixinsForParam ) {
				Object.keys( mixinsForParam ).forEach(function( methodName ) {
					if ( ! EndpointRequest.prototype[ methodName ] ) {
						EndpointRequest.prototype[ methodName ] = mixinsForParam[ methodName ];
					}
				});
			}
		});
	}

	Object.keys( handlerSpec._setters ).forEach(function( setterFnName ) {
		if ( EndpointRequest.prototype[ setterFnName ] ) {
			console.warn( 'Warning: method .' + setterFnName + '() is already defined!' );
			console.warn( 'Cannot overwrite .' + resource + '().' + setterFnName + '() method' );
		} else {
			EndpointRequest.prototype[ setterFnName ] = handlerSpec._setters[ setterFnName ];
		}
	});

	return EndpointRequest;
}
```
- example usage
```shell
...
// my-endpoint-response.json file, with no need to wait for a Promise.

site.namespace( 'myplugin/v1' ).authors()...
'''

To create a slimmed JSON file dedicated to this particular purpose, see the Node script [lib/data/generate-endpoint-request.js](
lib/data/generate-endpoint-request.js), which will let you download and save an endpoint response to your local project.

In addition to retrieving the specified resource with '.get()', you can also '.create()', '.update()' and '.delete()' resources:

### Creating Posts

To create posts, use the '.create()' method on a query to POST (the HTTP verb for "create") a data object to the server:

'''js
// You must authenticate to be able to POST (create) a post
...
```



# <a name="apidoc.module.wordpress-rest-api.path_part_setter"></a>[module wordpress-rest-api.path_part_setter](#apidoc.module.wordpress-rest-api.path_part_setter)

#### <a name="apidoc.element.wordpress-rest-api.path_part_setter.create"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.path_part_setter.</span>create ( node )](#apidoc.element.wordpress-rest-api.path_part_setter.create)
- description and source-code
```javascript
function createPathPartSetter( node ) {
	// Local references to 'node' properties used by returned functions
	var nodeLevel = node.level;
	var nodeName = node.names[ 0 ];
	var supportedMethods = node.methods || [];
	var dynamicChildren = node.children ? Object.keys( node.children )
		.map(function( key ) {
			return node.children[ key ];
		})
		.filter(function( childNode ) {
			return childNode.namedGroup === true;
		}) : [];
	var dynamicChild = dynamicChildren.length === 1 && dynamicChildren[ 0 ];
	var dynamicChildLevel = dynamicChild && dynamicChild.level;

	if ( node.namedGroup ) {
		<span class="apidocCodeCommentSpan">/**
		 * Set a dymanic (named-group) path part of a query URL.
		 *
		 * @example
		 *
		 *     // id() is a dynamic path part setter:
		 *     wp.posts().id( 7 ); // Get posts/7
		 *
		 * @chainable
		 * @param  {String|Number} val The path part value to set
		 * @return {Object} The handler instance (for chaining)
		 */
</span>		return function( val ) {
			/* jshint validthis:true */
			this.setPathPart( nodeLevel, val );
			if ( supportedMethods.length ) {
				this._supportedMethods = supportedMethods;
			}
			return this;
		};
	} else {
		/**
		 * Set a non-dymanic (non-named-group) path part of a query URL, and
		 * set the value of a subresource if an input value is provided and
		 * exactly one named-group child node exists.
		 *
		 * @example
		 *
		 *     // revisions() is a non-dynamic path part setter:
		 *     wp.posts().id( 4 ).revisions();       // Get posts/4/revisions
		 *     wp.posts().id( 4 ).revisions( 1372 ); // Get posts/4/revisions/1372
		 *
		 * @chainable
		 * @param  {String|Number} [val] The path part value to set (if provided)
		 *                               for a subresource within this resource
		 * @return {Object} The handler instance (for chaining)
		 */
		return function( val ) {
			/* jshint validthis:true */
			// If the path part is not a namedGroup, it should have exactly one
			// entry in the names array: use that as the value for this setter,
			// as it will usually correspond to a collection endpoint.
			this.setPathPart( nodeLevel, nodeName );

			// If this node has exactly one dynamic child, this method may act as
			// a setter for that child node. 'dynamicChildLevel' will be falsy if the
			// node does not have a child or has multiple children.
			if ( typeof val !== 'undefined' && dynamicChildLevel ) {
				this.setPathPart( dynamicChildLevel, val );
			}
			return this;
		};
	}
}
```
- example usage
```shell
...
// my-endpoint-response.json file, with no need to wait for a Promise.

site.namespace( 'myplugin/v1' ).authors()...
'''

To create a slimmed JSON file dedicated to this particular purpose, see the Node script [lib/data/generate-endpoint-request.js](
lib/data/generate-endpoint-request.js), which will let you download and save an endpoint response to your local project.

In addition to retrieving the specified resource with '.get()', you can also '.create()', '.update()' and '.delete()' resources:

### Creating Posts

To create posts, use the '.create()' method on a query to POST (the HTTP verb for "create") a data object to the server:

'''js
// You must authenticate to be able to POST (create) a post
...
```



# <a name="apidoc.module.wordpress-rest-api.resource_handler_spec"></a>[module wordpress-rest-api.resource_handler_spec](#apidoc.module.wordpress-rest-api.resource_handler_spec)

#### <a name="apidoc.element.wordpress-rest-api.resource_handler_spec.create"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.resource_handler_spec.</span>create ( routeDefinition, resource )](#apidoc.element.wordpress-rest-api.resource_handler_spec.create)
- description and source-code
```javascript
function createNodeHandlerSpec( routeDefinition, resource ) {

	var handler = {
		// A "path" is an ordered (by key) set of values composed into the final URL
		_path: {
			'0': resource
		},

		// A "level" is a level-keyed object representing the valid options for
		// one level of the resource URL
		_levels: {},

		// Objects that hold methods and properties which will be copied to
		// instances of this endpoint's handler
		_setters: {},

		// Arguments (query parameters) that may be set in GET requests to endpoints
		// nested within this resource route tree, used to determine the mixins to
		// add to the request handler
		_getArgs: routeDefinition._getArgs
	};

	// Walk the tree
	Object.keys( routeDefinition ).forEach(function( routeDefProp ) {
		if ( routeDefProp !== '_getArgs' ) {
			extractSetterFromNode( handler, routeDefinition[ routeDefProp ] );
		}
	});

	return handler;
}
```
- example usage
```shell
...
// my-endpoint-response.json file, with no need to wait for a Promise.

site.namespace( 'myplugin/v1' ).authors()...
'''

To create a slimmed JSON file dedicated to this particular purpose, see the Node script [lib/data/generate-endpoint-request.js](
lib/data/generate-endpoint-request.js), which will let you download and save an endpoint response to your local project.

In addition to retrieving the specified resource with '.get()', you can also '.create()', '.update()' and '.delete()' resources:

### Creating Posts

To create posts, use the '.create()' method on a query to POST (the HTTP verb for "create") a data object to the server:

'''js
// You must authenticate to be able to POST (create) a post
...
```



# <a name="apidoc.module.wordpress-rest-api.route_tree"></a>[module wordpress-rest-api.route_tree](#apidoc.module.wordpress-rest-api.route_tree)

#### <a name="apidoc.element.wordpress-rest-api.route_tree.build"></a>[function <span class="apidocSignatureSpan">wordpress-rest-api.route_tree.</span>build ( routes )](#apidoc.element.wordpress-rest-api.route_tree.build)
- description and source-code
```javascript
function buildRouteTree( routes ) {
	return Object.keys( routes ).reduce( reduceRouteTree.bind( null, routes ), {} );
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
