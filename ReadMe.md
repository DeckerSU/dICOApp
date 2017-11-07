# dICO App

Before starting make sure you have `marketmaker` daemon compiled and running on your machine.

You can find instructions to install `marketmaker` here:

https://github.com/SuperNETorg/komodo/wiki/Setting-up-Liquidity-Provider-(LP)-Node#installing-liquidity-provider-lp-node-on-ubuntudebian-system

### Setup
Once running, follow these steps:
```shell
git clone https://github.com/SuperNETorg/dICOApp.git
cd dICOApp
npm install
npm start
```

It will download "dICOApp". Open "dICOApp", and from there open "index.html" file in your web browser.

### Update
To update, follow these steps:
```shell
cd dICOApp
git pull
```

#### For end users

To build the production ready app, install `electron-packager` and `electron-prebuilt` packages from npm
```shell
sudo npm install electron-packager -g
sudo npm install electron-prebuilt -g
```

#### **Build the App**
Refer to the original [electron-packager](https://github.com/electron-userland/electron-packager) repository for more detailed information.

##### Linux
Change directory to dICOApp and execute the following command to build the Linux app
```shell
cd dICOApp
electron-packager . --platform=linux --arch=x64 --out=build/ --buildVersion=VERSION_NUMBER_HERE --ignore=assets/bin/win64 --ignore=assets/bin/osx --overwrite
```
change architecture build parameter to ```--arch=x32``` for 32 bit build

##### OSX
Change directory to dICOApp and execute the following command to build the OSX app
```shell
cd dICOApp
electron-packager . --platform=darwin --arch=x64 --out=build/ --buildVersion=VERSION_NUMBER_HERE --ignore=assets/bin/win64 --ignore=assets/bin/linux64 --overwrite
```

