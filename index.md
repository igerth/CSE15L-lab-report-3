# Lab Report 3

## Researching Commands
Here are 4 interesting ways I found to use the `grep` command, along with 2 examples for each of the 4 new options. 

### Coloring `grep` results using the `--color` option. 
2 examples of using this with the `written_2` files with a screenshot of each output:
```
$ grep --color "Lucayans" written_2/travel_guides/*/*.txt
```
![Image](https://github.com/igerth/CSE15L-lab-report-3/blob/main/Screenshot%202023-02-13%20at%201.44.32%20PM.png?raw=true)
```
$ grep --color "art museums" written_2/travel_guides/*/*.txt
```
![Image](https://github.com/igerth/CSE15L-lab-report-3/blob/main/Screenshot%202023-02-13%20at%201.54.00%20PM.png?raw=true)

This alternate way of using `grep` colors the search string or pattern that you are trying to find with `grep`. In the first example, I colored the word `Lucayans` and in the second, I colored the word `art museums`. This option can make it easier to locate the search string or pattern if the output is a sea of results. 

Info found [here](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix).

### We can use the `-r` option to search for a pattern in all files in a directory and its subdirectories
2 examples of using this with the `written_2` files with a screenshot of each output:
```
$ grep  -r "café" written_2 > results.txt
```
![Image](https://github.com/igerth/CSE15L-lab-report-3/blob/main/Screenshot%202023-02-13%20at%202.42.01%20PM.png?raw=true)
This is the first few lines of the .txt file that I transferred the `grep` results into since the command returned a lot of lines. The `wc` command could be helpful here. 
```
$ grep -r "exotic birds" written_2
```
![Image](https://github.com/igerth/CSE15L-lab-report-3/blob/main/Screenshot%202023-02-13%20at%202.43.51%20PM.png?raw=true)

This addition to the `grep` command is an easier way to search for a string or pattern through a directory and its subdirectories, without having to know any names of the directory's subdirectories. In the first example, I searched through the entire `written_2` directory for the string `café` and put the results of the `grep` into `results.txt`. Similarly, in the second example, I searched through `written_2` for the string `art museums` and put the results into `results.txt`, which overwrote the previous `grep` search. 

Found this info using the notorious [ChatGPT](https://chat.openai.com/chat).

### If you want to invert your search, that is, only return the lines that do not contain the search string or pattern, use `-v`.
2 examples of using this with the `written_2` files with a screenshot of each output:
```
$ grep -v -r "the" written_2 > results.txt
```
![Image](https://github.com/igerth/CSE15L-lab-report-3/blob/main/Screenshot%202023-02-13%20at%203.19.33%20PM.png?raw=true)
```
$ grep -v -r "art museums" written_2 > results.txt
```
![Image](https://github.com/igerth/CSE15L-lab-report-3/blob/main/Screenshot%202023-02-13%20at%203.19.07%20PM.png?raw=true)

The `-v` addition to `grep` is a useful tool for when you specifically do not want a certain string or pattern. You may use this when searching through a directory you are not quite familiar with where you do not want to see any results pertaining to something specific. The first example gave me the results of every file which does not contain the string `the` in the `written_2` directory, which I then put in `results.txt`. The second example gave me the results of every file which does not contain the string `art museums` in the `written_2` directory, which I then put in `results.txt` as well. 

Found this info [here](https://www.cyberciti.biz/faq/howto-use-grep-command-in-linux-unix/).

### Use the `--include` option to search for a pattern in specific types of files.
2 examples of using this with the `written_2` files with a screenshot of each output:
```
$ grep -c -r --include="*.txt" "biology" written_2/non-fiction
```
![Image](https://github.com/igerth/CSE15L-lab-report-3/blob/main/Screenshot%202023-02-13%20at%203.31.23%20PM.png?raw=true)
```
$ grep -c -r --include="*.txt" "Beaches" written_2/travel_guides/berlitz2
```
![Image](https://github.com/igerth/CSE15L-lab-report-3/blob/main/Screenshot%202023-02-13%20at%203.32.52%20PM.png?raw=true)

The `--include` addition to `grep` is nice because it only searches in the file type that you specify. For instance, in both examples, I searched for the strings `biology` and `Beaches` inside `written_2/non-fiction` and `written_2/travel_guides/berlitz2` respectivley, which only looked for the strings inside `.txt` files. 

Also used [ChatGPT](https://chat.openai.com/chat) for this one as well. 

## Summary
After completing this lab, I definitly think I've got a better grasp of the `grep` command and its different uses.  
