To run bitbout as a native app, follow Electron's Quick Start guide at:
http://electron.atom.io/docs/latest/tutorial/quick-start/

For example, save the Electron binary from [its release package](https://github.com/electron/electron/releases) to OS X's Application directory. In Terminal, navigate to node_modules/bitbout in your bitbout-native directory and run the following commands:

`npm install`

`npm run build`

Then navigate to your bitbout-native directory and run the following commands:

`npm install`

`/Applications/Electron.app/Contents/MacOS/Electron ./`

**NOTE: You must edit node_modules/bitbout/scripts/vendor/libopenmpt.js:**
**FROM** `var memoryInitializer="./scripts/vendor/libopenmpt.js.mem";`
**TO** `var memoryInitializer=require("path").join(__dirname, "/scripts/vendor/libopenmpt.js.mem");`