# Sound Sensor and LEDs

This Android Things sample demonstrates how to read data from a sound sensor using an ADC0832 converter and light up some leds lights depending of the sound level

[YouTube Demo](https://youtu.be/uuKKrqXgr54)

## Pre-requisites

- Android Things compatible board
- Android Studio IDEA
- [Rainbow HAT for Android Things](https://shop.pimoroni.com/products/rainbow-hat-for-android-things) or the following individual components: 
    - breadboard
    - 1 sound sensor
    - 3 LEDs
    - 3 resistors
    - 1 ADC0832 converter
   

## Schematics

Schematics for Raspberry Pi 3
<a href="https://ibb.co/cTwvWW1"><img src="https://i.ibb.co/cTwvWW1/microphone-sketch.jpg" alt="microphone-sketch" border="0"></a>

## Build and install

On Android Studio, click on the "Run" button.

If you have everything set up correctly, when receiving data from the sound sensor the leds will behave as follows:
- Green led lights up only if the sound level is low
- Blue led lights up only if the sound level is medium
- Red led lights up only if the sound level is high

## Enable auto-launch behavior

This sample app is currently configured to launch only when deployed from your
development machine. To enable the main activity to launch automatically on boot,
add the following `intent-filter` to the app's manifest file:

```xml
<activity ...>

    <intent-filter>
        <action android:name="android.intent.action.MAIN"/>
        <category android:name="android.intent.category.HOME"/>
        <category android:name="android.intent.category.DEFAULT"/>
    </intent-filter>

</activity>
```

And you will need to give the application some permissions in order to run correctly:
```xml
  <uses-permission android:name="com.google.android.things.permission.MANAGE_INPUT_DRIVERS" />
  <uses-permission android:name="com.google.android.things.permission.USE_PERIPHERAL_IO" />
  <uses-permission android:name="com.google.android.things.permission.MANAGE_BLUETOOTH" />
  <uses-permission android:name="com.google.android.things.permission.MANAGE_SENSOR_DRIVERS" />
```

## License
Copyright 2016 The Android Open Source Project, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
