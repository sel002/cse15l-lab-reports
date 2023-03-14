# Lab Report 5
## Researching Commands (choose "find" command)
1) find <directory> -type d
  * It will find directories or subdirectories and then search content in the directory. And then prints out the name of the file contains content.
* Example 1
    
```
# Input
find written_2/non-fiction/OUP -type d

# Outputs
written_2/non-fiction/OUP
written_2/non-fiction/OUP/Berk
written_2/non-fiction/OUP/Abernathy
written_2/non-fiction/OUP/Rybczynski
written_2/non-fiction/OUP/Kauffman
written_2/non-fiction/OUP/Fletcher
written_2/non-fiction/OUP/Castro
```
      
* Example 2

```
# Input
find written_2/travel_guides -type d

# Outputs
written_2/travel_guides
written_2/travel_guides/berlitz1
written_2/travel_guides/berlitz2
```
      
2) find <directory> -maxdepth i -type d
  * It will find directories listed down i times from the start point which is <directory>.

* Example 1

```
# Input
find written_2/ -maxdepth 1 -type d

# Outputs
written_2/
written_2//non-fiction
written_2//travel_guides
```

* Example 2

```
# Input
find written_2/ -maxdepth 2 -type d

# Outputs
written_2/
written_2//non-fiction
written_2//non-fiction/OUP
written_2//travel_guides
written_2//travel_guides/berlitz1
written_2//travel_guides/berlitz2
```

3) find <directory> -type f
  * It will find all files in the <directory>. "f" means file including such as text files, not considering (sub)directories. 
  * Able to see which specific (sub)directory has the specific file in <directory>

* Example 1

```
# Input
find written_2/non-fiction/OUP/Abernathy -type f

# Outputs
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch7.txt
written_2/non-fiction/OUP/Abernathy/ch6.txt
written_2/non-fiction/OUP/Abernathy/ch8.txt
written_2/non-fiction/OUP/Abernathy/ch9.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
written_2/non-fiction/OUP/Abernathy/ch14.txt
```

* Example 2

```
# Input
find written_2/non-fiction/OUP/Fletcher  -type f

# Outputs
written_2/non-fiction/OUP/Fletcher/ch2.txt
written_2/non-fiction/OUP/Fletcher/ch1.txt
written_2/non-fiction/OUP/Fletcher/ch5.txt
written_2/non-fiction/OUP/Fletcher/ch6.txt
written_2/non-fiction/OUP/Fletcher/ch9.txt
written_2/non-fiction/OUP/Fletcher/ch10.txt
```

4) find <directory> -size +(file size)
  * It search for the files have bigger file size than (file size) in command line.

* Example 1

```
# Input
find written_2/non-fiction -size +100k

# Outputs
written_2/non-fiction/OUP/Berk/ch2.txt
written_2/non-fiction/OUP/Berk/CH4.txt
```

* Example 2

```
# Input
find written_2/travel_guides -size +100k

# Outputs
written_2/travel_guides/berlitz1/WhereToIndia.txt
written_2/travel_guides/berlitz1/WhereToItaly.txt
written_2/travel_guides/berlitz1/WhereToMalaysia.txt
written_2/travel_guides/berlitz1/WhereToJapan.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt
written_2/travel_guides/berlitz2/China-WhereToGo.txt
```

## Resources
[Link1](https://www.redhat.com/sysadmin/linux-find-command)
[Link2](https://linuxconfig.org/how-to-use-find-command-to-search-for-files-based-on-file-size)
