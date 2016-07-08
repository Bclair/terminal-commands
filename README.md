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

// Generate a gif from a mov with ffmpeg
ffmpeg -i video.mov -pix_fmt rgb24 output.gif

// Reduce the frame rate and size. Set the start time and duration
ffmpeg -ss 00:00:00.000 -i video.mov -pix_fmt rgb24 -r 10 -s 320x240 -t 00:00:10.000 output.gif

// Optimize gif with ImageMagick
convert -layers Optimize output.gif output_optimized.gif

// Optimize gif with gifsicle
gifsicle -O3 output.gif -o ouptput-optimized.gif

// Install brew-cask
brew install caskroom/cask/brew-cask

// Install alternate versions tap
brew tap caskroom/versions

// Install necessary apps
brew cask install google-chrome
brew cask install google-chrome-canary
brew cask install firefox
brew cask install firefox-nightly
brew cask install atom
brew cask install keepingyouawake
brew cask install mamp
```

