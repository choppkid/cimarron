Cimarron
========

Cimarron is a zero-configuration http server. It's ideal for development and testing.


Installation
------------

Directly from NPM

    npm install cimarron -g

You can clone it from Github too:

    git clone https://github.com/fcingolani/cimarron.git
    cd cimarron
    npm install . -g
    
Usage
-----

`cd` into a directory, then run `cimarron`; a browser window will be open pointing to your recently started Web Server.

    cd DIRECTORY
    cimarron
    
Configuration
-------------

`cimarron` does not require any configuration to start serving your content. That doesn't mean it's not possible to configure it.

Configuration is done using a `Cimarronfile`, which can be one of two flavours:

1. Static configuration. Using JSON, YAML, or XML.
2. Dynamic configuration. Via JavaScript or CoffeeScript.

###Static Configuration

Create a `Cimarronfile.json` inside the directory you want to serve:

````json
{
    "host": "0.0.0.0",
    "port": 8000,
    "open_browser": true,
    "enable_header": true,
    "enable_logging": true,
    "routes": {
      "/": "."
    }
}
````

In fact those are the default values used when you don't create a `Cimarronfile`!

In case you want to add more routes, just add them to the routes array:

````json
{
    "routes": {
      "/": "./public",
      "/assets/": "./bower_components"
    }
}
````

Remember, it's not required to define every property, forementioned defaults will be used.