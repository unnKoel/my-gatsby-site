## Rendering options

#### How does SSG work?

- First, Gatsby generates all assets and HTML for all SSG pages at build time on a build server (this could be your laptop, any build service, or Gatsby Cloud worker if you use Gatsby Cloud).

- Then, the produced static files are uploaded to the content delivery network (CDN) provider of choice and served to end users. The build server is not needed after the build step and could even be turned off.

> Note: SSG doesn’t mean your site is not dynamic. You can still use JavaScript to communicate with any APIs, add private sections of your site for authorized users via client-side rendering and have any features that single-page applications (SPAs) can have.

#### Deferred Static Generation(DSG)

why: the initial build (the build without the cache), build times may become an issue. That’s where Deferred Static Generation could be beneficial

Unlike SSG, Deferred Static Generation requires you to keep the build server running after the initial build (using the gatsby serve command)

#### SSR 

You can also return HTTP headers along with data to control the page-caching strategy in your CDN.

## Hybrid app pages

Your created pages can make calls to external services and APIs in order to allow more interactive and dynamic behavior. These are sometimes referred to as hybrid app pages because they share a combination of static features that Gatsby creates to help load your site quickly and performantly as well as traditional web app features.

Because Gatsby is capable of generating content at build time as well as making calls to external services at runtime, you can make hybrid pages that take advantage of the benefits of static content as well as dynamic content. 

This combination of static/dynamic is possible through `React hydration`

[example](https://github.com/gatsbyjs/gatsby/tree/master/examples/data-fetching)


## Themes

#### what's the themems?

Gatsby themes are plugins that include a gatsby-config.js file and add pre-configured functionality, data sourcing, and/or UI code to Gatsby sites. You can think of Gatsby themes as separate Gatsby sites that can be put together and allow you to split up a larger Gatsby project

A Gatsby theme is effectively a composable Gatsby config

## Plugin

##### what's the plugin?

Gatsby’s plugin layer includes a wide variety of common website functionality that you can drop in to your website. These include integrations (“source plugins”), responsive images, dropping in analytics libraries, performance enhancements while using CSS libraries, and other website functionality.

Core concepts

- Each Gatsby plugin can be created as an npm package or as a local plugin
- A package.json is required
- Plugins implement the Gatsby APIs for Node, server-side rendering, and the browser
