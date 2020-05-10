# Native Titanium Swift Modules

This is an example project that uses pure Swift modules in Titanium. Both the module
and it's dependencies are 100 % Swift and do not require any additional setup / linking
anymore. This is a slightly modified, updated version of https://github.com/hansemannn/titanium-swift-module-example,
with `Alamofire` removed.

## What do I need to change?

There are a couple of things that you'll need to change in this project in order to get it to work for you.

### manifest

* You may want to change the version 
* If your XCode project targets specific architectures, you'll need to update the architectures.
* Description, author, licence and copyright should be updated so that they're relative to your project.
* name, moduleid, guid, platform and minsdk should also be updated to suit your project.

### titanium.xcconfig

* Update `TITANIUM_SDK_VERSION` to the version you're targeting.
* Update `TITANIUM_SDK` to reflect your own titanium installation path.

## How do I build this?

* First open the xcodeproj file and try building in XCode with `Command + B`. I suggest doing this first since XCode may give you more context in case you do encounter any build errors.
* Open a terminal at `<module_directory>/ios` and run `appc run -p ios --build-only`. This will produce a `build` folder if it's not already there, and place a .zip inside a `dist` folder. 
* Double-click the .zip and copy the resulting `<module-name>` folder into the `/modules` folder of your project. If replacing an existing version of the same module, you'll want to run `appc ti clean` in your project before running it.
* If you do encounter errors while building this module with appc (but XCode builds fine), try running `appc ti clean` within the ios folder.

## License

MIT

## Authors

Jason Sultana
Hans Knöchel