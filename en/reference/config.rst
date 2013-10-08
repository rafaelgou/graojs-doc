Config Reference
================

.. include:: ../links.rst


The File
--------

Mastering the content of ``your_grao_app\config.js``. Each part of it is 
detail below its code.

.. code:: javascript

    var fs = require('fs'),
        path = require('path'),
        rootPath = path.normalize(__dirname) + '/..',
        charset = 'utf-8',
        packageJson = JSON.parse(fs.readFileSync(rootPath+'/package.json', charset));

    module.exports = exports = {
        packageJson: packageJson,
        ports : [ 8015, 8016, 8017, 8018, 8019, 8020, 8021, 8022 ],
        charset: charset,
        db: 'mongodb://localhost/grao',
        rootPath: rootPath,
        bundles: rootPath + '/bundles',
        vendor: rootPath + '/vendor',
        locales: rootPath + '/config/locales',
        name : packageJson.description,
        log : {
            transport : {
                console : {
                    colorize: true,
                    json : false,
                    timestamp : true,
                    level : 'info'
                },
                file : {
                    filename : rootPath + '/log/grao.log',
                    json : false,
                    level : 'error'
                }
            },
            exception : {
                console : {
                    colorize: true,
                    json : false,
                    timestamp : true,
                    level : 'info'
                },
                file : {
                    filename : rootPath + '/log/grao.log',
                    json : false,
                    level : 'error'
                }
            },
        },
        facebook : {
            clientID : "APP_ID",
            clientSecret : "APP_SECRET",
            callbackURL : "http://localhost:3000/auth/facebook/callback"
        },
        twitter : {
            clientID : "CONSUMER_KEY",
            clientSecret : "CONSUMER_SECRET",
            callbackURL : "http://localhost:3000/auth/twitter/callback"
        },
        github : {
            clientID : 'APP_ID',
            clientSecret : 'APP_SECRET',
            callbackURL : 'http://localhost:3000/auth/github/callback'
        },
        google : {
            clientID : "APP_ID",
            clientSecret : "APP_SECRET",
            callbackURL : "http://localhost:3000/auth/google/callback"
        }
    }

Config Details
--------------

Header
``````

.. code:: javascript

    var fs = require('fs'),
        path = require('path'),
        rootPath = path.normalize(__dirname) + '/..',
        charset = 'utf-8',
        packageJson = JSON.parse(fs.readFileSync(rootPath+'/package.json', charset));

This first part it's not suposed to be changed. Main requires (``fs`` and ``path``),
``rootPath``, ``charset`` and ``packageJson`` variables are defined and that's the way they must be.

module.export
`````````````

That's the main part of configuration. It's a JSON_ Object, so it must be parsed accordingly.

packageJson
'''''''''''
Default: ``packageJson``

Global variable defined on the top of ``config.js`` file that merges the
``package.json`` file content into our global configuration, so you can centralize
some info about the application, such as:

* Name (``packageJson.name``)
* Description (``packageJson.description``)
* Version (``packageJson.version``)
* Author (``packageJson.author``)

See ``YOUR_GRAO_APP_ROOT/package.json`` for more info.

ports
'''''
Default: ``[8015, 8016, 8017, 8018, 8019, 8020, 8021, 8022]``

An array cPorts to start the NodeJS_ service. By default 8 ports are defined, from
8015 up to 8022. Use as many as ports as you to scale your application.

charset
'''''''
Default: ``charset``

Global variable defined on the top of ``config.js``, default: ``utf-8``.

db
''
TODO

rootPath
''''''''
TODO

bundles
''''''''
TODO

vendor
''''''
TODO

locales
'''''''
TODO

name
''''
TODO

log
''''
TODO

facebook
''''''''
TODO

twitter
'''''''
TODO

github
''''''
TODO

google

