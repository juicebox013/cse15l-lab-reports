# Lab Report 5 by Justin Nguyen
---
## Researching commands for `**grep**` 

The grep command is a very versatile tool in which we can use to search for various keywords within files of a directory/folder. 
When you are provided with extremely large repositories, we dont want to look through each folder/file for a specific
keyword, so we turn to the grep command.

This command can be used in a variety of different ways in order to narrow down your search. One of the simplest
ways to use this command cna be demonstrated as:
## `grep <string we want to search for> <the file we want to search>`

example 1 input: `$ grep ".txt" find-results.txt > grep-results.txt`
this places every file in which contains the string ".txt" within a new file in which i titled "grep-results.txt"

example 1 output:
```
written_2/
written_2/non-fiction
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
```

example 2 input: `$ grep "Poland" find-results.txt > grep-results.txt`
this replaces every file within the grep-results.txt file with every that contains "Poland"

example 2 output:
```
written_2/travel_guides/berlitz2/Poland-History.txt
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
```

## Another way to use the grep command is by adding the `e` keyword
this allows us to find certain files with multiple strings

example 1 input: `$ grep -e "Bahamas" -e "Poland" find-results.txt`
example 1 output:
```
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Poland-History.txt
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt
```

example 2 input: `$ grep -e "China" -e "Costa" find-results.txt`
example 2 output:
```written_2/travel_guides/berlitz2/China-History.txt
written_2/travel_guides/berlitz2/China-WhatToDo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
written_2/travel_guides/berlitz2/Costa-History.txt
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt
written_2/travel_guides/berlitz2/CostaBlanca-History.txt
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt
```

You can also use the grep command to find a the exact line in which a keyword is present in a file by using 
## the `-n` keyword 
this allows us to search through a file and print out which line a certain keyword is present within a file

example 1 input: `$ grep -n 10 find-results.txt`
example 1 output:
```
36:written_2/non-fiction/OUP/Fletcher/ch10.txt
43:written_2/non-fiction/OUP/Kauffman/ch10.txt
```

example 2 input: `$ grep -n "LosAngeles" find-results.txt`
example 2 output:
```
67:written_2/travel_guides/berlitz1/HandRLosAngeles.txt
110:written_2/travel_guides/berlitz1/IntroLosAngeles.txt
133:written_2/travel_guides/berlitz1/WhatToLosAngeles.txt
153:written_2/travel_guides/berlitz1/WhereToLosAngeles.txt
```

Furthermore, the grep command can also be used with 
##the `-v` keyword
this keyword allows the user to print out the lines of code in which **do not** contain a specific string

example 1 input: `$ grep -v "WhereTo" find-results.txt`
example 1 output:
```
written_2/
written_2/non-fiction
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Berk/CH4.txt
```

example 2 input: `$ grep -v "ch" find-results.txt`
example 2 output:
```
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz1/HandRHawaii.txt
written_2/travel_guides/berlitz1/HandRHongKong.txt
written_2/travel_guides/berlitz1/HandRIbiza.txt
written_2/travel_guides/berlitz1/HandRIsrael.txt
written_2/travel_guides/berlitz1/HandRIstanbul.txt
written_2/travel_guides/berlitz1/HandRJamaica.txt
written_2/travel_guides/berlitz1/HandRJerusalem.txt
written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
written_2/travel_guides/berlitz1/HandRLasVegas.txt
written_2/travel_guides/berlitz1/HandRLisbon.txt
written_2/travel_guides/berlitz1/HandRLosAngeles.txt
```

##sources used
[link1](https://linuxcommand.org/lc3_man_pages/grep1.html)
[link2](https://www.hostinger.com/tutorials/grep-command-in-linux-useful-examples/#:~:text=Grep%2C%20or%20global%20regular%20expression,any%20lines%20that%20contain%20it)



