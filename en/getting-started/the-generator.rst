The Generator
-------------

Your First Application
``````````````````````

Enter on the just-created directory with:

.. code:: bash

    cd /var/www/graojs-apps

and create your first application with the simple following command:

.. code:: bash

    grao --app my-first-app

Just that? Yes, just that! See what the generator has just created for you:

.. code:: bash

    my-first-app/
        ├── bundles
        │   ├── frontend
        │   │   ├── public
        │   │   │   ├── css
        │   │   │   ├── font
        │   │   │   ├── image
        │   │   │   └── js
        │   │   ├── theme
        │   │   └── view
        │   └── user
        │       ├── public
        │       │   └── js
        │       ├── UserController.js
        │       ├── User.js
        │       ├── UserRoute.js
        │       ├── UserSchema.js
        │       ├── UserValidator.js
        │       └── view
        │           ├── dashboard.jade
        │           ├── form.jade
        │           ├── grid.jade
        │           └── password.jade
        ├── config
        │   ├── locales
        │   └── prod.js
        ├── index.js
        ├── LICENSE
        ├── log
        │   └── grao.log
        ├── node_modules
        │   └── graojs
        ├── package.json
        └── scripts
            ├── graolinks.sh
            ├── grao.sh
            └── stress.sh


This directory treeview is simplified for better understading. Under ``node_modules``
you have all NodeJS_ dependencies for your app.

