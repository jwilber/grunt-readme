## Getting Started
_If you haven't used [grunt][] before, be sure to check out the [Getting Started][] guide._

From the same directory as your project's [Gruntfile][Getting Started] and [package.json][], install this plugin with the following command:

```bash
npm install {%= name %} --save-dev
```

Once that's done, add this line to your project's Gruntfile:

```js
grunt.loadNpmTasks('{%= name %}');
```

If the plugin has been installed correctly, running `grunt --help` at the command line should list the newly-installed plugin's task or tasks. In addition, the plugin should be listed in package.json as a `devDependency`, which ensures that it will be installed whenever the `npm install` command is run.

[grunt]: http://gruntjs.com/
[Getting Started]: https://github.com/gruntjs/grunt/blob/devel/docs/getting_started.md
[package.json]: https://npmjs.org/doc/json.html


In your project's Gruntfile, load the plugin with `grunt.loadNpmTasks('{%= name %}');` outside of `grunt.initConfig()`:

```js
grunt.initConfig({
  grunt.initConfig({
    // tasks
  });

  grunt.loadNpmTasks('grunt-readme');
  // Build the README.
  grunt.registerTask('default', ['readme']);
});
```

Optionally, if you need to change the plugin's defaults, In your project's Gruntfile, add a section named `{%= _.shortname(name) %}` to the data object passed into `grunt.initConfig()`:

```js
grunt.initConfig({

  // The "readme" task
  readme: {
    options: {
      sep: '\n',
      resolve: 'readme-template',
      prefixes: ["helper", "util", "assemble", "mixin"],
      metadata: 'test/fixtures/metadata.json',
      templates: ['tasks/templates/']
    }
  }
});
```