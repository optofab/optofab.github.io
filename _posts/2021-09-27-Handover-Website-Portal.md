---
layout: post
---

{% include toc %}

> This documentation is written for future TechLauncher team, as well as anyone who's willing to contribute to this project. The code is hosted in a public GitHub repository: [OptoFab Website Portal](https://github.com/swingrope/optofab-website).

## Requirements

The whole project is bootstrapped with [Create React App](https://github.com/facebook/create-react-app). Their documentation is a great place for you to get started if you are not familiar with developing in `React`.

0. Some basic terminal commands are useful throughout the entire project development, you can have a quick refresh [here](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview).
1. In most cases, we need to develop and test the website locally. To run the website locally, you need to intall the latest [`node.js`](https://nodejs.org/en/download/) manully first. Note that you’ll need to have Node 14.0.0 or later version in order for the successufl development on your local development machine, however, for the server side, it's not required.
2. For version control, you also need to install [`git`](https://git-scm.com/downloads) first. For more detailed quickstart with GitHub, please refer to the docs in GitHub [here](https://docs.github.com/en/get-started/quickstart/set-up-git). With `git` installed and a valid GitHub account, clone the project to your local drive, e.g. `git clone git@github.com:swingrope/optofab-website.git`, and `cd` into the folder `optofab-website`.
3. In the terminal, use the command `npm install` to install dependent node modules specified in the `package.json` automatically.

## Code Structure

### Main Pages

The overall structure of the main files and folders inside the project is as follows:

```
optofab-website
├── README.md
├── node_modules
├── package.json
├── .gitignore
├── public
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
├── backend
└── src
    ├── App.css
    ├── App.js
    ├── App.test.js
    ├── components
    │   ├── backgrounds
    │   │   ├── OvalBackground.js
    │   │   └── WaveBackground.js
    │   ├── buttons
    │   │   ├── SubmitButton.js
    │   │   └── UploadButton.js
    │   ├── layout
    │   │   ├── Header.js
    │   │   ├── layout.css
    │   │   └── layout.js
    │   ├── sections
    │   │   └── HeroSection.js
    │   ├── styles
    │   │   ├── ColorStyles.js
    │   │   ├── GlobalStyles.js
    │   │   └── TextStyles.js
    │   └── tooltips
    ├── data
    ├── features
    │   └── form
    │       ├── components
    │       │   ├── Coating.js
    │       │   ├── CustomerInfo.js
    │       │   ├── Geometry.js
    │       │   ├── Layer.js
    │       │   ├── Material.js
    │       │   ├── Spec.js
    │       │   ├── Substrate.js
    │       │   └── Surface.js
    │       ├── fields
    │       │   ├── MyTextArea.js
    │       │   └── MyTextInput.js
    │       ├── Feedback.js
    │       ├── Helpers.js
    │       ├── MainForm.js
    │       ├── Modify.js
    │       └── Track.js
    ├── images
    ├── index.css
    ├── index.js
    ├── logo.svg
    ├── pages
    ├── serviceWorkererviceWorker.js
    └── setupTests.js
```

There're five main pages in the website portal.

#### Update Packages

The [`package.json` file](https://nodejs.org/en/knowledge/getting-started/npm/what-is-the-file-package-json/) in the root directory "holds various metadata relevant to the project. This file is used to give information to npm that allows it to identify the project as well as handle the project's dependencies. It can also contain other metadata such as a project description, the version of the project in a particular distribution, license information, even configuration data - all of which can be vital to both npm and to the end users of the package." On the other hand, The [`package-lock.json` file](https://docs.npmjs.com/cli/v7/configuring-npm/package-lock-json) "is automatically generated for any operations where npm modifies either the node_modules tree, or package.json. It describes the exact tree that was generated, such that subsequent installs are able to generate identical trees, regardless of intermediate dependency updates."

Caveat: If you are sure and have tested in your team that the website files will still work without breaking anything in the latest packages with dependecies, use the following command line code to update to the latest versions with the help of [`npm-check-updates`](https://www.npmjs.com/package/npm-check-updates):

```terminal
npm i -g npm-check-updates
ncu -u
npm install
```

### Styling

At the core of styling, `CSS` is integrated into most of the components thanks to the npm package `styled-components`. The main reasons for using `styled-components` are automating styling with less painful maintainence and avoiding class name bugs within the `React` component system. For documentation on how to get started with `styled-components`, refer to their official documentaion [here](https://styled-components.com/docs/basics#getting-started). Please duplicate the project design and make customized modifications.

#### Prototype

Most of the color schemes, text settings, icons, background images, inputbox components, and detailed design of every single page involved is based on the Figma file [here](https://www.figma.com/community/file/1025776448190506190/OptoFab-Portal-Design) which has been published to the Figma community. Please duplicate the project and make customized

#### Dark and Light Themes

Global styles are set in the file `./src/components/styles/GlobalStyles.js` where it supports both light and dark mode themes, although we haven't got time to adapt every single element like the font color or some background images to go well with the theme change. It can be fine tuned by importing `themes` from `./src/styles/ColorStyles.js` and specifying the color scheme to use.

For example, we have the title in `./src/components/sections/HeroSection.js` using the following:

```js
const Title = styled(H1)`
  color: ${themes.dark.text1};
`;
```

**Caveat**:

If you need to dynamically change the theme based on the user's preference, use the default styling as usual, but add `@media (prefers-color-scheme: dark)` to customized the styled tag separately. For example, for the wave background in the hero section, if the user's theme is dark, the background wave can change from a default white wave to a darker wave using the following:

```js
const BottomWave = styled(Wave)`
  @media (prefers-color-scheme: dark) {
    content: url("/images/waves/hero-wave3-dark.svg");
  }
`;
```

#### Layout

As a recommended practice to avoid confusing css styles, all the default html tags are reset using the public domain [stylesheet](http://meyerweb.com/eric/tools/css/reset/) from Meyer. The reset css code resides in the file `./src/components/layout/layout.css`.

The Header on most pages are specified in the file `./src/components/layout/Header.js`. The Header file is using the static data from `./src/data/MenuData.js` which is a temporary solution. For future CMS management, you may consider using services like [`contentful`](https://www.contentful.com/developers/docs/) to host the data and cooperate within your team.

**Caveat**:

Bug: The function of the tooltip is missing right now and needs fixing if you are trying to use the Hamburger button on smaller screen.
Bug: In some pages, some of the header links are unclickable. The temporary solution is to click on the logo and go back to the homepage and start from there to the page you want to visit.

#### Backgounds

As of now, three background components are ready to use for any page that needs a waved or oval shaped background. Simply import the background file into the page/component you want to create. Alternatively, you can generate similar background components using customized background images from `svg/png/jpg` files.

#### Buttons

**Caveat**:

The components in `./src/components/buttons` need to refactor for simplicity and better maintainence in th future. Most of the buttons styles correspond to the design files in the Figma file provided.

### Deployment

The front-end has been deployed to `https://tl20212.cecs.anu.edu.au`.

#### `SSH` to ANU Server

First, you need to be added to the sudo user group by a member already in that group. If you are the first one in your team to do so, please contact [us](mailto:tian.wu@anu.edu.au?cc=hengrui.xu@anu.edu.au) for details.

#### `HTTP` to `HTTPS`

This has been taken care of by `certbot`. It renews the certificate automatically.

#### `Nginx` Config

After connecting to the ANU server, you can check the config file in `/etc/nginx/sites-available/default`.

#### Build & Deploy to ANU Server

Currently, there are two ways to update the website:

1. You can manually git clone the project and build it locally.
2. Or you can use command line tools `scp` to copy the locally built files to the ANU server.

## Known Issues/Bugs

1. Display on smaller screens

2. PHP deployment

3. Upload file type/size check

4.

## Contact
