title: Electron Build Commands
---
[Quasar CLI](/guide/quasar-cli.html) makes it incredibly simple to develop or build the final distributables from your source code.

## Developing
```bash
$ quasar dev -m electron

# ..or the longer form:
$ quasar dev --mode electron

# with a specific Quasar theme, for iOS platform:
$ quasar dev -m electron -t ios

# with a specific Quasar theme, for Android platform:
$ quasar dev -m electron -t mat
```

It opens up an Electron window with dev-tools included. You got HMR for the renderer process and changes to main process are also picked up (but the latter restarts the Electron window on each change).

Check how you can tweak Webpack config Object for the Main Process on [Configuring Electron](/guide/electron-configuring-electron.html) page.

## Building for Production
```bash
$ quasar build -m electron

# ..or the longer form:
$ quasar build --mode electron

# with a specific Quasar theme, for iOS platform:
$ quasar build -m electron -t ios

# with a specific Quasar theme, for Android platform:
$ quasar build -m electron -t mat
```

It builds your app for production and then uses electron-packager to pack it into an executable. Check how to configure this on [Configuring Electron](/guide/electron-configuring-electron.html) page.

### A note for non-Windows users
If you want to build for Windows with a custom icon using a non-Windows platform, you must have [wine](https://www.winehq.org/) installed. [More Info](https://github.com/electron-userland/electron-packager#building-windows-apps-from-non-windows-platforms).
