# openxcom-ios
A repository to house everything that's needed to build OpenXcom for iOS

## Getting the Projects
Some of the projects (including OpenXcom) are added via submodules. In order to retrieve them, you have to instruct `git` to
get them along with the rest of the repository. The easiest way to do that is to just clone the repository recursively:

    $ git clone --recursive https://github.com/sfalexrog/openxcom-ios

If your git client doesn't support recursive cloning, you can clone the repository and then initialize the submodules manually:

    $ git clone https://github.com/sfalexrog/openxcom-ios
    $ cd openxcom-ios
    $ git submodule update --init --recursive
    
## Building OpenXcom
Go to `Sources/OpenXcom/xcode-ios` and open the `OpenXcom.xcodeproj` project file. This should open your Xcode, with
all subprojects and resources in place. Be sure to configure your signing certificate before running on a real device!

You may want to place your *X-Com: UFO Defense* and/or *Terror from the Deep* files into `Sources/OpenXcom/bin/UFO` and
`Sources/OpenXcom/bin/TFTD` folders respectively. This will copy the game data into the app bundle, which will allow you
to run OpenXcom a lot more easily. Note though that this *will make the app bundle non-redistributable*! Not that there's
a way to redistribute an app outside of an app store, though.

You may also want to place translations into `Sources/OpenXcom/bin/common/Language`,
`Sources/OpenXcom/bin/standard/xcom1/Language` and `Sources/OpenXcom/bin/standard/xcom2/Language`. You can get the translations
from a nightly version of OpenXcom for Windows or from the OpenXcom Transifex (if you have it set up).

## Running OpenXcom on iOS
If you copied your *UFO Defense*/*TFTD* files into the bundle during the build phase, that's probably everything you'd want.
If not, you'll be greeted with an error message upon running the app. This means you'll have to use iTunes to get the data
to the app: you'll have to copy your `UFO` and/or `TFTD` folder from a working installation of OpenXcom.

Saved games are in the xcom1 and xcom2 folders that you can access through iTunes. They should be compatible with the desktop
versions

Mods can also be uploaded through iTunes.

## Acknowledgements
Thanks to SupSuper, Warboy1982 and all other OpenXcom authors and contributors for making a perfect recreation of the X-Com
Experience!

Thanks to Ryan C.Gordon, Sam Lantinga and all other SDL authors and contributors for making THE best cross-platform multimedia
library! They make the "write once, run anywhere" dream come true.

Thanks to everyone on #OpenXcom IRC for their kind words, support and bug reports! Sorry for not paying much attention lately,
I'll get back to the Android version, I promise!

Last but not least, thanks to the person who convinced me to do this thing in the first place! You know who you are :-)
