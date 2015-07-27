# Bootstrap Your Mac

This is a Kitchenplan configuration repository. This repository contains all configuration to install and configure OSX workstations. More information about Kitchenplan and on how to use it can be found in the [Kitchenplan README](https://github.com/kitchenplan/kitchenplan).

## Customizing Your Setup

If you look in the people directory, you'll see some "YAML" config files for different users. These must match your OSX username (typically the name of your "Home" folder). You can add one for yourself or edit an existing one if you'd like.

The easiest way to get it going is to look at the existing files, especially "snaptopixel" since it is the most customized.

Once you've got it configured to your liking, follow the steps below.

## Setup and Install Directions

1. Open Terminal (Hit Cmd+Space, type Terminal then ENTER)

1. Install Homebrew  
**Note:** This will prompt to install "XCode Command-line tools" - Do it!  
`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

1. Install Ruby (via Homebrew)  
`brew install ruby`

1. You'll need to update your `PATH` variable so that the new Ruby is used, follow these steps:  
    - Launch the "pico" editor `sudo pico /etc/paths`  
    - Make sure `/usr/local/bin` is at the top of the list use `ctrl+K` to cut and `ctrl+u` to paste.  
    - Exit with `ctrl+x` and answer `y` if you want to save the file, then hit `enter`

1. Close Terminal Window and Re-Open (So the changes take effect)

1. Install Kitchenplan  
`gem install kitchenplan`

1. Setup Kitchenplan  
`kitchenplan setup`

1. Answer `y` for config repository and use the following url:  
`https://github.com/snaptopixel/kitchenplan-config.git`

1. "Own" a few directories to prevent permission errors  
`sudo chown -R $USER:admin /usr/local /Library/Caches/Homebrew /Applications`

1. Install All The Things!  
**Note:** When the installer gets to "TotalTerminal" you will get an alert with the options to "Cancel" or "Close", you want to cancel, so the installer can finish.  
`sudo kitchenplan provision`

1. Install SASS  
Unfortunately, there is currently a bug preventing the auto-install of the SASS Preprocessor. Just issue one last command in the terminal to install it:  
`gem install sass`

## Totally Random OSX Stuff That I Don't Have A Place For

### Mail.app :heart: Gmail Accounts
I really wanted to use Mail.app with my Gmail accounts, but it can be tricky. The following things helped me get it set up pretty nicely:

- Any Gmail labels with a `/` in them will cause Mail.app to eat cpu, spin up fans and basically go bonkers. Quit Mail.app, rename them in Gmail's web interface and reopen mail.

- Create filters using Gmail's oh-so-nice auto-categorization and use labels to get them in your Mail.app. Enter in the "Has the words" field `category:` then the name of the category in lowercase, ie: `category:forums` then "Skip the Inbox" and add a label, something like "Gmail - Forums".

- Go to the "Labels" tab in Gmail's settings and turn off "Show in IMAP" for everything but the essential stuff. If nothing else make sure you turn off "All Mail" "Spam" and "Trash"

- Open Mailbox.app preferences, go to the Accounts tab and for each account, click "Mailbox Behaviors" and uncheck everything but the "Drafts" option.
