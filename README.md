# cordova_is_simulator_plugin_demo
cordova device plugin which provide is_simulator for iOS &amp; Android

since is_simulator pr for cordava-plugin-device is not merged yet,
we should reinstall the plugin:

``` sh
$ cordova plugin remove cordava-plugin-device
$ cordova plugin add https://github.com/AndyChenW/cordova-plugin-device
```

then in the project you can use device.is_simulator as:

``` javascript
alert("is simulator: " + device.is_simulator);
```

note that we should make sure that the device is ready as in the demo:
index.js and index.html
``` javascript
document.addEventListener("deviceready", onDeviceReady, false);
function onDeviceReady() {
  alert("is simulator: " + device.is_simulator);
}
```
