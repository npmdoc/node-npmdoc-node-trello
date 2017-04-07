# api documentation for  [node-trello (v1.1.2)](https://github.com/adunkman/node-trello)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-trello.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-trello) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-trello.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-trello)
#### Node wrapper for Trello's HTTP API.

[![NPM](https://nodei.co/npm/node-trello.png?downloads=true)](https://www.npmjs.com/package/node-trello)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-trello/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-trello_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-trello/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-trello/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-trello/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Luca Matteis",
        "email": "lmatteis@gmail.com"
    },
    "bugs": {
        "url": "http://github.com/adunkman/node-trello/issues"
    },
    "config": {
        "travis-cov": {
            "threshold": 75
        },
        "blanket": {
            "pattern": "//^((?!/node_modules/)(?!/test/).)*$/ig"
        }
    },
    "contributors": [
        {
            "name": "Andrew Dunkman",
            "email": "andrew@dunkman.org"
        }
    ],
    "dependencies": {
        "oauth": "0.9.7",
        "request": "2.51.0"
    },
    "description": "Node wrapper for Trello's HTTP API.",
    "devDependencies": {
        "blanket": "1.1.6",
        "mocha": "2.1.0",
        "should": "5.1.0",
        "travis-cov": "0.2.5"
    },
    "directories": {},
    "dist": {
        "shasum": "7276155d69d9c9f493b2d6119704d84e37171187",
        "tarball": "https://registry.npmjs.org/node-trello/-/node-trello-1.1.2.tgz"
    },
    "engines": [
        "node >= 0.6.17"
    ],
    "gitHead": "fe60c6426bdd858f1019f115ca523cf595350891",
    "homepage": "https://github.com/adunkman/node-trello",
    "keywords": [
        "http",
        "trello",
        "api",
        "web-service"
    ],
    "main": "./index",
    "maintainers": [
        {
            "name": "lmatteis",
            "email": "lmatteis@gmail.com"
        },
        {
            "name": "adunkman",
            "email": "andrew@dunkman.org"
        }
    ],
    "name": "node-trello",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/adunkman/node-trello.git"
    },
    "scripts": {
        "test": "mocha --reporter spec && ./node_modules/.bin/mocha --require blanket --reporter travis-cov",
        "test-cov-report": "mocha --require blanket --reporter html-cov > coverage.html && open coverage.html"
    },
    "version": "1.1.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-trello](#apidoc.module.node-trello)
1.  [function <span class="apidocSignatureSpan">node-trello.</span>OAuth (key, secret, loginCallback, appName)](#apidoc.element.node-trello.OAuth)
1.  object <span class="apidocSignatureSpan">node-trello.</span>OAuth.prototype

#### [module node-trello.OAuth](#apidoc.module.node-trello.OAuth)
1.  [function <span class="apidocSignatureSpan">node-trello.</span>OAuth (key, secret, loginCallback, appName)](#apidoc.element.node-trello.OAuth.OAuth)

#### [module node-trello.OAuth.prototype](#apidoc.module.node-trello.OAuth.prototype)
1.  [function <span class="apidocSignatureSpan">node-trello.OAuth.prototype.</span>getAccessToken (bag, callback)](#apidoc.element.node-trello.OAuth.prototype.getAccessToken)
1.  [function <span class="apidocSignatureSpan">node-trello.OAuth.prototype.</span>getRequestToken (callback)](#apidoc.element.node-trello.OAuth.prototype.getRequestToken)



# <a name="apidoc.module.node-trello"></a>[module node-trello](#apidoc.module.node-trello)

#### <a name="apidoc.element.node-trello.OAuth"></a>[function <span class="apidocSignatureSpan">node-trello.</span>OAuth (key, secret, loginCallback, appName)](#apidoc.element.node-trello.OAuth)
- description and source-code
```javascript
OAuth = function (key, secret, loginCallback, appName) {
  this.oauth = new OAuth(requestUrl, accessUrl, key, secret, "1.0", loginCallback, "HMAC-SHA1");
  this.appName = appName;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-trello.OAuth"></a>[module node-trello.OAuth](#apidoc.module.node-trello.OAuth)

#### <a name="apidoc.element.node-trello.OAuth.OAuth"></a>[function <span class="apidocSignatureSpan">node-trello.</span>OAuth (key, secret, loginCallback, appName)](#apidoc.element.node-trello.OAuth.OAuth)
- description and source-code
```javascript
OAuth = function (key, secret, loginCallback, appName) {
  this.oauth = new OAuth(requestUrl, accessUrl, key, secret, "1.0", loginCallback, "HMAC-SHA1");
  this.appName = appName;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-trello.OAuth.prototype"></a>[module node-trello.OAuth.prototype](#apidoc.module.node-trello.OAuth.prototype)

#### <a name="apidoc.element.node-trello.OAuth.prototype.getAccessToken"></a>[function <span class="apidocSignatureSpan">node-trello.OAuth.prototype.</span>getAccessToken (bag, callback)](#apidoc.element.node-trello.OAuth.prototype.getAccessToken)
- description and source-code
```javascript
getAccessToken = function (bag, callback) {
  var token = bag.oauth_token;
  var tokenSecret = bag.oauth_token_secret;
  var verifier = bag.oauth_verifier;

  this.oauth.getOAuthAccessToken(token, tokenSecret, verifier, function (error, accessToken, accessTokenSecret, results) {
    if (error) {
      return callback(error, null);
    }

    callback(null, {
      oauth_token: token,
      oauth_token_secret: tokenSecret,
      oauth_access_token: accessToken,
      oauth_access_token_secret: accessTokenSecret
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-trello.OAuth.prototype.getRequestToken"></a>[function <span class="apidocSignatureSpan">node-trello.OAuth.prototype.</span>getRequestToken (callback)](#apidoc.element.node-trello.OAuth.prototype.getRequestToken)
- description and source-code
```javascript
getRequestToken = function (callback) {
  var appName = this.appName;

  this.oauth.getOAuthRequestToken(function (error, token, tokenSecret, results) {
    if (error) {
      return callback(error, null);
    }

    callback(null, {
      oauth_token: token,
      oauth_token_secret: tokenSecret,
      redirect: authorizeUrl + ("?oauth_token=" + token + "&name=" + appName)
    });
  });
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
