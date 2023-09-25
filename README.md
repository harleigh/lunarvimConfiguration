# lunarvim Bits
bits regarding LunarVim and my cobbled together customizations, as well as generic vanilla vim; all of this jazz is playing in windows 10.


## Windows:
* Resizing Windows: In normal mode hold ctrl and hit arrow keys left/right

## Tabs:
* Shift h and l (<S-h>, <S-l>) lets us toggle between buffer (tabs)

## Terminals:
* Alt 1, 2, 3 for various types of terminals (horizontal, vertical, float)
* We can loose focus in the terminal (e.g. after pasting with mouse), we gain terminal back by going into
insert mode (i)
* A *beutiful* toggled terminal with <C-\> 

## Markdown:
* glow is a simple no nonsense markdown viewer done in-terminal, without any messing about with plugin. All
that is required is a call on the terminal 'glow'. So, all of the markdown can be done entirely in LunarVim.

## React JSX:
* nvim-ts-autotag is a must; beautiful autocompletion of tags just like in vscode.

## Searching (and replacing):
* The lot in the current file (which is '%') :%s/{search}/{replace}/g
* To get confirmation on each search and replace: %s/{search}/{replace}/gc
* Stop highlighting your last search (but allow highlighting in the future), we enter ":noh",
 or have a binding of [noremap <silent> <c-_> :let @/ = ""<CR>]  (brackets to group), or [nnoremap / :let @/=""<CR>/] which
will clear the highlight by hitting '/' agian
* great resource: https://vim.fandom.com/wiki/Search_and_replace



## Cut-Off itallic letters?

Example of the issue of cut-off letters:
![image](https://github.com/harleigh/lunarvimConfiguration/assets/4912070/0b0c3550-65db-4899-bd12-6175a7b7ab3d)

What we want:
![image](https://github.com/harleigh/lunarvimConfiguration/assets/4912070/c3355998-8427-4e2f-8490-78b9761fc04d)

Resolution:
* This is a terminal issue; we need to install a nerd-font that has support for itallics
* Head to https://www.nerdfonts.com/font-downloads
* Get a font that has itallics support (e.g. hacker) i.e. download its .zip. How do you know if your font supports itallics? When extracted you will see an itallics verion of the font. For example compare 'hacker' vs 'Aurulent' (the Aurulent, when extracted, does not have an itallics version) 
* Extract and Install *all* of the nerd-font (for *all* users)
* In your terminal, set the font to your itallics-supported font (e.g. Hack Nerd Font)
* Load your file and check to see if the cut-off letters has been resolved.
