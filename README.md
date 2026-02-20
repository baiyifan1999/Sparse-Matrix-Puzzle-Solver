# Sparse-Matrix-Puzzle-Solver
A C program that manipulates large sparse matrices using dynamic memory and supports a set of cell/row/column operations to transform an initial matrix into a target matrix, with stage-based formatted output (COMP10002 FoA Assignment 2).

This program implements a sparse matrix transformation engine in C. It reads an initial matrix, a target matrix, and a sequence of manipulation instructions from standard input, then applies the operations in order while reporting intermediate states. The goal is to transform the initial matrix into the target matrix, treating the process like a puzzle solved in as few steps as possible.

Because matrices can be extremely large (up to millions of rows/columns) but mostly zero, the program uses dynamic memory and a sparse matrix representation to store and manipulate only nonzero entries efficiently.

The program supports:
	•	Parsing an instruction-based input format that defines initial/target sparse matrices
	•	Tracking matrix dimensions and the number of nonzero entries (nnz)
	•	Printing matrices in two modes:
	•	compact grid view for small matrices with values 0–9
	•	coordinate list format (r,c)=v for large or wide-range matrices
	•	Executing core matrix manipulations, including:
	•	setting and swapping individual cells (s, S)
	•	scaling and shifting values (m, a)
	•	copying and swapping whole rows/columns (r, c, R, C)
	•	Stage-based progression (Stage 0–2) with formatted output matching provided specifications
	•	Early termination when the current matrix matches the target matrix, reporting the total steps used
	•	Careful memory management using malloc() / free() to avoid leaks

Developed for the University of Melbourne COMP10002 Foundations of Algorithms course, focusing on dynamic memory, sparse data structures, and robust procedural program design.
