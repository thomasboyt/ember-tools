Ember Tools
-----------

![demo](http://i.imgur.com/bRJobg5.gif)

## Installation

`npm install ember-tools`

## What's in the bag?

### Features

- prescribed file organization for sanity
- template precompilation for performance
- single file application build for convenience
- generators for faster application development
- commonjs (node) style modules for js community <3 and isolated testing

### Commands

- `ember create [appDir]`
- `ember build`
- `ember-generate [options] [resource]`
- `ember-precompile --directory [directory] --file [file]`

### Current Library Versions

- ember 1.0.0.pre4
- ember-data rev 11
- handlebars 1.0.rc.2
- jQuery 1.9.0

## `ember create [dir]`

Creates the directory at [dir] and shoves a boilerplate ember app into
it. Also creates an `.ember` file in the current directory so `ember
build` knows what directory to build.

**IMPORTANT**: Your app must be a sub-directory of the app you create it
from. I anticipate more information to be stored in the `.ember` file
like CoffeeScript and AMD support, etc.

_Example:_

```sh
ember create client
```

## `ember build`

Builds your app, handing you a fresh-from-the-oven `application.js` with
everything inside.

_Example:_

```sh
ember build
```

## `ember generate [options] [resource]`

Generates boilerplate application modules.

Examples:


| options | object name | file |
| --------|-------------|------|
| `--model, -m burrito` | `Burrito` | `models/burrito.js` |
| `--view, -v burrito` | `BurritoView` | `views/burrito.js` |
| `--controller, -c post/comments` | `PostCommentsController` | `controllers/post/comments.js` |
| `--template, -t post/comments` | n/a | `templates/post/comments.handlebars` |
| `--route, -r taco_cart` | `TacoCartRoute` | `routes/taco_cart.js` |
| `-mvcrt tacos` | `Taco` <br>`TacosView` <br>`TacosController` <br>`TacosRoute` | `models/taco.js` <br>`views/tacos_view` <br>`controllers/tacos_controller.js` <br>`routes/taco_route.js` <br>`templates/tacos.handlebars`|

_Notes:_

- Models will always be singular.
- Sub-directories will be created for you if they don't exist.
- Files will be overwritten **without warning**.

## `ember precompile --directory [dir] --file [file]`

Precompiles templates found in `dir` into `file`.

_Examples_

`ember-precompile --directory app/templates --file app/templates.js`
`ember-precompile -d app/templates -f app/templates.js`


## Roadmap

- create CONTRIBUTING file
- moar tests
- travis-ci
- warn before overwriting a file
- scaffolding (functional CRUD in one command)
- baked in testing
- generated tests
- support for custom application namespace (instead of just `App`)
- consolidate all bin script usage into `ember` (get rid of ember-generate, etc.)
- emblem.js templates
- coffeescript generators
- AMD generators/build (maybe)
- coffeescript + AMD generators! (maybe-er)
- ES6 module generators/build EVEN THOUGH E'RBODY UP IN THEIR GRILL (maybeist)
- refactor some of the ugly parts of the code

## License and Copyright

[MIT Style License](http://opensource.org/licenses/MIT)

Copyright &copy; 2013 [Ryan Florence](http://ryanflorence.com)

## Contributing

Run tests with

`mocha test`
