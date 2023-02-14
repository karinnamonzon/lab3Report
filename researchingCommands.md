# Researching Commands

 ## `grep` command-line options
 Sources: [Grep wikibooks](https://en.wikibooks.org/wiki/Grep)
 [grep geeksforgeeks.org](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
 

The `grep` command is used to search for patterns in files andl directories according to a string that is used with the command. This string specifies the result of the `grep` command. There are different command-line options for `grep`, these examples will be seen using the `written_2/` folder.

---

`grep -o`
Displays only the matched pattern. By default, `grep` usually returns the whole line that has the matched string but the `-o` allows it to only siplay the matched pattern. This is ran using the format: `grep -o "<pattern>" <file_path>` Here is an example of using `grep -o`

Running `$  grep -o "vistas" written_2/travel_guides/berlitz1/*.txt`
```
$ grep -o "vistas" written_2/travel_guides/berlitz1/*.txt
written_2/travel_guides/berlitz1/IntroDublin.txt:vistas
written_2/travel_guides/berlitz1/IntroLakeDistrict.txt:vistas
written_2/travel_guides/berlitz1/IntroMadeira.txt:vistas
written_2/travel_guides/berlitz1/WhereToIbiza.txt:vistas
written_2/travel_guides/berlitz1/WhereToIbiza.txt:vistas
written_2/travel_guides/berlitz1/WhereToIsrael.txt:vistas
written_2/travel_guides/berlitz1/WhereToJerusalem.txt:vistas
written_2/travel_guides/berlitz1/WhereToJerusalem.txt:vistas
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt:vistas
written_2/travel_guides/berlitz1/WhereToMadeira.txt:vistas
```

Running `$  grep -o "pyramid" written_2/travel_guides/berlitz1/*.txt`
```
$ grep -o "pyramid" written_2/travel_guides/berlitz1/*.txt
written_2/travel_guides/berlitz1/HistoryEgypt.txt:pyramid
written_2/travel_guides/berlitz1/HistoryJapan.txt:pyramid
written_2/travel_guides/berlitz1/IntroEgypt.txt:pyramid
written_2/travel_guides/berlitz1/IntroEgypt.txt:pyramid
written_2/travel_guides/berlitz1/IntroLasVegas.txt:pyramid
written_2/travel_guides/berlitz1/WhatToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhatToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhatToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhatToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhatToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhatToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToEgypt.txt:pyramid
written_2/travel_guides/berlitz1/WhereToFrance.txt:pyramid
written_2/travel_guides/berlitz1/WhereToFrance.txt:pyramid
written_2/travel_guides/berlitz1/WhereToFrance.txt:pyramid
written_2/travel_guides/berlitz1/WhereToFrance.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIndia.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIsrael.txt:pyramid
written_2/travel_guides/berlitz1/WhereToIsrael.txt:pyramid
written_2/travel_guides/berlitz1/WhereToJapan.txt:pyramid
written_2/travel_guides/berlitz1/WhereToJerusalem.txt:pyramid
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:pyramid
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:pyramid
```

`grep -o` can provide information on the exact file where the pattern is found but does not show whole line. 

---

`grep -rl`
Recursively searches files for a line. The `r` pertains to recursion while the `l` lists the file names. This command is ran using the format: `grep -rl "<pattern>" <file_path>` 

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
This second example searches for the pattern in a specified path `travel_guides/berlitz2` withing the `written_2` directory. It shows that only the `PuertoRico-WhatToDo.txt` has the pattern.

---

`grep -c`
Outputs the count of the amount of matching lines only. The returned integer is like a count for the number of times the pattern is matched within a file. This command is ran using the formatS `grep -c "<pattern>" <file_path>`

Running `grep -c "giraffe" written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt`
```
$ grep -c "giraffe" written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt 
1
```
This shows that the word `giraffe` has only been found one time in the single file `PuertoRico-WhatToDo.txt`

Another example is using `grep -c` for a larger directory with multiple files:
Running `grep -c "vistas" written_2/travel_guides/berlitz1/*.txt`
```
$  grep -c "vistas" written_2/travel_guides/berlitz1/*.txt
written_2/travel_guides/berlitz1/HandRHawaii.txt:0
written_2/travel_guides/berlitz1/HandRHongKong.txt:0
written_2/travel_guides/berlitz1/HandRIbiza.txt:0
written_2/travel_guides/berlitz1/HandRIsrael.txt:0
written_2/travel_guides/berlitz1/HandRIstanbul.txt:0
written_2/travel_guides/berlitz1/HandRJamaica.txt:0
written_2/travel_guides/berlitz1/HandRJerusalem.txt:0
written_2/travel_guides/berlitz1/HandRLakeDistrict.txt:0
written_2/travel_guides/berlitz1/HandRLasVegas.txt:0
written_2/travel_guides/berlitz1/HandRLisbon.txt:0
written_2/travel_guides/berlitz1/HandRLosAngeles.txt:0
written_2/travel_guides/berlitz1/HandRMadeira.txt:0
written_2/travel_guides/berlitz1/HandRMadrid.txt:0
written_2/travel_guides/berlitz1/HandRMallorca.txt:0
written_2/travel_guides/berlitz1/HistoryDublin.txt:0
written_2/travel_guides/berlitz1/HistoryEdinburgh.txt:0
written_2/travel_guides/berlitz1/HistoryEgypt.txt:0
written_2/travel_guides/berlitz1/HistoryFrance.txt:0
written_2/travel_guides/berlitz1/HistoryFWI.txt:0
written_2/travel_guides/berlitz1/HistoryGreek.txt:0
written_2/travel_guides/berlitz1/HistoryHawaii.txt:0
written_2/travel_guides/berlitz1/HistoryHongKong.txt:0
written_2/travel_guides/berlitz1/HistoryIbiza.txt:0
written_2/travel_guides/berlitz1/HistoryIndia.txt:0
written_2/travel_guides/berlitz1/HistoryIsrael.txt:0
written_2/travel_guides/berlitz1/HistoryIstanbul.txt:0
written_2/travel_guides/berlitz1/HistoryItaly.txt:0
written_2/travel_guides/berlitz1/HistoryJamaica.txt:0
written_2/travel_guides/berlitz1/HistoryJapan.txt:0
written_2/travel_guides/berlitz1/HistoryJerusalem.txt:0
written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt:0
written_2/travel_guides/berlitz1/HistoryLasVegas.txt:0
written_2/travel_guides/berlitz1/HistoryMadeira.txt:0
written_2/travel_guides/berlitz1/HistoryMadrid.txt:0
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:0
written_2/travel_guides/berlitz1/HistoryMallorca.txt:0
written_2/travel_guides/berlitz1/IntroDublin.txt:1
written_2/travel_guides/berlitz1/IntroEdinburgh.txt:0
written_2/travel_guides/berlitz1/IntroEgypt.txt:0
written_2/travel_guides/berlitz1/IntroFrance.txt:0
written_2/travel_guides/berlitz1/IntroFWI.txt:0
written_2/travel_guides/berlitz1/IntroGreek.txt:0
written_2/travel_guides/berlitz1/IntroHongKong.txt:0
written_2/travel_guides/berlitz1/IntroIbiza.txt:0
written_2/travel_guides/berlitz1/IntroIndia.txt:0
written_2/travel_guides/berlitz1/IntroIsrael.txt:0
written_2/travel_guides/berlitz1/IntroIstanbul.txt:0
written_2/travel_guides/berlitz1/IntroItaly.txt:0
written_2/travel_guides/berlitz1/IntroJamaica.txt:0
written_2/travel_guides/berlitz1/IntroJapan.txt:0
written_2/travel_guides/berlitz1/IntroJerusalem.txt:0
written_2/travel_guides/berlitz1/IntroLakeDistrict.txt:1
written_2/travel_guides/berlitz1/IntroLasVegas.txt:0
written_2/travel_guides/berlitz1/IntroLosAngeles.txt:0
written_2/travel_guides/berlitz1/IntroMadeira.txt:1
written_2/travel_guides/berlitz1/IntroMadrid.txt:0
written_2/travel_guides/berlitz1/IntroMalaysia.txt:0
written_2/travel_guides/berlitz1/IntroMallorca.txt:0
written_2/travel_guides/berlitz1/JungleMalaysia.txt:0
written_2/travel_guides/berlitz1/WhatToDublin.txt:0
written_2/travel_guides/berlitz1/WhatToEdinburgh.txt:0
written_2/travel_guides/berlitz1/WhatToEgypt.txt:0
written_2/travel_guides/berlitz1/WhatToFrance.txt:0
written_2/travel_guides/berlitz1/WhatToFWI.txt:0
written_2/travel_guides/berlitz1/WhatToGreek.txt:0
written_2/travel_guides/berlitz1/WhatToHawaii.txt:0
written_2/travel_guides/berlitz1/WhatToHongKong.txt:0
written_2/travel_guides/berlitz1/WhatToIbiza.txt:0
written_2/travel_guides/berlitz1/WhatToIndia.txt:0
written_2/travel_guides/berlitz1/WhatToIsrael.txt:0
written_2/travel_guides/berlitz1/WhatToIstanbul.txt:0
written_2/travel_guides/berlitz1/WhatToItaly.txt:0
written_2/travel_guides/berlitz1/WhatToJamaica.txt:0
written_2/travel_guides/berlitz1/WhatToJapan.txt:0
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:0
written_2/travel_guides/berlitz1/WhatToLasVegas.txt:0
written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:0
written_2/travel_guides/berlitz1/WhatToMadeira.txt:0
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:0
written_2/travel_guides/berlitz1/WhatToMallorca.txt:0
written_2/travel_guides/berlitz1/WhereToDublin.txt:0
written_2/travel_guides/berlitz1/WhereToEdinburgh.txt:0
written_2/travel_guides/berlitz1/WhereToEgypt.txt:0
written_2/travel_guides/berlitz1/WhereToFrance.txt:0
written_2/travel_guides/berlitz1/WhereToFWI.txt:0
written_2/travel_guides/berlitz1/WhereToGreek.txt:0
written_2/travel_guides/berlitz1/WhereToHawaii.txt:0
written_2/travel_guides/berlitz1/WhereToHongKong.txt:0
written_2/travel_guides/berlitz1/WhereToIbiza.txt:2
written_2/travel_guides/berlitz1/WhereToIndia.txt:0
written_2/travel_guides/berlitz1/WhereToIsrael.txt:1
written_2/travel_guides/berlitz1/WhereToIstanbul.txt:0
written_2/travel_guides/berlitz1/WhereToItaly.txt:0
written_2/travel_guides/berlitz1/WhereToJapan.txt:0
written_2/travel_guides/berlitz1/WhereToJerusalem.txt:2
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt:1
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:0
written_2/travel_guides/berlitz1/WhereToMadeira.txt:1
written_2/travel_guides/berlitz1/WhereToMadrid.txt:0
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:0
written_2/travel_guides/berlitz1/WhereToMallorca.txt:0
```
The results show that 8 of the `.txt` files in `written_2/travel_guides/berlitz1/` have the string `vistas` and `-c` returns the amount of times the pattern is found in the respective file.

---

`grep -rn`
Recursively searches for pattern where `r` pertains to recursion and `n` pertains to find the file and line where the pattern is found. This command is ran using the format: `grep -rn "<pattern>" <file_path>`

Running `grep -rn "John Simcoe" written_2/` 
```
$  grep -rn "John Simcoe" written_2/
written_2/travel_guides/berlitz2/Canada-History.txt:25:With great pioneering skill, Upper Canada’s first lieutenant governor, John Simcoe, pushed new highways north from Lake Ontario and west to Hamilton. He established the provincial capital at a trading post, Toronto, in the heart of a malarial swamp, and renamed it York. A landed gentry made up of army officers, government officials, and commercial speculators ran the province, creating a hereditary aristocracy known as the Family Compact. More Americans were lured over the border with land grants; the population rose from 14,000 in 1792 to 90,000 by 1812. French-Canadians were also multiplying rapidly, from 60,000 when New France was abandoned in 1760 to 330,000 fifty years later.
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:26:Ethnically diverse, Toronto is Canada’s largest city, home to 4.3 million people. Hard to believe that this gleaming citadel of big business and the good urban life was a malarial swamp in the 1790s. Muddy York once could be recommended only by its commanding position on Lake Ontario, from which Fort York guarded the troublesome American border. Today, the mud is neatly paved over, the mosquitoes have flown elsewhere, and the Americans are less trouble than they used to be. Yonge Street, the military highway that founder John Simcoe thrust north from the fort to Lake Simcoe, starts out now as downtown Toronto’s main commercial artery. Its intersection at the elegant shopping thoroughfare, Bloor Street, is the fashionable hub of the city.        
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:27:Following John Simcoe’s military grid pattern, Toronto’s main arteries run from the lakefront north: Spadina and University Avenues, Bay, Yonge, and Church Streets; and east–west: Front, King, Queen, Dundas, College-Carlton, and Bloor Streets. Our sightseeing itinerary starts down at the waterfront and works north through the business district to the chic shopping and museum area. As an alternative, especially if you have children, you may prefer to start downtown, around Union Station, and visit the other sights to the north before coming back to relax among the recreational attractions of the waterfront. Getting around the city is quite simple, but while downtown, park your car and walk or use the buses or subway.
```
Shows that the file `written_2/travel_guides/berlitz2/Canada-History.txt` has the name `John Simcoe`. `grep -rn` also shows the lines, here we can see that lines 25, 26, and 27 all include the string `John Simcoe`.


Running `grep -rn "Chronicles" written_2/travel_guides/berlitz1/` shows that `grep -rn` can return multiple files containing the same pattern.
```
$  grep -rn "Chronicles" written_2/travel_guides/berlitz1/
written_2/travel_guides/berlitz1/HistoryJapan.txt:9:        (“Chronicles of Japan”), the islands of Japan were born of a marriage
written_2/travel_guides/berlitz1/HistoryJapan.txt:23:        Prehistory and Early Chronicles
written_2/travel_guides/berlitz1/WhereToGreek.txt:352:        Parian Chronicles, a history of ancient Greece enscribed on marble
```
