# Lab Report 3

# grep Command Line

## -i command option
```
grep -i "BAHAMAS" grep-results.txt 
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
```

The grep `-i` option ignores any uppercase or lowercase of the word you are looking for. So here even if it is all caps or all lowercase it will return the paths to the files  with the first letter capaitalized.

```
[cs15lwi23asj@ieng6-202]:skill-demo1-data:314$ grep -c -i "cuba" grep-results.txt 
3
```
Here where the search is case sensitive, the `-i` ignores the capitalization so the command will work correctly. This would be good for if you want to look for a specific word without having to worry about the case sensitiveness.


## -c command option

```
[cs15lwi23asj@ieng6-202]:skill-demo1-data:313$ grep -c "Cuba" grep-results.txt 
3
```

```
grep -c "Athens" grep-results.txt 
4
```

The `-c` option gets the count of the amount of lines or files with the specific string that we are looking for. This is good when you need get a count of how many fiels there are of a certain string.

## -l command option

```
grep -l "Lucayans" berlitz2/*.txt
berlitz2/Bahamas-History.txt
```
Using the grep `-l` it finds the specific file that contains the certain string when given a certain path. This is good when looking for a file that contains a certain string.

```
grep -rl "Bahamas" 
written_2/travel_guides/berlitz1/WhatToFWI.txt
written_2/travel_guides/berlitz2/Bahamas-History.txt
written_2/travel_guides/berlitz2/Bahamas-Intro.txt
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
find-results.txt
grep-results.txt
```
The `-r` feature seaches recursively throughout all the files and directories, and the subdirectories looking for that specific string and the `l` modifys it so that it returns the files that contains it.

## -o command option

```
grep -o "Cuba" grep-results.txt 
Cuba
Cuba
Cuba
```
The `-o` command looks through the files and returns the matching parts of the element in the quotation marks.

```
grep -ro "Cuba from Spain" 
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:Cuba from Spain
```
Adding the `-r` command it looks through the directories and returns the matching element in the quotation marks. As well as the file that contains it. This would be useful if you need to check if there is a matching element.

For all the command options I found it at [https://en.wikibooks.org/wiki/Grep](https://en.wikibooks.org/wiki/Grep).
