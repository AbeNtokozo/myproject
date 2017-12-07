# InstaDrive+ Terminal Frontend
React Native Project for Terminal app
## Development Setup

Install javascript dependencies:

    $ npm install

Install Objective C dependency manager:

    $ sudo gem install cocoapods

Install Objective C dependencies:

    $ cd ios
    $ pod install
    $ cd ..

Start react-native:

    $ react-native run-ios --simulator="iPad Air 2"

If the compilation fails, run XCode and try to compile within the IDE:

    $ cd ios
    $ open InstaDRIVETerminal.xcworkspace

## Configuration

The map area and destinations can be tweaked in the `config.js` file.

## Deployment

Some words about naming:

* _Distribution:_ Release (code-optimized) build signed with an iOS Distribution certificate.
* _Development:_ Debug (non-optimized) build signed with an iOS Developer certificate.
* _Deploy_ = build + publish the app.

To create a __full distribution build of the app (native and JS code) and publish it to all channels__ (currently [HockeyApp][hockeyapp] and [CodePush][codepush]), simply use the command:

```
npm run deploy
```

You can also ship an updated JS bundle via CodePush without distributing a new binary. The app will refresh at launch (so you might need to kill it first), assuming a working internet connection. To do this, use:

```
npm run deploy:bundle
```

If you want to just generate the signed IPA file on your local machine, use

```
npm run build:distribution
```

or

```
npm run build:development
```

depending on your needs.

[hockeyapp]: https://hockeyapp.net/
[codepush]: https://microsoft.github.io/code-push/
