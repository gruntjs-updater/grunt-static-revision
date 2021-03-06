# grunt-static-revision

> Create *.json for the static file asset and revisioning through content hashing.

## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-static-revision --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-static-revision');
```

## The "static-revision" task

### Overview
In your project's Gruntfile, add a section named `static-revision` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  'static-revision': {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    },
  },
});
```

### Options

#### options.src
Type: `String`

The project source directory

#### options.dist
Type: `String`

The project dist directory

#### options.configFile
Type: `String`

Default value:  `static-revision.json`

The configuration file name

#### options.initVersion
Type: `String`

Default value:  `0.0.0`

Initialization version

#### options.maxVersionNumber
Type: `Array`

Default value:  `[10, 100, 100]`

Max version number

### Usage Examples
```js
grunt.initConfig({
    'static-revision': {
        options: {
            src: '<%= config.src %>',
            dist: '<%= config.dist %>'
        },
        src: [
            '<%= config.src %>/js/{,*/}*.js',
            '<%= config.src %>/css/{,*/}*.css'
        ]
    }
});
```

## Release History
2014-11-18 Only build the changed file

2014-08-11 Incremental updating strategy,add `chalk` module for terminal string styling

2014-07-29 Bugfix:build a error key for multilayer directory

2014-07-25 Optimizing log format

2014-07-24 Concat config into one json file & bugfix

2014-07-21 First commit
