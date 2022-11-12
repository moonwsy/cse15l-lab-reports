# Lab report4

**Part1**

- Demo: Changing the name of the start parameter and its uses to base

step 1:
- vim DocSearchServer.java, then press enter. 
- Goal: To enter the file then we're in the normal mode.

> ![](vim-start.png)

step 2:
- /start, then press enter.
- Goal: To search the word that we want to change, syntax is / + searchword, the cursor postition is the first character of the searchword
> ![](vim-p1-1.png)

step 3:
- dw
- Goal: delete the characters of the word from the cursor position to the start of the next word
> ![](vim-dw.png)

step 4:
- i then tap base,  then press esc
- Goal: go to the insert mode add new word 'base' after the 'Path', then leave insert mode to normal mode
> ![](vim-i+base.png)

step 5:
- n
- Goal: repeats the last search from the cursor's position down
> ![](vim-n.png)

step 6:
- dw
- Goal: delete the characters of the word from the cursor position to the start of the next word
> ![](vim-dw-2.png)

step 7:
- i then tap base,  then press esc
- Goal: go to the insert mode add new word 'base' after the '= ', then leave insert mode to normal mode
> ![](vim-i+base2.png)

step 8:
- n
- Goal: repeats the last search from the cursor's position down
> ![](vim-n2.png)

step 9:
- dw
- Goal: delete the characters of the word from the cursor position to the start of the next word
> ![](vim-dw3.png)

step 10:
- i then tap base,  then press esc
- Goal: go to the insert mode add new word 'base' after the '(', then leave insert mode to normal mode
> ![](vim-i+base3.png)

step 11:
- :wq
- Goal: save and quit
> ![](vim-wq.png)
> ![](vim-save.png)

step:  vim DocSearchServer.java -> /start -> dw -> i -> base -> esc -> n -> dw -> i -> base -> esc -> n -> dw -> i -> base -> esc -> :wq -> enter


**Part2**