[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)

## [Webogram](https://web.telegram.org) — Telegram Web App with Incognito wallet

Telegram offers great [apps for mobile communication](https://www.telegram.org). It is based on the [MTProto protocol](https://core.telegram.org/mtproto) and has an [Open API](https://core.telegram.org/api). I personally like Telegram for its speed and cloud-support (that makes a web app possible, unlike in the case of WA and others).

MTProto data can be carried over HTTP (SSL is also supported), so this project is my take at creating one.

That said, I'm using this app myself and I'd like to share its sources, so anyone can contribute to the development. Any help is welcome!

### Features currently supported by incognito

* Set up your incognito account via your Telegram account
* Import/Export incognito account
* Create new Incognito account
* Remove account from accounts list
* Display all key for accounts
* Display balances for all currencies 
* Token following
* Transfer your PRV to another account by incognito address or telegram username

### Maintained locations


| Description        | URL           | Type  |
| ------------- |-------------| -----:|
| Online Web-version (hosted on 482solutions servers)      | http://incognito.482.solutions/ | hosted


**Hosted version**: the app is downloaded via HTTPS as a usual website. Will be available offline due to application cache.

**Packed version**: the app is downloaded at once in a package via HTTPS. The package is updated less frequently than the Web-version.

All of the apps above are submitted and maintained by [@zhukov](https://github.com/zhukov), so feel free to use them and report bugs [here](https://github.com/zhukov/webogram/issues). Please do not report bugs which are only reproducible in different locations.


### Interface


Here are some screenshots of the interface:


![Incognito screenshot 2](/app/img/screenshot2.png)
![Incognito screenshot 3](/app/img/screenshot3.png)
![Incognito screenshot 4](/app/img/screenshot4.png)
![Incognito screenshot 5](/app/img/screenshot5.png)
![Incognito screenshot 6](/app/img/screenshot6.png)
![Incognito screenshot 7](/app/img/screenshot7.png)
![Incognito screenshot 8](/app/img/screenshot8.png)

## Technical details

The app is based on the AngularJS JavaScript framework, and written in pure JavaScript. jQuery is used for DOM manipulations, and Bootstrap as the CSS-framework.


### Running locally


The project repository is based on angularjs-seed and includes gulp tasks, so it's easy to launch the app locally on your desktop.
Install [node.js](http://nodejs.org/).

Install dependencies with:

```lang=bash
npm install
```

Optionally, run the following commands in the project directory to install gulp globally:

```lang=bash
sudo npm install -g gulp
```

This will install all the needed dependencies.


#### Running web-server


Just run `npm start` (`gulp watch`) to start the web server and the livereload task.
Open http://localhost:8000/app/index.html in your browser.



#### Running as Chrome Packaged App

To run this application in Google Chrome as a packaged app, open this URL (in Chrome): `chrome://extensions/`, then tick "Developer mode" and press "Load unpacked extension...". Select the downloaded `app` folder and Webogram should appear in the list.

Run `npm start` (`gulp watch`) to watch for file changes and automatically rebuild the app.


#### Running as Firefox OS App

To run this application in Firefox as a packaged app, open "Menu" -> "Developer" -> "WebIDE" (or hit `Shift + F8`). Choose "Open packaged app" from the Project menu and select the `app` folder.

Run `npm start` (`gulp watch`) to watch for file changes and automatically rebuild the app.

#### Running in production

Run `npm run clean` (`gulp clean`), then `npm run build` (`gulp publish`) to build the minimized production version of the app. Copy `dist` folder contents to your web server. Don't forget to set `X-Frame-Options SAMEORIGIN` header ([docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/X-Frame-Options)).


### Third party libraries

Besides the frameworks mentioned above, other libraries are used for protocol and UI needs. Here is the short list:

* [JSBN](http://www-cs-students.stanford.edu/~tjw/jsbn/)
* [CryptoJS](https://code.google.com/p/crypto-js/)
* [zlib.js](https://github.com/imaya/zlib.js)
* [UI Bootstrap](http://angular-ui.github.io/bootstrap/)
* [jQuery Emojiarea](https://github.com/diy/jquery-emojiarea)
* [nanoScrollerJS](https://github.com/jamesflorentino/nanoScrollerJS)
* [gemoji](https://github.com/github/gemoji)
* [emoji-data](https://github.com/iamcal/emoji-data)

Many thanks to all these libraries' authors and contributors. A detailed list with descriptions and licenses is available [here](/app/vendor).


### Licensing

The source code is licensed under GPL v3. License is available [here](/LICENSE).


### [Contribute](CONTRIBUTING.md)
