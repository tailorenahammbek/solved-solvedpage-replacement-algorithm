Download Link: https://assignmentchef.com/product/solved-solvedpage-replacement-algorithm
<br>
The main aim of this program is to develop understanding of page replacement algorithms as used in demand paging regimes. After you complete this program you should be able to devise a simulator to rank the performance of various pagereplacement algorithms. Note: If you are unfamiliar with page replacement algorithms refer to the notes or a suitable reference book.

Write a program that receives a filename via the command line and then calculates thef rame composition and the number of major and minor page faults that occur. Your program should work with First In First Out (FIFO), Least Recently Used (LRU), Least Frequently Used (LFU) and Optimal (OPT) page replacement algorithms. The input file should specify *the page replacement algorithm*, the page *frame size* ( i.e. number of frames available) and the page *reference string*. An example input file is shown below:

“`cppLRU370120304230321201701“`

If no input filename is given via the command line then your program should prompt for this information. An example run is shown below (Note: bold-italics indicates user input.):

$ ./a.out

Enter page replacement algorithm: ***LRU***

Enter page frame size: ***3***

Enter reference string: ***70120304230321201701***

“`cppLRU: String / Frames / FaultsStr: 7 0 1 2 0 3 0 4 2 3 0 3 2 1 2 0 1 7 0 1Fr1: 7 7 7 2 2 2 2 4 4 4 0 0 0 1 1 1 1 1 1 1Fr2: – 0 0 0 0 0 0 0 0 3 3 3 3 3 3 0 0 0 0 0Fr3: – – 1 1 1 3 3 3 2 2 2 2 2 2 2 2 2 7 7 7Flt: m m m M – M – M M M M – – M – M ¨C M – –LRU: 3 Minor Faults 9 Major Faults.“`

You can assume the *reference string* will be a sequence of integers (digits 0..9) and no longer than 1000 digits. The value for the page frame size should be 1 to 9. If any file input is invalid your program should print an error message and terminate. If any user input is invalid your program should print an appropriate error message and request that input again. Your program should be implemented in one file named `pager.cpp`.

Add additional functionality to your program in Step-1 so that if a ‘0’ is entered for the *page frame size* your program will test the given *page replacement algorithm* on all frame sizes from 1 to 9 and print a graph showing the number of major page faults (vertical axis) vs the number of frames (horizontal axis). An example run is shown below:

“`cpp$ ./a.out input.txt

LRU: 82329264348593826347485947836236347854945944

9 X8 X X7 XPage 6Faults 5 X X4 X3 X21 X01 2 3 4 5 6 7 8 9Frames“`

(Note: the above plot is fictional and for format purposes only.)