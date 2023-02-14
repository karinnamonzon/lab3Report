# Researching Commands

 ## `grep` command-line options
 Sources: [Grep wikibooks](https://en.wikibooks.org/wiki/Grep)
 [grep geeksforgeeks.org](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
 

The `grep` command is used to search for patterns in files andl directories according to a string that is used with the command. This string specifies the result of the `grep` command. There are different command-line options for `grep`, these examples will be seen using the `written_2/` folder.

---

`grep -o`
Displays only the matched pattern. By default, `grep` usually returns the whole line that has the matched string but the `-o` allows it to only siplay the matched pattern. This is ran using the format: `grep -o "<pattern>" <file_path>` Here is an example of using `grep -o`

Running `$  grep -o "vistas" written_2/travel_guides/berlitz1/*.txt`
![Image](https://github.com/karinnamonzon/lab3Report/blob/main/grepO1.png?raw=true)

Running `$  grep -o "pyramid" written_2/travel_guides/berlitz1/*.txt`
![Image](https://github.com/karinnamonzon/lab3Report/blob/main/grepOpyramid.png?raw=true)

`grep -o` can provide information on the exact file where the pattern is found but does not show whole line. 

---

`grep -rl`
Recursively searches files for a line. The `r` pertains to recursion while the `l` lists the file names. This command is ran using the format; `grep -rl "<pattern>" <file_path>` 

Running `$  grep -rl "vistas" written_2/`
```
$ grep -rl "vistas" written_2/
written_2/travel_guides/berlitz1/IntroDublin.txt
written_2/travel_guides/berlitz1/IntroLakeDistrict.txt
written_2/travel_guides/berlitz1/IntroMadeira.txt
written_2/travel_guides/berlitz1/WhereToIbiza.txt
written_2/travel_guides/berlitz1/WhereToIsrael.txt
written_2/travel_guides/berlitz1/WhereToJerusalem.txt
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt
written_2/travel_guides/berlitz1/WhereToMadeira.txt
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt
```
This first example searches for the given pattern throughput a whole directory and is useful in returning the exact files with the pattern found in them.

Running `$  grep -rl "giraffe" written_2/travel_guides/berlitz2`
```
$ grep -rl "giraffe" written_2/travel_guides/berlitz2
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt
```
This second example searches for the pattern in a specified path `travel_guides/berlitz2` withing the `written_2` directory. 

---

`grep -c`
Outputs the count of the amount of matching lines only. The returned integer is like a count for the number of times the pattern is matched within a file.

`grep -l`
outputs the count of the amount of matching files only
