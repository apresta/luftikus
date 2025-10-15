# lkjb Luftikus Audio Plugin

This repository contains an updated version of the Luftikus plugin by lkjb, updated to build with newer versions of JUCE and produce an Apple Silicon-compatible plugin.

The build process was tested on macOS 15.7.1 with Xcode 26.0.1 and JUCE 8.0.10.

Prebuilt AU and VST3 plugins are available in the [Releases](https://github.com/apresta/luftikus/releases/latest) section. Please note that you will likely need to code-sign the plugins before you can run them:

```sh
sudo codesign -s - /Library/Audio/Plug-Ins/VST3/lkjb_Luftikus.vst3/Contents/MacOS/lkjb_Luftikus --timestamp --deep --force
sudo xattr -rd com.apple.quarantine /Library/Audio/Plug-Ins/VST3/lkjb_Luftikus.vst3

sudo codesign -s - /Library/Audio/Plug-Ins/Components/lkjb_Luftikus.component/Contents/MacOS/lkjb_Luftikus --timestamp --deep --force
sudo xattr -rd com.apple.quarantine /Library/Audio/Plug-Ins/Components/lkjb_Luftikus.component
```


# License
JUCE is licensed under the GPL v3 or a commercial license. See juce.com for more details.
The lkjb part of the code is now licensed under the MIT license. Feel free to use the code in other products or create (hopefully freeware) plugins.
