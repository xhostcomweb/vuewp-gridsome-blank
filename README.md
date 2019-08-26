# Vue JS Wordpress starter for Gridsome

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/gridsome/gridsome-starter-wordpress)

Total blank version (almost, just header and footer to change/swap out)


## Install & Todo
Install Gridsome first, then clone repo and run yarn.

Uses no CSS custom nav, but can swap out nav, header, footer for your own.
Just change nav and page templates to yours, header and footer in components folder.
4 pages made, Home, About, Blog/News and Contact
See main.js for imports, put extra plugins in index.js.  DELETE index.html if not required but that currently pulls in Font Awesome 4.7 (usually for cdns/font awsome etc). Some extra assets in images and img folder, not used yet.

## Guide

Add your WordPress URL to the plugin options. Already done here, change to required field in gridsome.config and netlify.toml

```js
// gridsome.config.js

module.exports = {
  plugins: [
    {
      use: '@gridsome/source-wordpress',
      options: {
        baseUrl: 'YOUR_WEBSITE_URL', // required
        typeName: 'WordPress', // GraphQL schema name (Optional)
        routes: {
          post: '/:year/:month/:day/:slug', //adds route for "post" post type (Optional)
          post_tag: '/tag/:slug' // adds route for "post_tag" post type (Optional)
        }
      }
    }
  ]
}

```

See all [options](https://gridsome.org/plugins/@gridsome/source-wordpress).

## Included templates

This starter includes basic templates for categories, tags and posts, Home, About and News page.
