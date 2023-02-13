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

This alternate way of using `grep` colors the search string or pattern that you are trying to find with `grep`. This option can make it easier to locate the search string or pattern if the output is a sea of results. 

[Link](https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix)

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

This addition to the `grep` command is an easier way to search for a string or pattern through a directory and its subdirectories, without having to know any names of the directory's subdirectories. Say I wanted to search through a directory for a specific string, but I know nothing of any subdirectories. The `grep -r` command would come in handy. 
