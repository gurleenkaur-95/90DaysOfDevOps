# File IO Practice

- Below lines are output from terminal

this is line 1
this is line 2
this is line 3
this is line 4, just to check again the tee command
line 5 added in vim


- Explanation time :
to create a file - `touch file-io-practice.md`
to add line 1 - `echo "this is line 1" > file-io-practice.md`
to add line 2 - `echo "this is line 2" >> file-io-practice.md`
to add line 3 - `echo "this is line 3" | tee -a file-io-practice.md`
to add line 4 - `echo "this is line 4, just to check again the tee command" | tee -a file-io-practice.md`
to add line 5 - `vim file-io-practice.md` and start insert mode with `I` and write `line 5 added in vim` then to exit `esc + :wq`


`|` - pipe operator - passes output to next command
`tee` command will show the output in the terminal on execute (without cat) 
`-a` ia for append (otherwise it will overwrite)

also practiced 
`head -n 2 file-io-practice.md` - shows the first two lines of the file
`tail -n 2 file-io-practice.md` - shows the last two lines of the file