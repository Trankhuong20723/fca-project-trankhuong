## Important !

[ ENG ]: This package require NodeJS 14.17.0 to work properly.

[ VIE ]: Gói này yêu cầu NodeJS 14.17.0 để hoạt động bình thường.

## Support Language :

+ English
+ VietNamese
+ Tagalog
+ Cebuano(Bisaya)

## Download

If You Want To Use It, Download It By:
```bash
npm i trankhuong20723/fca-project-trankhuong 
```
or
```bash
npm install trankhuong20723/fca-project-trankhuong 
```

It Will Download To node_modules (Your Lib) - Note Replit Will Not Show Anywhere To Find 😪

### Download Latest Version Or Update

If You Want To Use The Latest Or Updated Version Then Go To Terminal Or Command Promt Type:
```bash
npm install trankhuong20723/fca-project-trankhuong@latest
```
Or
```bash
npm i trankhuong20723/fca-project-trankhuong@latest
```

## If You Want To Test Api

The benefit of this is that you won't waste time paying and having an account 😪
Please Use With Test Account => [Facebook Whitehat Accounts](https://www.facebook.com/whitehat/accounts/).

## Using

```javascript
const login = require("fca-project-trankhuong"); // get it from lib

// log in
login({email: "Gmail Account", password: "Your Facebook Password"}, (err, api) => {

     if(err) return console.error(err); // error case

     // create a bot that automatically imitates you:
     api.listenMqtt((err, message) => {
         api.sendMessage(message.body, message.threadID);
     });

});
```

As a result, it will imitate you as shown below:
<img width="517" alt="screen shot 2016-11-04 at 14 36 00" src="./Screenshot_2023-12-07-23-27-22-28_40deb401b9ffe8e1df2f1cc5ba480b12.jpg">
<img width="517" alt="screen shot 2016-11-04 at 14 36 00" src="./Screenshot_2023-12-07-23-32-51-67_40deb401b9ffe8e1df2f1cc5ba480b12.jpg">

If You Want Advanced Use Then Use The Bot Types Listed Above!

## List

You Can Read Full Api At => [here](DOCS.md).

## Settings For Mirai:

You Need To Go To File Mirai.js, Then Find Line
```js
     var login = require('depend on bot');
     /* Maybe :
         var login = require('@maihuybao/fca-Unofficial');
         var login = require('fca-xuyen-get');
         var login = require('fca-unofficial-force');
     ...
     */
```

And Replace It With:

```js
     var login = require('fca-project-trankhuong')
```

After that, run normally!

## Self-study

If You Want To Research Or Create Your Own Bot, Go To This To Read Its Functions And How To Use => [Link](https://github.com/Schmavery/facebook-chat-api#Unofficial %20Facebook%20Chat%20API)

------------------------------------

### Save Login Information.

To Save, You Need 1 Apstate Type (Cookie, etc,..) To Save Or Use Login Code As Above To Log In!

And this mode is already available in some Vietnamese bots, so you can rest assured!

__Instructions With Appstate__

```js
const fs = require("fs");
const login = require("fca-project-trankhuong");

var credentials = {email: "FB_EMAIL", password: "FB_PASSWORD"}; // account information

login(credentials, (err, api) => {
     if(err) return console.error(err);
     // log in
     fs.writeFileSync('appstate.json', JSON.stringify(api.getAppState(), null,'\t')); //create appstate
});
```

Or Easier (Professional) You Can Use => [c3c-fbstate](https://github.com/c3cbot/c3c-fbstate) To Get Fbstate And Rename It Back To Apstate! (appstate.json)

------------------------------------

## FAQS

FAQS => [Link](https://github.com/Schmavery/facebook-chat-api#FAQS)
