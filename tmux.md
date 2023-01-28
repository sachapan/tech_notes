# tmux & screen cheat-sheet

Credit to:
[Dayid](http://www.dayid.org/comp/tm.html)

This helped me years ago when I migrated from screen to tmux and I respectfully preserve it here.

## screen and tmux

A comparison of the features (or more-so just a table of notes for accessing some of those features) for GNU screen and BSD-licensed tmux.

The formatting here is simple enough to understand (I would hope). ^ means ctrl+, so ^x is ctrl+x. M- means meta (generally left-alt or escape)+, so M-x is left-alt+x

It should be noted that this is no where near a full feature-set of either group. This - being a cheat-sheet - is just to point out the most very basic features to get you on the road.

Trust the developers and manpage writers more than me. This document is originally from 2009 when tmux was still new - since then both of these programs have had many updates and features added (not all of which have been dutifully noted here).



| Action 	|  tmux    |	screen   |
|---------|----------|-----------|
| start a new session	| tmux OR tmux new OR tmux new-session	| screen |
| re-attach a detached session	|tmux attach OR tmux attach-session	| screen-r |
| re-attach an attached session (detaching it from elsewhere)	| tmux attach -d OR tmux attach-session -d	| screen -dr |
| re-attach an attached session (keeping it attached elsewhere)	| tmux attach OR tmux attach-session	| screen -x |
| detach from currently attached session |	^b d OR ^b :detach	| ^a ^d OR ^a :detach |
| rename-window to newname |	^b , <newname> OR ^b :rename-window <newn>	| ^a A <newname> |
| list windows	| ^b w	| ^a w |
| list windows in chooseable menu |	|	^a " | 
| go to window #	| ^b #	| ^a # |
| go to last-active window	| ^b l	| ^a ^a |
| go to next window	| ^b n	| ^a n |
| go to previous window	| ^b p	| ^a p |
| see keybindings |	^b ? |	^a ? |
| list sessions	| ^b s OR tmux ls OR tmux list-sessions |	screen -ls |
| toggle visual bell	|	| ^a ^g |
| create another window	| ^b c	| ^a c |
| exit current shell/window |	^d	| ^d |
| split window/pane horizontally	| ^b " |	^a S |
| split window/pane vertically	| ^b %	| ^a `|` |
| switch to other pane	| ^b o |	^a <tab> |
| kill the current pane	| ^b x OR (logout/^D) | |	
| collapse the current pane/split (but leave processes running)	| |	^a X |
| cycle location of panes	| ^b ^o | |	
| swap current pane with previous	| ^b { |	|
| swap current pane with next	| ^b } | |	
| show time	| ^b t |	
| show numeric values of panes	| ^b q | |	
| toggle zoom-state of current pane (maximize/return current pane)	| ^b z | |	
| break the current pane out of its window (to form new window)	 | ^b ! | |	
| re-arrange current panels within same window (different layouts)	| ^b [space]	| |
| Kill the current window (and all panes within)	| ^b killw [target-window] | |	

Last Modified: 2017/01/11
URL: http://www.dayid.org/comp/tm.html
