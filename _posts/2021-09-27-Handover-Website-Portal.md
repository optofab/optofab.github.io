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

Main files and folders inside the project.

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
        ├── backgrounds
        ├── buttons
        ├── layout
        ├── sections
        ├── styles
        └── tooltips
    ├── data
    ├── features
        └── form
    ├── images
    ├── index.css
    ├── index.js
    ├── logo.svg
    ├── pages
    └── serviceWorker.js
    └── setupTests.js
```

There're five main pages in the website portal.

#### Update Packages

### Styling

### Deployment

#### `SSH` to ANU Server

#### `HTTP` to `HTTPS`

#### `Nginx` Config

#### Build & Deploy to ANU Server

## Known Issues/Bugs

1. Display on smaller screens

2. PHP deployment

3. Upload file type/size check

4.

## Contact
