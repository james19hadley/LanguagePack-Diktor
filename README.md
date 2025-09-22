## Diktor Language Pack (fork)

This repository is an unofficial fork of AnySoftKeyboard/LanguagePack (Apache-2.0),
trimmed down to a single add-on: the Diktor Russian layout pack.

- Upstream (deprecated mono-repo): https://github.com/AnySoftKeyboard/LanguagePack
- Main project: https://github.com/AnySoftKeyboard/AnySoftKeyboard (addons/languages)

### What’s included
- `api` and `base` libraries from ASK add-on SDK
- `languages/diktor`: Diktor pack (pack + apk)
- Optional: `languages/english` may exist locally as a reference, but only Diktor participates in the build.

### Build
- Debug APK:
```
./gradlew :languages:diktor:apk:assembleDebug
```
Result APK will also be copied to `add_ons_apks/debug/`.

- Release APK: configure signing (do not commit keystores)
  - Optionally set a unique applicationId in `languages/diktor/apk/build.gradle`:
    `ext.override_app_id = "com.yourorg.ask.languagepack.diktor"`

### Credits & License
- Original authors: AnySoftKeyboard contributors (Apache License 2.0)
- This fork modernizes the build and provides Diktor-specific layouts and resources.

```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
