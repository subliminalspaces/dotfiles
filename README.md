Installation Instructions

Clone this repo. Be sure to recurse.
```
git clone https://github.com/subliminalspaces/dotfiles --recurse-submodules
```
The aconfmgr configs are private for security reasons. I will be adding some minimum configs for just these dotfiles soon.

After cloning this repo down, you should be able to
Otherwise, you would be able to.
```
cd ~/.config/aconfmgr/
sh aconfmgr apply
```


Be sure to download and add alacritty's terminfo.

```
wget https://raw.githubusercontent.com/alacritty/alacritty/master/extra/alacritty.info
sudo tic -xe alacritty, alacritty-direct, alacritty.info
infocmp alacritty
```

nvm should be installed. So install node.

```
nvm install --lts
```

Install the dependencies for lsp.

```
npm install -g typescript typescript-language-server
npm install -g vscode-langservers-extracted
```


Be sure to copy .zshenv.bak to .zshenv and give those variables the right values
oh-my-zsh is submoduled for convience.
Be sure to copy .zshenv.root.bak to home directory as .zshenv
```
cd .zshenv.bak .zshenv
cd .zshenv.root.bak ~/.zshenv
```
then you can

```
chsh -s /usr/bin/zsh
```
Install polybar

Necessary dependencies are:
```
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
```

then install vimpc

```
yay -Syu vimpc-git
```

Then install polybar.

```
git clone --recursive https://github.com/polybar/polybar
cd polybar
mkdir build
cmake ..
make -j$(nproc)
#if you get a memory time out
#make -j 1
sudo make install
```

Now run arandr to configure monitor layout.

Configure polybar, configure feh.
And configure wireplumber.

There's going to be issues right now so use at your own risk.

