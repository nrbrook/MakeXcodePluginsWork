## What is this?

This is a bash script that can unsign the Xcode binary and update the Xcode compatibility UUID in plugins.

Xcode disabled plugins in Xcode 8 in favour of its extensions API. Unfortunately this is very limited at this point. Unsigning Xcode allows plugins to run again.

Also, each version of Xcode has it's own UUID which needs to be listed inside the plugin to ensure compatibility. It seems lots of plugins work just fine with Xcode 8, but authors are unlikely to update them with the new UUID as Xcode stops them loading. This script can also add in that UUID.

*Use at your own risk.* Although a copy of the binary is left inside your Xcode.app at `Xcode.app/Contents/MacOS/Xcode.signed`, you are using this at your own risk. I've tested it, it works for me. Your results may vary.

Uses the unsign project at [https://github.com/steakknife/unsign](https://github.com/steakknife/unsign)

This doesn't fix the problem long term! If you like plugins, Be sure to file a radar at [https://bugreport.apple.com/](https://bugreport.apple.com/)

## Installation

Clone this repo or just download the script, then run it
