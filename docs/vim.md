# VIM stuff I usually forget

## Commenting a number of lines.

### There's a [vim plugin](https://github.com/junegunn/vim-plug) for that....

[vim commentary](https://github.com/tpope/vim-commentary)


### The Old ways

First, move the cursor to the first char of the first line in block code you want to comment, then type Ctrl + v.

Then vim will go into VISUAL BLOCK mode.

Use j to move the cursor down until you reach the last line of your code block. Then type: Shift + i

Now vim goes to INSERT mode and the cursor is at the first char of the first line. Finally, type # then ESC and the code block is now commented.

### Alternate way I used to use

Select the lines you'd like to comment out
Then:
`:s/^/# /`

## neovim

### Install on debian based distro because the package maintainers don't seem to include virsion .9

curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim.appimage
chmod u+x nvim.appimage
./nvim.appimage

./nvim.appimage --appimage-extract
./squashfs-root/AppRun --version

# Optional: exposing nvim globally.
sudo mv squashfs-root /
sudo ln -s /squashfs-root/AppRun /usr/bin/nvim
nvim
