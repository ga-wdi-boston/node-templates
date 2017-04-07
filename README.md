[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# node-template

## Updating Dependencies

At the beginning of each cohort update [`package.json`](package.json):

-   replace all dependent package versions with a glob (`*`).
-   `rm -r node_modules`.
-   `npm update --save`.
-   `npm update --save-dev`.
-   `npm install`
-   `grunt test`

Fix errors and conflicts as necessary.

## Structure

Dependencies are stored in [`package.json`](package.json).

Do not configure `grunt` packages directly in the
[`Gruntfile.js`](Gruntfile.js). Instead, store configurations in the
[`grunt`](grunt) directory. You won't need a top-level key, since that's
generated by the `Gruntfile.js` based on the filename of the configuration
object stored in the `grunt` directory.

Developers should store JavaScript files in [`lib`](lib). If an entry point is
needed, it can go in the root of the project; `index.js` is the node default;
`app.js`, `main.js`, or `server.js` might be appropriate depending on the task.

`grunt server` will start `nodemon` on `bin/index.js`.

## Tasks

Developers should run these often!

-   `grunt nag`: runs code quality analysis tools on your code
    and complains.
-   `grunt test`: runs any automated tests; may depend on `grunt build`.
-   `grunt`: runs both `nag` and then `test`
-   `grunt make-standard`: reformats all your code in the standard style.

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.
1.  Does this show up as "3."

