# wifi_configuration

A new Flutter plugin.

## Getting Started

This plugin allows Flutter apps to get available wifi ssid list,
user can connect to wifi with ssid and password.
This plugin works Android.
iOS will be released later.


Sample usage to check current status:



Note :-   This plugin requires the location permission to auto enable the wifi if android version is above 9.0.


For Android : -
Add below Permissions to your manifist.xml file -
```dart
    <uses-permission android:name="android.permission.CHANGE_WIFI_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    <uses-feature android:name="android.hardware.wifi" />
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```



```dart
  import 'package:wifi_configuration/wifi_configuration.dart';

  var listAvailableWifi = await WifiConfiguration.getWifiList();
  //If wifi is available then device will get connected

  bool connectionState = await WifiConfiguration.connectToWifi("Wifi ssid", "Wifi Pass");
  //This will return a boolean value
```



When you use connection on iOS (iOS 11 only)

1. 'build Phass' -> 'Link Binay With Libraries' add 'NetworkExtension.framework'
    ![NetworkExtension](https://github.com/once10301/wifi/blob/master/png/NetworkExtension.png)

2. in 'Capabilities' open 'Hotspot Configuration'

    ![NetworkExtension](https://github.com/once10301/wifi/blob/master/png/Hotspot%20Configuration.png)

3. If you device is iOS12, in 'Capabilities' open 'Access WiFi Information'

    ![NetworkExtension](https://github.com/once10301/wifi/blob/master/png/Access%20WiFi%20Information.png)

If you want to use Wifi.list on iOS,



For help getting started with Flutter, view our 
[online documentation](https://flutter.dev/docs), which offers tutorials, 
samples, guidance on mobile development, and a full API reference.
