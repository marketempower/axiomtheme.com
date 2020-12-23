+++
weight = 5
title = "Upgrade Guide"
subtitle = "Upgrading Axiom from v0.7.x to v0.8.0 - Tailwind CSS v2."
tags = ["upgrade"]
categories = ["docs"]
+++

Upgrading Axiom from v0.7.x to v0.8.0 - Tailwind CSS v2.

Axiom's v0.8.0 release is a major upgrade from v0.7.x and includes some breaking changes due to changes in Tailwind CSS v2.

In general the upgrade doesn't change anything major within a deployed Axiom website, as the changes are mainly on the build side.

## Reference the Example Project's v0.4.0 Commits

The Example project's [v0.4.0 commits](https://github.com/marketempower/axiom-example/commits/v0.4.0) on Dec 23, 2020 show all the major steps required to upgrade a typical project.

The rest of this document breaks down each of those commits one-by-one.

## Update Your Project's Axiom Theme Version

Follow the documentation on [Updating the Theme]({{< relref "docs/quick-start#updating-the-theme" >}}) to update your project's Axiom theme version to v0.8.0.

## Update Your Project's package.json File

Update your project's `package.json` file `devDependencies` section to match the Axiom Example project's [section](https://github.com/marketempower/axiom-example/blob/v0.4.0/package.json#L26).

Install the updated package versions:

```shell
# cd into project root
cd example.com

# Empty the /node_modules directory

# Install updated package versions
npm install
```

## Upgrade Your Project's tailwind.config.js File

Upgrade your project's `tailwind.config.js` file to match the Example project's [file](https://github.com/marketempower/axiom-example/blob/v0.4.0/tailwind.config.js).

## Remove References to Deprecated Tailwind CSS Classes

Tailwind CSS v2 changed or deleted some of the class names it provides. You'll need to search and replace within your project to update any instances. See the Tailwind CSS [v2 Upgrade Guide](https://tailwindcss.com/docs/upgrading-to-v2) for more information.

## Rebuild Your Project's CSS Assets

See the Extending Axiom [Custom CSS]({{< relref "docs/extending#custom-css" >}}) documentation and rebuild your project's CSS assets.

## Build and Preview Locally to Verify

Build and preview your project locally to verify the CSS is displaying as intended. Tailwind CSS v2 changed all the color values dramatically, so pay careful attention to shifts in saturation and naming.
