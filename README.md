## Terminal Commands

In the words of the great Willie Wonka:

>A little nonsense now and then is relished by the wisest men.

A collection of useful terminal commands:

```bash
// remove all node_modules from a folder
for package in `ls node_modules`; do npm uninstall $package; done;

// Keep mac awake until app is idle
caffeinate -i open -W -a iMovie.app

// Show hidden files (FALSE to hide)
defaults write com.apple.finder AppleShowAllFiles TRUE

// Create textfile of directory and all sub-directories (use .csv to maked a CSV)
ls -R /DIRECTORY > file-name.txt

// Find the PID running on port 3000
lsof -wni tcp:3000
//kill that process
kill -9 PID

// Compress Image using Imagemagick
convert -strip -interlace Plane -quality 85% source.jpg result.jpg

// Compress all subdirectories into their own .zip
for i in */; do zip -r "${i%/}.zip" "$i"; done

// Restart Wireless Networking (use en0 for Ethernet)
As Sudo:
ifconfig en1 down
ifconfig en1 up

// Convert ISO to DMG
hdiutil convert /path/imagefile.iso -format UDRW -o /path/convertedimage.dmg

// Restart OS X UI
sudo killall -HUP WindowServer

// Homebrew-cask commands
brew cask install google-chrome
brew cask install google-chrome-canary
brew cask install firefox
brew cask install firefox-nightly
brew cask install atom
```

