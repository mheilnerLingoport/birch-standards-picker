# \<birch-standards-picker\>

[![Maintainability](https://api.codeclimate.com/v1/badges/8962312026628a7db1ae/maintainability)](https://codeclimate.com/repos/5c4b1f52d51c2b02b3001d2a/maintainability) [![Test Coverage](https://api.codeclimate.com/v1/badges/8962312026628a7db1ae/test_coverage)](https://codeclimate.com/repos/5c4b1f52d51c2b02b3001d2a/test_coverage) [![Build Status](https://travis-ci.com/fs-webdev/birch-standards-picker.svg?branch=master)](https://travis-ci.com/fs-webdev/birch-standards-picker)

A Polymer-based web component that enables entering and selection of standardized dates and places.

## Styling
The following custom properties and mixins are available for styling:
| Custom Property                       | Description               | Default |
|---------------------------------------|---------------------------|---------|
| `--birch-standards-picker-paper-item` | Mixin applied to the item | `{}`    |

## Properties

## Running the Component

<details>

1. (Once) Install or update the [Polymer CLI](https://www.npmjs.com/package/polymer-cli): ```npm i -g polymer-cli```
1. (Once) Install the [frontier-cli](https://github.com/fs-webdev/frontier-cli): ```npm i -g https://github.com/fs-webdev/frontier-cli```
1. Run `npm install` to get dependencies needed to set up the unit testing framework, useful commit hooks, and standards tools (`bower install` is also run as a post-install step).
1. Or (if you want to live dangerously) just run `bower install` to load all of the component's primary dependencies.
1. Run `polymer analyze > analysis.json` to initialize the docs page.

This component's auto-generated documentation is viewable by running:

```bash
frontier element serve
```

> NOTE: If you attempt to `frontier element serve` on a clean install, you will get an error, stating that the analysis.json file (used to populate the documentation page) does not exist. You can fix this by either running `frontier element serve -a`, or by auto-loading the demo page via:

```bash
frontier element serve -d
```

This component's demo page is viewable by running the above command.

</details>

## Online Docs & Demo

The FamilySearch Element Catalog is located at: [https://www.familysearch.org/frontier/catalog/](https://www.familysearch.org/frontier/catalog/), with access granted to members of the `fs-webdev` GitHub organization. [How to create a shared component of your own](https://www.familysearch.org/frontier/ui-components/creating-a-new-web-component/).

## Build, Commit, Test, and Standards Tools

For detail about automatic releases, test plugins, pre-commit hooks, and standards enforcement, see: [fs-common-build-scripts](https://github.com/fs-webdev/fs-common-build-scripts#)

> IMPORTANT NOTE: When running package dependency commands (i.e. `wct`, `standard`), you need to prefix the command with [`npx`](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b).

## Running Tests

<details>

This component is set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester).

To run tests locally, run:

```bash
npm test
```

which will run the standards checks through `semistandard` and `stylelint`, and then the unit tests via `wct`.

```bash
npx wct --skip-plugin sauce
```

If you need to debug locally (keeping the browser open), run:

```bash
npx wct --skip-plugin sauce -p
```

or

```bash
polymer test --skip-plugin sauce --local chrome -p
```

If you want to run the full suite of SauceLabs browser tests, run:

```bash
npx wct test/index.html --configFile wct.conf.json  --sauce-username {USERNAME} --sauce-access-key {ACCESS_KEY}
```

> NOTE: You can export `SAUCE_USERNAME` and `SAUCE_ACCESS_KEY` in your `.bash_profile` to be able to simply run `npx wct` without needing additional options.

</details>
