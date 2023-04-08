Installation Instructions

After cloning this repo down, you should be able to
cd ~/.config/aconfmgr/
sh aconfmgr apply



Be sure to download and add alacritty's terminfo.

wget https://raw.githubusercontent.com/alacritty/alacritty/master/extra/alacritty.info
sudo tic -xe alacritty, alacritty-direct, alacritty.info
infocmp alacritty

nvm should be installed. So install node.
nvm install --lts

Install the dependencies for lsp.
npm install -g typescript typescript-language-server
npm install -g vscode-langservers-extracted



Be sure to copy .zshenv.bak to .zshenvr and give those variables the right values
install oh-my-zsh.
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

then you can

chsh -s /usr/bin/zsh

Install polybar

Necessary dependencies are:
pkg-config
libuv
cairo
libxcd
xcb-proto xcb-util-image
xcb-util-wm
python-sphinx
python-packaging
xcb-util-cursor
xcb-util-xrm
xcb-xkb
alsa-lib
libpulse
i3-wm 
mpd
libmpdclient(should be installed as mpd dependency)
curl(should be installed already)
wireless_tools
sphinx
clang

then install vimpc
yay -Syu vimpc-git
then git clone --recursive https://github.com/polybar/polybar
cd polybar
mkdir build
cmake ..
make -j$(nproc)
#if you get a memory time out
#make -j 1
sudo make install

Now run arandr to configure monitor layout.

Configure polybar, configure feh.
And configure wireplumber.


