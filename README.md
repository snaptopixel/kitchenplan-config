# Kitchenplan Configuration

This is a Kitchenplan configuration repository. This repository contains all configuration to install and configure our OSX workstations. More information about Kitchenplan and on how to use it can be found in the [Kitchenplan README](https://github.com/kitchenplan/kitchenplan).

1. Open Terminal

1. Install Homebrew  
**Note:** This will prompt to install "XCode Command-line tools" - Do it!  
`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

1. Install Ruby (via Homebrew) 
`brew install ruby`

1. You'll need to update your `PATH` variable so that the new Ruby is used, follow these steps:  
- Launch the "pico" editor `sudo pico /etc/paths`
- Make sure `/usr/local/bin` is at the top of the list use `ctrl+K` to cut and `ctrl+u` to paste.
-  Exit with `ctrl+x` and answer `y` if you want to save the file, then hit `enter`

1. Close Terminal Window and Re-Open (So the changes take effect)

1. Install Kitchenplan  
`gem install kitchenplan`

1. Setup Kitchenplan  
`kitchenplan setup`

1. Answer `y` for config repository and use the following url:  
`https://github.com/lightspeedvt/boilerplate-config.git`

1. "Own" a few directories to prevent permission errors
`sudo chown -R $USER:admin /usr/local /Library/Caches/Homebrew /Applications`

1. Install All The Things!  
**Note:** When the installer gets to "TotalTerminal" you will get an alert with the options to "Cancel" or "Close", you want to cancel, so the installer can finish.
`sudo kitchenplan provision`



