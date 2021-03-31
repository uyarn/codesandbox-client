---
title: FAQs
authors: ['CompuIves']
slug: /faqs
description: Answers to the mostly commonly asked CodeSandbox-related questions.
---

## Which languages and frameworks are supported?

CodeSandbox works with JavaScript (including TypeScript) and has front-end and
full-stack support.

We have client templates available for the following languages and frameworks: React, Vue, Angular, Preact, Svelte, Dojo, CX,
Reason, vanilla JavaScript (powered by Parcel), and one for static
(HTML, JavaScript, CSS) projects.

We also have container templates for the following: Node.js, Angular, Adonis, Gatsby, Marko,
Nuxt, Next, Sapper, Apollo, Ember, Nest, Styleguidist, MDX Deck, Gridsome,
Quasar, Docusaurus and Vuepress.

[Create a sandbox from a template](https://codesandbox.io/s/), or read more
about the
[difference between client and container sandboxes](/docs/environment).

## How do I make a sandbox private?

Note that a [Pro subscription](https://codesandbox.io/pricing) is required to
make sandboxes private or unlisted.

You can set a sandbox as private in two main ways: From the editor, change the
privacy setting from the Privacy drop-down under Sandbox Info.

![Make private in the editor](./images/sandbox-private.png)

You can also make a sandbox private from the dashboard right-click and select make private.
<!-- Picture needs to be included for this as well -->

## Why am I getting a 422 error when importing from GitHub?

There are a few possible reasons why you might receive a 422 error when importing a repository from GitHub. To fix this problem, ensure that the following conditions are met:
- Your repository contains`package.json` file
- Your project contains less than 500 modules (files). 

If the 422, error persists. please[get in touch](mailto:hello@codesandbox.io) with us
and provide a link to the repo you're importing and we will try our best to assist you in solving the problem.

## Why are my start scripts not having any effect?

For performance reasons we ignore any specified scripts in client sandboxes,
instead using a default script. If you need to control the scripts, then we
recommend using a container sandbox.
<!-- this need to be worded better = -->
## Can I change the Node version used in a container sandbox?

Yes you can. Container sandboxes run on Node v10.20.1 (LTS) by default. However, you can
specify a `node` version the in `sandbox.config.json` file. For more details, see [configuration](/docs/configuration).
<!-- maybe include a screen shot highlighting exactly where to put the node version in the config file -->
## Can I open the terminal or console or test panel instead of the browser in a sandbox?
<!-- I don't understand this question -->
Yes, the terminal, console, and problems tabs are all draggable. Click on the
tab and drag it up into the bar alongside browser and tests. You can then
re-order those items by dragging them in that bar. Whichever is 1st from left to
right in the list of tabs is what opens first when other folks view the sandbox.
The ordering is maintained within the sandbox. You can also achieve this change
by setting a value for "view" in a
[sandbox config file](/docs/configuration#sandbox-configuration).

## How do I change the font used in the editor?

Ensure the font you want to use has been installed on your computer, then put
the name of it first in the comma-separated list under 'Editor: Font Family'
from File > Preferences > Settings in the editor.
<!-- This needs to be displayed in a screenshot
Also, include a link to a resource that discusses how to install a font on your computer -->
## Are there any limitations with sandboxes?

- A sandbox cannot use more than 500 modules (files). Note though that
  `node_modules` and dependencies are not counted towards this limit.
- Imported sandboxes must contain a `package.json` file.
- The maximum file size that can be opened in the editor is 2MB. Files uploaded
  that are larger than that still exist but are linked as a static asset.
- The maximum file upload size is 7MB. If you need to upload a larger file, please
  [email us](mailto:hello@codesandbox.io) with your username and
  type and size of the file(s) you want to upload.
- In container sandboxes, there is a sync limit of 10 files per second and only
  files up to 2MB are synced with the editor. 
  <!-- what does mean- synced with the editor -->
  Files larger than that still exist
  but are not shown in the editor's file tree. You're still able to write and
  read to and from them in your code code and they can be seen and edited via
  the terminal.
<!-- is there some way to show this in practice? maybe a sample sandbox where this is the case -->
- Terminal commands which alter the filesystem of the container instance aren't
  synced with files shown in the editor. You'll need to refresh to see files
  updated this way.
- Container sandboxes sleep after 10 minutes and can be woken by opening
  the sandbox or preview in a web browser.
<!-- by opening the sandbox? what does this mean?-->
## I'm getting a 'Request Entity too Large' error. What should I do?

If you encounter this error when importing a project to CodeSandbox, check your sandbox or
repo for large binary files and remove them.
<!-- might be helpful to include examples of large binary files -->
## Can I use a database on CodeSandbox?

Yes. With container sandboxes,  you can use file-based database options like [SQLite](https://codesandbox.io/s/sqlite3-sequelize-example-starter-lst3n), [Lowdb](https://codesandbox.io/s/lowdb-json-file-database-example-starter-pldy5), and [NeDB](https://codesandbox.io/s/nedb-example-starter-kyv7s). For more
powerful databases like MongoDB, MySQL, etc. we recommend using a third-party
host, like [MongoDB Atlas](https://codesandbox.io/s/mongodb-database-example-starter-v3ker),
and interacting with them through an API or SDK.

## How do I change the editor theme?

You can change the theme from File > Preferences > Color Theme in the editor.
<!-- gif or image would be helpful here -->
You can also set a custom VS Code theme. Open VS Code, Press (CMD or CTRL) +
SHIFT + P, Enter: '> Developer: Generate Color Scheme From Current Settings',
copy the contents and paste it into Preferences > Appearance from the top-right
avatar menu. After completing that you need to reload the browser and select
"Custom" as your color theme from File > Preferences > Color Theme.
<!-- gif or image would be helpful here. maybe even short video -->
## I can't edit my code because of an infinite loop. What should I do?

While we do have infinite loop protection as a
[configurable option](https://codesandbox.io/docs/configuration), there are still scenarios where infinite loops can occur, such as with incomplete
code. When this happens, you can append `runonclick=1` to the editor URL to stop
the code from being automatically executed. This will stop the infinite loop and allow you to edit your code. 
<!-- For example:
[https://codesandbox.io/s/new?runonclick=1](https://codesandbox.io/s/new?runonclick=1) -->
<!-- not sure how this is a infinite loop example -->
## How do I cancel my Pro or Patron plan?

For Pro users, you can cancel your subscription on the
[Pro page](https://codesandbox.io/pro). For legacy Patron users, you can cancel
your subscription on the [Patron page](https://codesandbox.io/patron).
<!-- screen shot please -->