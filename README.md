requirejs-stub
==============

Stub loader plugin for leaving out AMD loader plugins during optimization.

`bower install --save-dev requirejs-stub`

In your r.js optimization configuration, use it in place of a loader that you completely want to exclude from optimization:

App configuration:

```
require.config({
    paths: {
        'text': '../bower_components/requirejs-text/text',
        'less': '../bower_components/require-less/less',
        'lessc': '../bower_components/require-less/lessc',
        'normalize': '../bower_components/require-less/normalize',
       ...
    }
    ...
});
```

Build configuration:

```
mainConfigFile: 'src/main.js',
paths: {
    'less': '../bower_components/requirejs-stub/stub', // Disable compilation for requirejs-less
    'almond': '../bower_components/almond/almond'
}
...

```
