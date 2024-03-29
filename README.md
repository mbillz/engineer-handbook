# Engineer Handbook

_A guide and resource for modern engineering_

## Table of Contents

1.  [Development Tools](#tools) :wrench:
1.  [Style Guide](#style) :nail_care:
1.  [Server Management Resources](#server) :cloud:

<a name="tools"></a>

## Development Tools :wrench:

<a name="tools--editor"></a><a name="1.1"></a>

- [1.1](#tools--editor) **Code Editor**

  - [Visual Studio Code](https://code.visualstudio.com/)

<a name="tools--build"></a><a name="1.2"></a>

- [1.2](#tools--development) **Development Tools**

  - [Git](https://git-scm.com/) | _Version Control_

    - [Getting Started Guide](http://rogerdudler.github.io/git-guide/)

  - [Webpack](https://webpack.js.org/) | _Build Tool &amp; Bundler_

    - [Getting Started Guide](https://webpack.js.org/guides/getting-started/)

  - [ESLint](https://github.com/eslint/eslint) | _JavaScript Linter_

    - [ESLint Visual Studio Code extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

  - [stylelint](https://github.com/stylelint/stylelint) | _CSS Linter_

    - [styelint Visual Studio Code extension](https://marketplace.visualstudio.com/items?itemName=shinnn.stylelint)

  - [Prettier](https://github.com/prettier/prettier) | _JavaScript Formatting Tool_

<a name="style"></a>

## Style Guide :nail_care:

<a name="style--react"></a><a name="2.1"></a>

- [2.2](#style--react) **React**

  <a name="react--frameworks"></a><a name="2.1.1"></a>

  - [2.1.1](#react--frameworks) **Frameworks**

    - [Gatsby - Static Site Generator](https://www.gatsbyjs.org/)

      - A React based static site generator for creating speed optimized web apps. It builds into static HTML files, but it is simple to implement GraphQL or REST request for a dynamic user experience.

    - [NextJS - Server Side Rendering Framework](https://nextjs.org/)

      - A React based framework that builds into a Node app allowing a developer to easily implement routing and server side rendering without going through the trouble of building their own custom Express server.

  <a name="react--modern-practices"></a><a name="2.1.2"></a>

  - [2.1.2](#react--modern-practices) **Modern Practices**

    - [Hooks](https://reactjs.org/docs/hooks-intro.html)

      - Hooks enable a developer to use state and lifecycle methods without using ES6 classes.

<a name="style--wordpress"></a><a name="2.2"></a>

- [2.1](#style--wordpress) **Wordpress**

  <a name="wordpress--framework"></a><a name="2.2.1"></a>

  - [2.2.1](#wordpress--framework) **Framework**

    - A modern Wordpress framework written by Matt Billings is used to allow for modern JS & CSS features to be utilized. The framework is available [here](https://github.com/mbillz/wordpress-starter).

  <a name="wordpress--structure"></a><a name="2.2.2"></a>

  - [2.2.2](#wordpress--structure) **Structure**

    - Theme development takes place in `/src`. JavaScript is written in `/src/js/` and CSS is written in `/src/css`. The Wordpress theme is developed in `/src/theme/`.

    - Custom page templates are placed in `/src/theme/page-templates`.

    - Single post type templates, archives, and category pages are placed in the root of theme in `/src/theme`.

    - Reusable modules that multiple templates throughout the theme call are placed in `/src/theme/inc` and called by the `get_template_part()` function as documented [in the Wordpress codex](https://developer.wordpress.org/reference/functions/get_template_part/).

    - Images used by the theme are placed in `/src/theme/img`.

    - When necessary, any vendor CSS or JS files are placed in `/src/theme/vendor` (as further described below).

  <a name="wordpress--css"></a><a name="2.2.3"></a>

  - [2.2.3](#wordpress--css) **CSS**

    - CSS is organized and written in a modular structure. All files are imported into `/src/css/index.css`. Organize files by feature or page. A reset.css is included in the repository.

    - [BEM](http://getbem.com/)

      - All CSS is written using BEM to maximize collaboration. BEM or Block Element Modifier is a methodology that helps you to create reusable components and code sharing in front-end development

      - [Getting Started Guide](https://en.bem.info/methodology/quick-start/)

    - If making any fundamental changes to previously written code, please ensure that the modifications won't break anything else on the site.

    - Third party CSS will be installed by npm and imported in `index.css`. If the package isn't available by npm, place the css file in a `/src/theme/vendor` and enqueue the CSS file in `/src/theme/functions.php`. Use conditional statements to only enqueue external files when needed.

  <a name="wordpress--js"></a><a name="2.2.4"></a>

  - [2.2.4](#wordpress--js) **JavaScript**

    - JS is organized and written in a modular structure. All files are imported into `/src/js/index.js`. Organized files by feature.

    - When possible, write in plain JavaScript without jQuery. jQuery brings unecessary file size into a website. Modern JavaScript has brought many features from jQuery into use.

      - [PlainJS](https://plainjs.com/javascript/) is a helpful tool for functions and strategies that replace jQuery methods.

    - At times, clients require outside libraries that have jQuery as a dependancy so it will need to be included. In this case, enqueue it properly in `/src/theme/functions.php` as described [here](https://digwp.com/2009/06/including-jquery-in-wordpress-the-right-way/).

    - Third party JS libraries will be installed with npm and import in the relevant JS file. If the package isn't available by npm, place the css file in a `/src/theme/vendor` and enqueue the CSS file in `/src/theme/functions.php`. Use conditional statements to only enqueue external files when needed.

  <a name="wordpress--fonts"></a><a name="2.2.5"></a>

  - [2.2.5](#wordpress--fonts) **Fonts**

    - Custom fonts are placed in `/src/fonts`.

    - Only .woff and .woff2 are necessary in modern browsers.

<a name="server"></a>

## Server Management Resources :cloud:

<a name="server--ubuntu"></a><a name="3.1"></a>

- [3.1](#server--ubuntu) **Ubuntu**

  - [How To Install Nginx on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04)

  - [How To Install Node.js on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04)

  - [How To Set Up a Node.js Application for Production on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-node-js-application-for-production-on-ubuntu-18-04)

  - [How To Install Linux, Apache, MySQL, PHP (LAMP) stack on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-ubuntu-18-04)

- [3.2](#server--general) **General**

  - [How To Add Swap Space on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-add-swap-space-on-ubuntu-18-04)

* [3.3](#server--lets-encrypt) **Lets Encrypt**

  - [How To Secure Nginx with Let's Encrypt on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-18-04)
