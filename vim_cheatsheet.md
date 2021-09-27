# Vim Cheatsheet

### Moving Cursor:

	    h   : Left
	    j   : Down
	    k   : Up
	    l   : Right
	    j$  : End of below line
### Delete:

	    x   : current character
	    dw  : current word
	    de  : to end of current word
	    d$  : to end of current line
	    dd  : delete whole line 
**Note:** d is the operator, the following characters are motion. Motions can be repeated. 
### Motion: 

	    w   : current word
	    e   : end of word
	    $   : end of line	
### Repeation:

	    2w  : moves cursor two words forward
	    3e  : moves cursor to end of three words forward 
	    0   : start of line
	    d2w : deletes two words 
	    2dd : deletes two lines 
### Modes:
	    i   : insert mode
	    a   : append mode
### Undo: 

	    u       : undo last command
	    U       : undo whole line
	    Ctrl+R  : redo
### Put:

	    p   : put previously deleted text after cursor
### Replace: 

	    rx  : replace current character with x
	    R   : replace mode, more than one character
### Change:

	    ce  : change until the end of word (deletes word and places in Insert mode)
	    c$  : until end of line
	    cw  : change current word
	    c2w : change 2 words -> c [number] motion
### Cursor Location & File Status

	    Ctrl + g: Location and file status
	    G       : Bottom of file
	    gg      : start of file
### Search:
	    /<phrase>   : search phrase
	    n           : next one
	    N           : opposite dir
	    ?<phrase>   : for searching backward direction
	    Ctrl + O    : Go back where you came 
	    Ctrl + I    : Go Forward
### Matching parantheses
	    %   : find a matching ),},]
### Substitute

	    :s/old/new/  	: in current line
	    :s/old/new/g 	: globally
	    :#,#s/old/new/g : btw line numbers #, #
	    :%s/old/new/gc  : with a prompt whether substitute or not 

### External commands
	    :!<command>	: execute shell command

### Write 
	    :w <filename> 

### Visual 
	     v   : visual selection (type v and select text then press : and save it with w <filename> ) 	 	 	

### Retrieving or merging files

	    :r <filename>   : retrieves files to cursor position
	    :r !<command>   : retrieve the output of command

### Open 

	    o   : open a line below the cursor and place you in Insert mode.
	    O   : a line above
### Append 
    	a   : append mode, after cursor
        A   : insert text after the end of the line.

**NOTE:**  a, i and A all go to the same Insert mode, the only difference is where
       the characters are inserted.	

### Copy and Paste

    	y   : copy 
        p   : paste

**NOTE:** you can also use  y  as an operator;  yw  yanks one word.

### Set option

	    :set ic		: set ignore case
	    :set hls	: hlsearch
	    :set is 	: incsearch - shows multiple matches
	    :set hls is : hlsearch & incsearch
	    :set noic	: disable ignorecase
	    :nohlsearch : removes highlight
	    /<phrase>/c : ignore case for just one search command

## Help
	    :help
	    :help w
	    :help user-manual
	    :help insert-index

### Completion
	    :<operator> Ctrl+D