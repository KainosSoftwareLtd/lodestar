
# Node JS Style Guide

## Style Guide

All JavaScript code should follow the [Standard JS](https://github.com/feross/standard) style guide.

Standard is very opinionated and you may find some of the opinions disturbing - we know we did. No semi-colons? What is this madness? 

But trust us (you really can) - Standard will lead you to JavaScript code that is very clean and highly consistent.

Any Node JS components developed should include a step to lint the source files as part of the `package.json` test script definition, before any unit tests are run:

E.g.

``` package.json
"scripts": {
  "test": "node_modules/.bin/standard"
}
```

Standard should also be enabled for your development IDE.

A list of plugins for all common editors can be found here: [Text Editor Plugins](https://github.com/feross/standard#text-editor-plugins)

## Examples

Kainos have used the Standard style guidelines on several projects - most notably Assisted Prison Visits for HMPPS and Home Office.

APVS is open source, so it is recommended you check out one of the [Node JS repositories](https://github.com/ministryofjustice/apvs-external-web) to see an example of a project using this style guide in practice.

## Conventions

For conventions and other recommendations we will use the [AirBnB public standards](https://github.com/airbnb/javascript) where they do not conflict with StandardJS.
