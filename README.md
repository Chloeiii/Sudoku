# Sudoku - CSC320 Project
	
Global Pre-Conditions:
- Python 2.7 installed :sunglasses:
- minisat 2.2.0 installed :star:
--------------------------------------------------------------------------------------------------
Base Assignment Files - Minimal Encoding using miniSAT
--------------------------------------------------------------------------------------------------	
	->python python sud2sat.py 1.txt outcome.txt 
	->minisat CNF.txt solution.txt
	->python sat2sud.py solution.txt
	
	File: sud2sat.py
	python python sud2sat.py 1.txt outcome.txt 
	output: CNF.txt
	
	Pre-Condition:
	- <sudoku file> has format: contiguous string of 81 characters on the
	  first line of the .txt file where all digits are sudoku numbers and all 
	  other characters represent blank spaces(we are using 1.txt as input file)
	  EX: "000083900100000030004000070042030000600000004000070010020000000080009200000250006"
	- <encoding file> has standard format: simplified "DIMACS CNF" format which is named as "CNF.txt"

	File: sat2sud.py
	
	Pre-Conditions:
	-miniSAT successed and has a input for example(solution.txt)
	
	To Execute (General Format):
		> python sat2sud.py <SAT solver output file>
		
-------------------------------------------------------------------------------------------------
Additional Assignment Files - Extended Encodings
-------------------------------------------------------------------------------------------------

	->python python extendsud2sat.py 1.txt outcome.txt 
	->minisat CNF.txt solution.txt
	->python sat2sud.py solution.txt
	
	File: extendsud2sat.py
	python python extendsud2sat.py 1.txt outcome.txt 
	output: CNF.txt
	
	Pre-Condition:
	- <sudoku file> has format: contiguous string of 81 characters on the
	  first line of the .txt file where all digits are sudoku numbers and all 
	  other characters represent blank spaces(we are using 1.txt as input file)
	  EX: "4.....8.5.3..........7......2.....6.....8.4......1.......6.3.7.5..2.....1.4......
    
	- <encoding file> has standard format: simplified "DIMACS CNF" format which is named as "CNF.txt"

	File: sat2sud.py
	
	Pre-Conditions:
	-miniSAT successed and has a input for example(solution.txt)
	
	To Execute (General Format):
		> python sat2sud.py <SAT solver output file>



-------------------------------------------------------------------------------------------------
Additional Assignment Files - n*n Puzzle (4x4)
-------------------------------------------------------------------------------------------------
	1. from puzzle to CNF
		RUN: python sud2sat4X4.py 4X4input.txt 4X4cnf.txt
		Pre-Condition:
		- <sudoku file> has format: contiguous string of 81 characters on the
		  first line of the .txt file where all digits are sudoku numbers and all 
		  other characters represent blank spaces(we are using 4X4input.txt as input file)
		  EX: "4000000310000002"
		- <encoding file> has standard format: simplified "DIMACS CNF" format which is named as "CNF.txt"
	2. run minisat
		RUN: minisat CNF.txt solution.txt 
		
	3.from SAT solution to puzzle solution
		RUN: python sat2sut4X4.py solution.txt
		Pre-Conditions:
		-miniSAT successed and has a input for example(solution.txt)
		
	puzzle sample:
		4000
		0003
		1000
		0002	
	solved output sample:
		4 | 3 | 2 | 1
		-------------
		2 | 1 | 4 | 3
		-------------
		1 | 2 | 3 | 4
		-------------
		3 | 4 | 1 | 2
-------------------------------------------------------------------------------------------------
Sample test cases with solutions using the program && run time calculation
-------------------------------------------------------------------------------------------------
- CSC320Report.pdf
-------------------------------------------------------------------------------------------------
