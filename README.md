# Kitchenplan Configuration

This is a Kitchenplan configuration repository. This repository contains all configuration to install and configure our OSX workstations. More information about Kitchenplan and on how to use it can be found in the [Kitchenplan README](https://github.com/kitchenplan/kitchenplan).

1. Install Homebrew  
`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

1. Install Ruby (via Homebrew)  
`brew install ruby`

1. Close Terminal Window and Re-Open (So the new Ruby takes effect)

1. Install Kitchenplan  
`gem install kitchenplan`

1. Setup Kitchenplan  
`kitchenplan setup`

1. Answer `y` for config repository and use the following url:  
`https://github.com/lightspeedvt/boilerplate-config.git`

1. Install All The Things!  
`kitchenplan provision`



