# Material + Flex-layout

[![Greenkeeper badge](https://badges.greenkeeper.io/arangates/sastrayonitvat.svg)](https://greenkeeper.io/)

Include angular material + flex layout for material design components

# Lodash

Lodash FP is latest
@Memoize helps improving performance by remembering the function result for same input pure functions

https://blog.codeminer42.com/functional-programming-with-lodash-fp-8fe0619b3024

https://medium.com/@armno/til-importing-lodash-into-angular-the-better-way-aacbeaa40473

# WebAnimations
`npm install --save web-animations-js`

Include web animations in polyfill to use browser animations

# Generate project with service worker for PWA 
`ng new angular-pwa-app --service-worker --style=scss --routing`

# HMR
enable HMR for app for faster development
https://github.com/angular/angular-cli/wiki/stories-configure-hmr

# Material Icons

include Google material Icons 

# Rxjs Extentions

Include rxjs extensions in polyfills , to use it across the app without importing



<p align="center">
  <a href="https://sastrayonitvat-dev.firebaseapp.com">
    <img alt="OM" src="public/om.png" width="546">
  </a>
</p>
arthashastra
vivekanandha quotes

# Sastrayonitvat - The scripture being the source of right knowledge
[![Build Status][travis-image]][travis-url]
[![Dependency Status][daviddm-image]][daviddm-url]
[![License][license-image]][license-url]
[![Code Coverage][coverage-image]][coverage-url]
[![Code Style][code-style-image]][code-style-url] 
[![Lighthouse Score][pwa-image]][pwa-url]

http://sssbpt.org/sri-rudram/instructions-to-user.htm

http://compendia.samskrutam.com/MainPage.ashx

You can find a example of this project in this [DEMO](https://sastrayonitvat-dev.firebaseapp.com/).

### Simple run


To just run the project on you won device you should have installed: git, node and npm. Let's asume that this is the case.

Now in your concole go to the destionation where you want to save the project and run this command:

```js
git clone https://github.com/arangates/sastrayonitvat.git
```

or

```js
git clone https://github.com/arangates/sastrayonitvat.git my_project
```

if you want to save the project into a specific folder (inthis example "my_project"). The folder must be empty!

Now go with the console into the folder. If you havn't provided a name like "my_project" then it will be the default "sastrayonitvat".

In he folder run this command to start the develeoplemt mode of the project:

```js
npm run dev
```

For publishing run:

```js
npm run build
```

After it finished folloe the instructions or publish the project build folder to your prefered  provider or own server.

### Reuse for own project

You can eather fork this project or clone it into your own repo. I use the second for new projects. You can find [here](https://help.github.com/articles/duplicating-a-repository/) more information about how to clone/duplicate a repo into your own.

After cloning the repo into your own you should change the configurations like project name and the firebase config. Here is a list of all changes you should make:
* **package.json**  - here you should change the name and version
* **src/config.js**  - here you should change all firebase data and other options
* **public/index.html**  - change the title (it will be overriden but it looks better)
* **public/firebase-messaging-sw.js**  - change the ``messagingSenderId``


After setting up the code we need to deploy our application to firebase. As first create an application biuld with runing `npm run build`.

How might my targeted audience change?
    if the app really deos well and found its way around teaching,people from universities
    may slowly start to use and it might also help for vedha researchers.

Do they all have the same reqirements?
    Pretty much Yes., but we dont know actually. we will have to adapt.

How can i find out?
    from the Feedback from users.
    or maybe a FB fanpage ,if required.

What platform most people use ?
    80% browsers and android phone.

What connectivity do my users h ave?
    basic 3G or 2G connectivity.

Where will the users be when using the application/
    home,temple mostly.

what content must it Definetly deliver?
    -sanskrit text
    -english text(defalut) / prefferd language
    -audio
    -desctiption
    -comment
    -public commet option for particular module to let user express their views.

what are functionalities nice to have?
    -multi-language support
    -Rich content
    -Offline first
    -commenting
    -feedback mechanisms
    

Offline?
    Definetly !!!

### Authorisation

Authentication and authorisation are not the same thing! With authentication we identify who we have as user and with athorisation we identify what that user can do in our application. In this project authorisation is managed over `grants` and `roles`. Every grant gives the user the authorisation to do a specific action (read, create, edit or delete) in the database. Roles are defining a group of grants you can give a user. They are just for managing large number of grants easely. Every grant can still be managed seperately.

Only administrators have access to add or remove grants and roles to a user. Only administrators can make other users to administrators.

**WARNING:** In this demo the rules are manipulated that everyone can make other users to admins and even himselfe. So everyone can see how it works. In production there should be made a change in the database.rules file.

From:

```js
"admins":{
  ".read": "auth != null",
  "$uid":{
    ".write": "auth != null || root.child('admins/'+auth.uid).exists()"
  }
},

```

To:

```js
"admins":{
  ".read": "auth != null",
  "$uid":{
    ".write": "auth != null && root.child('admins/'+auth.uid).exists()"
  }
},

```


- Refer the project page of the repo [Satryonitvat - TODO](https://github.com/arangates/sastrayonitvat/projects)

## Logo

Om (Auṃ or Oṃ, Sanskrit: ॐ) is a sacred sound and a spiritual icon in Hindu religion. It is also a mantra in Hinduism, Buddhism, Jainism, and Sikhism.

## License

MIT

[logo-image]: assets/images/icons/icon-512x512.png
[logo-url]: https://github.com/arangates/sastrayonitvat/blob/master/README.md
[travis-image]: https://travis-ci.org/arangates/sastrayonitvat.svg?branch=master
[travis-url]: https://travis-ci.org/arangates/sastrayonitvat
[daviddm-image]: https://img.shields.io/david/arangates/sastrayonitvat.svg?style=flat-square
[daviddm-url]: https://david-dm.org/arangates/sastrayonitvat
[coverage-image]: https://img.shields.io/codecov/c/github/arangates/sastrayonitvat.svg?style=flat-square
[coverage-url]: https://codecov.io/gh/arangates/sastrayonitvat
[license-image]: https://img.shields.io/npm/l/express.svg
[license-url]: https://github.com/arangates/sastrayonitvat/master/LICENSE
[code-style-image]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[code-style-url]: http://standardjs.com/ 
[pwa-image]: https://img.shields.io/badge/pwa%20score-98%25-blue.svg
[pwa-url]:https://img.shields.io/badge/pwa%20score-98%25-blue.svg