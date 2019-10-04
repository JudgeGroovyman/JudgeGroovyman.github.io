# React Native
How I installed it and ran it:
* Install [npm](https://www.npmjs.com)
* `npm install -g create-react-native-app`
* `sudo chown -R $(whoami) /usr/local/lib/node_modules`
* `npm install -g create-react-native-app`
* `cd ~/Sites`
* `create-react-native-app tipcalc`
* Follow instructions to install Expo CLI, and select expo-template-tabs
* `cd tipcalc`
* `npm start`
    * That brought up a browser simulator.
* (in another window)
* `xcode-select --install`
    * (xcode has to be installed first)
* (back in the first window)
* Ctrl-c
* `npm run ios`

I dragged the whole folder onto textmate
then while the ios simulator is visible, 
in `screens/HomeScreen.js` I copied line 38 which said "Get started by opening" and changed the copy to "Hello, World!"

Hot reload worked perfectly!


