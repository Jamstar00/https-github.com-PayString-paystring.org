<p align="center">
  <a href="https://paystring.org">
    <img alt="PayString" src="https://paystring.org/icons/icon-72x72.png" width="60" />
  </a>
</p>
<h1 align="center">
  PayString Marketing Site
</h1>

> **Note:** This repository contains a copy of the PayString website from [github.com/PayString/paystring.org](https://github.com/PayString/paystring.org)

This repository powers the [PayString.org](https://paystring.org) web application built using [Gatsby](https://gatsbyjs.org)

## ⚙️ Requirements

- **Node.js 18.x or higher** - This project requires Node 18 or higher
- **npm 6.x or higher**

## 🚀 Quick start

1.  **Clone the PayString.org repository.**

    Use git to pull down the PayString.org repository.

    ```shell
    git clone https://github.com/paystring/paystring.org.git
    ```

2.  **Start developing.**

    Navigate into PayString.org's directory, install the packages, and start it up.

    ```shell
    cd paystring.org/
    npm i
    npm run start
    ```

3.  **Start editing!**

    PayString.org is now running at `http://localhost:8000`!

    Save your changes and the browser will update in real time!

## 🧐 What's inside?

A quick look at the top-level files and directories you'll see in the PayString.org repository.

    .
    ├── .github
    ├── .vscode
    ├── node_modules
    ├── src
    ├── static
    ├── .dockerignore
    ├── .gitignore
    ├── .gitlab-ci.yml
    ├── Dockerfile
    ├── gatsby-browser.js
    ├── gatsby-config.js
    ├── package.json
    ├── package-lock.json
    ├── README.md
    ├── tailwind.config.js
    └── tsconfig.json

1.  **`/.github`**: This directory contains github configuration files such as the `CODEOWNERS` file.

2.  **`/.vscode`**: This directory contains the recommended vscode extensions and settings for the editor.

3.  **`/node_modules`**: This directory contains all of the modules of code that our project depends on (npm packages) are automatically installed when using the `npm i` command.

4.  **`/src`**: This directory contains all of the code related to what you will see on the front-end of PayString.org. `src` is a convention for “source code”.

5.  **`/static`**: This directory contains any files or assets that will be accessible at the root of https://PayString.org. For instance favicon.ico can be accessed at https://PayString.org/favicon.ico.

6.  **`.dockerignore`**: This is a configuration file for [Docker](https://docker.com/). Dockerignore tells our docker build to exclude certain directories from the docker container.

7.  **`.gitignore`**: This is a configuration file for git. The gitignore tells us which files to exclude in our committed source code.

8.  **`.gitlab-ci.yml`**: This is a configuration file for [Gitlab CI](https://docs.gitlab.com/ee/ci/yaml/README.html). This is the required steps that setups up our continuous deployment as well as tests our code to ensure our code meets basic standards before being merged into github.

9.  **`Dockerfile`**: This is a configuration file for [Docker](https://docker.com/). The Dockerfile tells the docker container how to process and deploy the code.

10.  **`gatsby-browser.js`**: This file is where Gatsby expects to find any usage of the [Gatsby browser APIs](https://www.gatsbyjs.org/docs/browser-apis/). These allow customization/extension of default Gatsby settings affecting the browser.

11.  **`gatsby-config.js`**: This is the main configuration file for a Gatsby site. We specify information about PayString.org like the site title and description, which Gatsby plugins we include, etc. (Check out the [gatsby config docs](https://www.gatsbyjs.org/docs/gatsby-config/) for more detail).

12.  **`package.json`**: A manifest file for Node.js projects, which includes things like metadata (the project’s name, author, etc). This manifest is how npm knows which packages to install for your project.

13.  **`package-lock.json`** (See `package.json` below, first). This is an automatically generated file based on the exact versions of your npm dependencies that were installed. **(You won’t change this file directly).**

14.  **`README.md`** This the code that hosts the helpful content you are reading right now.

15.  **`tailwind.config.js`**: This is the main css configuration file that holds all of our theming configuration. This is for the [CSS framework tailwind](https://tailwindcss.com/) which we use for PayString.org.

16.  **`tsconfig.js`**: This is the configuration file for our typescript configuration. We use a strict configuration that doesn't allow any loose typings in order to maintain a high code quality.
