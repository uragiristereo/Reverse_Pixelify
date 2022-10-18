# Reverse Pixelify
Revert/disable internal spoofing caused by custom ROMs. Some people don't like it when their device recognized as another device in apps.

## Requirements
- [LSPosed](https://github.com/LSPosed/LSPosed) min. API 93
- Supported ROM, see below.

## Supported ROMs
- [Pixel Experience](https://github.com/PixelExperience/frameworks_base/blob/thirteen/core/java/com/android/internal/util/custom/PixelPropsUtils.java)
- [Evolution X](https://github.com/Evolution-X/frameworks_base/blob/tiramisu/core/java/com/android/internal/util/evolution/PixelPropsUtils.java)
- [CrDroidAndroid](https://github.com/crdroidandroid/android_frameworks_base/blob/13.0/core/java/com/android/internal/util/crdroid/PixelPropsUtils.java)

## Installation
1. Install the module APK (available from [Releases](https://github.com/uragiristereo/Reverse_Pixelify/releases) page).
2. Open `LSPosed Manager`, and enable the module.
3. Choose apps that you want to disable the spoofing, or leave it default.
> You can also add another app that isn't marked as recommended.
4. Reboot the device.
5. Enjoy!
> You may need to clear some apps' data like **Google Photos** or **Play Store** after enabling to takes effect.

## How does this module works?
This module basically hooks `setProps` method in `PixelPropsUtils` class and prevents it to be called by returning `null` prematurely.

## License
    Copyright 2022 Agung Watanabe

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
