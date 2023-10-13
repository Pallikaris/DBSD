### Developing Data Base Systems###
### National & Kapodistrian University of Athens###
### Department of Informatics and Telecommunications###
### 3/12/2022 - 9/1/2023


__Students__
Dimitris Georgantopoulos	sdi1900036
Giorgos Pallikaris		sdi1400335

__Announcement__
https://drive.google.com/file/d/11CKdv2JLmja1_VzPhkNWe-hLCQMlZqje/view?usp=sharing

__Grading__
100/100

__Project__
Developing Primary and Secondary Hash Table Files for Database usage
over a given Block-Buffer handling library <bf.h>  .

__Description__
Our project correctly manages to store files up to the limit that hardware allows.
Specifically our local disk.It is vulnerable to errors that preexist in the given library,
due to incosistent error handling  in <bf.h>
We don't expand such errors in any case.

__Use__
You should use these executables for demonstration or actuall storing of Records like those 
defined in record.h .
At sht_main.c , ht_main.c and hp_main.c you can see a demo execution.
We suggest reading it before trying a new project of your own based on this one.
Line of execution should follow.

		*Block layer  initilization & replacement algorithm selection.

		*Creating file(s)

		*Opening file(s)  thus storing a live copy of files' index  which will be used as handler until the file is closed.


		**Insertion,deletion,search, use of multiple files secondary hash tables etc..

		*Closing file(s)


__Usefoul Info__

For custom confugurations go to ~/examples directory and set your own records number,buckets num and other parameters there.

Check error file to see possible errors for your implementation and fast debugging.

Check demo file to undestand what is going on under the hood and verify expected results.

You can see them also at the end of execution at your terminal by typing the choosing the correspondive letter in 5 seconds.


__Features__

Replacement algorithm selection
Create
Open
Close
Insert record
Search record
Filetype specified operations
Live statistics in O(1)
Error handling
Optimall use of the given memory buffer for the given algorithm.


__Coming_Features__

	*Variating record sizes

	*Real data oriented hash functions

	*Unique entries


__Running__

To automatically run Heap file demonstration example go script directory and run :

$ bash hp.sh

To automatically run Hash Table file demonstration example go script directory and run :

$ bash ht.sh

To  automatically run Secondary Hash Table & Hash Table demonstration example go script directory and run :

$ bash sht.sh


	**To manually run a file run :

	$make clean
	
	to destroy log files and database in case you want to reuse an already existing database name.
	________________________________________________________________________________________________

	**Otherwise just set a new database name( 2 names in case of sht) in your main function that uses the library and run: 

	$ make cleanlog   

	so you can reuse logfiles.



	Complilation commands:

	$make ht 
	$make hp 
	$make sht

	Execution commands:

	$./build/ht_main
	$./build/hp_main
	$./build/sht_main



__For_examiners__

		Our project can create a file name by the users' main function  to store entries of the predefined type you gave.
		Three file structures are implemented over a dynamic bucket size,dynamic record size,memory page buffer replacement algo. and others...

		Executables do not leave memory junks created by our programms,although university given library itself creates some.

		Page/block pin/unpin/setdirty functions are used correctly and return verified results in a range of possible executions.

		2 implementations of buffer handler exist in our programm:
			A.]Live variable file handler in main with lifetime from opening to close
			B.]Reuse of metadata block ( "block 0") 

		We strongly prefer the first one mostly because of 
		1.code clarity 
		2.database usage
		Nevertheless second option may be better for a other systems with small buffer ability or high multiple file load.

		*Friendly reminder for next years:
		The random record generator has to be fixxed in a way that does not allow junk letters at the end of string attributes.
		
		
		
		
		
		
Thank you!



