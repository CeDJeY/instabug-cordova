Cordova Instabug Plugin
=================================

The purpose of this plugin is to simplify the process of integrating the Instabug SDK in a hybrid application, as well as to provide an interface to interfacing with the SDK through JavaScript.


### Installation
Currently, this plugin can only be installed via the Command-Line Interface.
```
cordova plugin add https://github.com/CeDJeY/instabug-cordova 
```

## Usage
To initialize Instabug in your app, you need to do the following: 
```
cordova.plugins.instabug.activate(
    {
        ios: 'MY_IOS_TOKEN',
        android: 'MY_ANDROID_TOKEN'
    },
    'shake',
    function () {
        console.log('Instabug initialized.');
    },
    function (error) {
        console.log('Instabug could not be initialized - ' + error);
    }
);
```
 You can change the invocation event with any of the following: ```'button'```, ```'screenshot'```, ```'swipe'```, or ```'shake'```.

