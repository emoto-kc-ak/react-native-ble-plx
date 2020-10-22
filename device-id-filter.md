# device-id-filter branch

This fork introduces a new option to filter BLE device by device IDs for Bluetooth LE scan; i.e., MAC addresses on Android, UUIDs on iOS.

The `options` argument of the function `BleManager#startDeviceScan` can take the following new option,
- `filteredDeviceIds`: `Array<DeviceId>`

Programs written for the original version should work with this fork.

## Building outside a react native project

This module is usually built in a context of a react native project.

To build this module outside a react native project, you have to resolve the [Android Annotation](https://developer.android.com/jetpack/androidx/releases/annotation) library.
Add the following line to [`android/build.gradle`](./android/build.gradle) to resolve it.

```
dependencies {
    implementation "androidx.annotation:annotation:1.1.0"
}
```