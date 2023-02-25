# Lab Report 3
## Researching Commands (choose "grep" command)
* grep -rl --exclude-dir
  * It will exclude subdirectory or subdirectories and then search content in the directory. And then prints out the name of the file contains content.
1) Example 1
  * It searches "autonomy" in the file which is not located in travel_guides, Fletcher, Berk directories.
    

```
# Input
grep -rl --exclude-dir="written_2/travel_guides" --exclude-dir="written_2/non-fiction/OUP/Fletcher" --exclude-dir="written_2/non-fiction/OUP/Berk" "autonomy" written_2
# Outputs
written_2/non-fiction/OUP/Abernathy/ch2.txt
written_2/non-fiction/OUP/Abernathy/ch3.txt
written_2/non-fiction/OUP/Castro/chP.txt
```
      
2) Example 2
  * It searches "Hong Kong" from only non-fiction directory but not travel_guides directory.

```
# Input
grep -rl --exclude-dir="written_2/travel_guides" "Hong Kong" written_2

# Outputs
written_2/non-fiction/OUP/Abernathy/ch1.txt
written_2/non-fiction/OUP/Abernathy/ch15.txt
```
      
  * grep -i
    * It will ignore the case. 
    * grep -i "HaLekULani" written_2/*/*/*.txt
      * Outputs
        * written_2/travel_guides/berlitz1/HandRHawaii.txt:        Halekulani $$$$ 2199 Kalia Road, Honolulu, HI 96815; Tel.
written_2/travel_guides/berlitz1/HandRHawaii.txt:        <www.halekulani.com>. Very large rooms, most facing the ocean,
written_2/travel_guides/berlitz1/HandRHawaii.txt:        outdoor lounge for sunset drinks, Halekulani is a complete resort. 454
    * grep -i "RoCKHousEHOtel" written_2/*/*/*.txt
      * Outputs
        * written_2/travel_guides/berlitz1/HandRJamaica.txt:        rockhousehotel.com>. Commanding a rocky promontory in West End with
  * grep -wl
    * It will search content for full string, not the sub-string. And then prints out the name of the file contains content.
    * grep -wl "Joan, Palma" written_2/*/*/*.txt
      * Outputs
        * written_2/travel_guides/berlitz1/WhereToMallorca.txt
    * grep -wl "Victoria Harbor" written_2/*/*/*.txt
      * Outputs
        * written_2/travel_guides/berlitz1/IntroHongKong.txt
        * written_2/travel_guides/berlitz1/WhereToHongKong.txt
  * grep -m #
    * It search and print the content # times per file then it stops. 
    * grep -m 2 "Hong Kong Island" written_2/*/*/*.txt
      * Outputs
        * written_2/travel_guides/berlitz1/HistoryHongKong.txt:        Hong Kong Island formally became a British possession two
written_2/travel_guides/berlitz1/IntroHongKong.txt:        architecture are on Hong Kong Island. Across Victoria Harbor, connected
written_2/travel_guides/berlitz1/WhatToHongKong.txt:        Kowloon, especially along Nathan Road; Central on Hong Kong Island,
written_2/travel_guides/berlitz1/WhatToHongKong.txt:        changing rooms, toilets, and snack stands. On Hong Kong Island, Repulse
written_2/travel_guides/berlitz1/WhereToHongKong.txt:        begin across Victoria Harbor on Hong Kong Island, where the city was
written_2/travel_guides/berlitz1/WhereToHongKong.txt:        soaring skyline of Hong Kong Island draws nearer.
    * grep -m 2 "Upper Egypt" written_2/*/*/*.txt
      * Outputs
        * written_2/travel_guides/berlitz1/HistoryEgypt.txt:        b.c. that King Narmer of Upper Egypt conquered Lower Egypt. Around 3100
written_2/travel_guides/berlitz1/HistoryEgypt.txt:        in Heliopolis in Lower Egypt and Thebes (modern Luxor) in Upper Egypt.
written_2/travel_guides/berlitz1/WhatToEgypt.txt:        In Upper Egypt, Nubian floorshows have a different
written_2/travel_guides/berlitz1/WhatToEgypt.txt:        Upper Egypt. Always study any item carefully before purchase.
written_2/travel_guides/berlitz1/WhereToEgypt.txt:        in your vacation along the Nile Valley in Upper Egypt.
written_2/travel_guides/berlitz1/WhereToEgypt.txt:        Upper Egypt
  * Resources
    * https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/
    * https://www.shayanderson.com/linux/grep-exclude-directory.htm
    * https://www.unix.com/shell-programming-and-scripting/113991-grep-m-option.html
