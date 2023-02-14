# Lab Report 3
* Researching Commands (choose "grep" command)
  * grep -rl --exclude-dir
    * It will exclude subdirectory or subdirectories and then search content in the directory. And then prints out the name of the file contains content.
    * grep -rl --exclude-dir="written_2/travel_guides" --exclude-dir="written_2/non-fiction/OUP/Fletcher" --exclude-dir="written_2/non-fiction/OUP/Berk" "autonomy" written_2
      * Outputs 
        * written_2/non-fiction/OUP/Abernathy/ch2.txt
        * written_2/non-fiction/OUP/Abernathy/ch3.txt
        * written_2/non-fiction/OUP/Castro/chP.txt
      * It searches "autonomy" in the file which is not located in travel_guides, Fletcher, Berk directories.  
    * grep -rl --exclude-dir="written_2/travel_guides" "Hong Kong" written_2 
      * Outputs
        * written_2/non-fiction/OUP/Abernathy/ch1.txt
        * written_2/non-fiction/OUP/Abernathy/ch15.txt
      * It searches "Hong Kong" from only non-fiction directory but not travel_guides directory.
  * grep -i
    * It will ignore the case. 
    * grep -i "HaLekULani" written_2/*/*/*.txt
      * Outputs
      * written_2/travel_guides/berlitz1/HandRHawaii.txt:        Halekulani $$$$ 2199 Kalia Road, Honolulu, HI 96815; Tel.
written_2/travel_guides/berlitz1/HandRHawaii.txt:        <www.halekulani.com>. Very large rooms, most facing the ocean,
written_2/travel_guides/berlitz1/HandRHawaii.txt:        outdoor lounge for sunset drinks, Halekulani is a complete resort. 454
  * grep -w
    * It will search content for full string, not the sub-string.
  * grep -m #
    * It search and print the content # times then it stops. 
  * Resources
    * https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/
    * https://www.shayanderson.com/linux/grep-exclude-directory.htm
    * https://www.unix.com/shell-programming-and-scripting/113991-grep-m-option.html
