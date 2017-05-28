
# Node JS Style Guide

#### Style Guide

All JavaScript code should follow the [Standard JS](https://github.com/feross/standard) style guide.

Any Node JS components developed should include a step to lint the source files as part of the `package.json` test script definition, before any unit tests are run:

E.g.

``` package.json
"scripts": {
  "test": "node_modules/.bin/standard"
}
```

Standard should also be enabled for your development IDE.

A list of plugins for all common editors can be found here: [Text Editor Plugins](https://github.com/feross/standard#text-editor-plugins)


#### Conventions

For conventions and other recommendations we will use the [AirBnB public standards](https://github.com/airbnb/javascript) where they do not conflict with StandardJS.
