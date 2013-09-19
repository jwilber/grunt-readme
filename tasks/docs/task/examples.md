# Usage examples

Simple example of using data files in both `.json` and `.yml` format to build Handlebars templates.

```javascript
assemble: {
  options: {
    data: 'src/data/**/*.{json,yml}'
  },
  docs: {
    files: {
      'dist/': ['src/templates/**/*.hbs']
    }
  }
}
```

## Using multiple targets

```js
assemble: {
  options: {
    assets: 'assets',
    layoutdir: 'docs/layouts'
    partials: ['docs/includes/**/*.hbs'],
    data: ['docs/data/**/*.{json,yml}']
  },
  site: {
    options: {
      layout: 'default.hbs'
    },
    src: ['templates/site/*.hbs'],
    dest: './'
  },
  blog: {
    options: {
      layout: 'blog-layout.hbs'
    },
    src: ['templates/blog/*.hbs'],
    dest: 'articles/'
  },
  docs: {
    options: {
      layout: 'docs-layout.hbs'
    },
    src: ['templates/docs/*.hbs'],
    dest: 'docs/'
  }
},
```

Visit [Assemble's documentation](http://assemble.io) for many more examples and pointers on getting started.


## foo

```js
assemble: {
  development: {
    options: {
      assets: ["dev/assets"]
    },
    files: {
      "dev/": "templates/*.hbs"
    }
  },
  production: {
    options: {
      paths: ["dist/assets"]
    },
    files: {
      "dist/": "templates/*.hbs"
    }
  }
}
```

## Bar

This:

```js
grunt.initConfig({
  assemble: {
    options: {
      engine: 'swig',
      swig: {
        varControls: ["<%=", "%>"]
      }
    },
    site: {
      files: {
        '_gh_pages/': ['src/templates/**/*.swig']
      }
    }
  }
});
```

Results in this:

```js
grunt.initConfig({
  assemble: {
    options: {
      engine: 'swig',
      swig: {
        varControls: ["<%=", "%>"]
      }
    },
    site: {
      files: {
        '_gh_pages/': ['src/templates/**/*.swig']
      }
    }
  }
});
```

## baz

```js
grunt.initConfig({
  assemble: {
    options: {
      engine: 'swig',
      swig: {
        varControls: ["<%=", "%>"]
      }
    },
    site: {
      files: {
        '_gh_pages/': ['src/templates/**/*.swig']
      }
    }
  }
});
```

