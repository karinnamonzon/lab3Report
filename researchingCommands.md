# Researching Commands

 ## `grep` command-line options
 Sources: [Grep wikibooks](https://en.wikibooks.org/wiki/Grep)
 [grep geeksforgeeks.org](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
 

The `grep` command is used to search for patterns in files andl directories according to a string that is used with the command. This string specifies the result of the `grep` command. There are different command-line options for `grep`, these examples will be seen using the `written_2/` folder.

`grep -o`
Displays only the matched pattern. By default, `grep` usually returns the whole line that has the matched string but the `-o` allows it to only siplay the mathed pattern. Here is an example of using `grep -o`

Running `$  grep -o "vistas" written_2/travel_guides/berlitz1/*.txt`
![Image](https://github.com/karinnamonzon/lab3Report/blob/main/grepO1.png?raw=true)

Running `$  grep -o "pyramid" written_2/travel_guides/berlitz1/*.txt`
![Image](https://github.com/karinnamonzon/lab3Report/blob/main/grepOpyramid.png?raw=true)

`grep -o` can provide information on the exact file where the pattern is found but does not show whole line.

---

`grep -v`
returns everything but the path contianing the string

`grep -c`
outputs the count of the amount of matching lines only

`grep -l`
outputs the count of the amount of matching files only
