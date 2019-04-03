# gatsby-plugin-scss-typescript &middot; [![NPM Version](https://img.shields.io/npm/v/gatsby-plugin-scss-typescript.svg)](https://www.npmjs.com/package/gatsby-plugin-scss-typescript) [![downloads](https://img.shields.io/npm/dt/gatsby-plugin-scss-typescript.svg)](https://www.npmjs.com/package/gatsby-plugin-scss-typescript) ![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg) [![CircleCI](https://circleci.com/gh/Debens/gatsby-plugin-scss-typescript.svg?style=shield&circle-token=2d506be7c3ec07e440056881ce5c376f7618f214)](https://circleci.com/gh/Debens/gatsby-plugin-scss-typescript)

Includes Gatsby V2 webpack support for SCSS stylesheets modules and generation of accompanying typings.

## Install

`yarn add gatsby-plugin-scss-typescript`

## Usage

1.  Include the plugin in your `gatsby-config.js` file.
2.  Write your SCSS and import them as normal.

```javascript
// in gatsby-config.js
plugins: ['gatsby-plugin-scss-typescript'];
```

Only files that include the `.module.scss` extensions shall be treated as module files, and hence have typings generated. `.scss` files shall be loaded using the regular [css-loader](https://github.com/webpack-contrib/css-loader).

## Options

If you need to pass options to the underlying css-loader use the plugins options; see [css-loader](https://github.com/webpack-contrib/css-loader)
for all available options.

```javascript
// in gatsby-config.js
plugins: [
    {
        resolve: 'gatsby-plugin-scss-typescript',
        options: {
            importLoaders: 1,
            localIdentName: '[local]___[hash:base64:5]_[emoji:1]',
        },
    },
];
```
