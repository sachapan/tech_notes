# VIM stuff I usually forget

## Commenting a number of lines.

First, move the cursor to the first char of the first line in block code you want to comment, then type Ctrl + v.

Then vim will go into VISUAL BLOCK mode.

Use j to move the cursor down until you reach the last line of your code block. Then type: Shift + i

Now vim goes to INSERT mode and the cursor is at the first char of the first line. Finally, type # then ESC and the code block is now commented.

### Alternate way I usually choose

Select the lines you'd like to comment out
Then:
`:s/^/# /`
