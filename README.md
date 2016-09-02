# Mac Setup

## Shell Commands

~~~shell
# Install Homebrew
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Enable dev mode
sudo /usr/sbin/DevToolsSecurity -enable
sudo /usr/sbin/dseditgroup -o edit -t group -a staff _developer

sudo scutil --set ComputerName "newname"
sudo scutil --set LocalHostName "newname"
sudo scutil --set HostName "newname"

brew update
brew install fish gh git git-lfs wget vim
brew install carthage xctool
brew install ffmpeg gifsicle imagemagick jpegoptim optipng webkit2png potrace
brew install python python3 qt5 rename node postgresql rbenv ruby-build

xcode-select --install

echo "/usr/local/bin/fish" | sudo tee -a /etc/shells
chsh -s /usr/local/bin/fish

brew tap thoughtbot/formulae
brew install rcm

wget -qO- -O tmp.zip https://github.com/kaishin/dotfiles/archive/master.zip
unzip tmp.zip -d ~ > /dev/null 2>&1
rm -rf tmp.zip > /dev/null 2>&1
mv ~/dotfiles-master ~/.dotfiles

rcup -t fish vim osx git ruby

curl -s https://raw.githubusercontent.com/Shougo/neobundle.vim/master/bin/install.sh | sh > /dev/null 2>&1
~~~
