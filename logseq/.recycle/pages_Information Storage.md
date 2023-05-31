- {{renderer :toc_clytbvq}}
	- ## 0. Introduction
		- machine storage information as `bit`
		- a block of 8 bits = `byte`
		- A machien-level proagram views memory as ==a very large array of byte== = ==virtual memory==
			- How byte → array of byte?
			  ((6280570d-252f-4d24-9cdd-32444b776144))
		- task of a complier and the run-time- system ==subdivide virtual memory== into more =  ==manageable units==
			- What's manageable units?
			  To store different ==program objects==, that is, program data, instructions, and control information.
		- Summary
		  machine(==bit== → ==byte== → byte array with unique number(address) called ==virtual memory== → subdivide into ==program objects== by high level program)
	- ## 1. Hex Notation
		- Math sign it as
		  ((62805b9c-a873-460d-809d-3534ee95471c))
		- Program sign it as `0x00` to `0xFF`
		- console.log(0xFF)
		  
		  fmt.Printf(0xFF)
		- The mean of Hex Notation: just be easy for human to read bit array
	- ## 2. Word Size
		- ==word size== is a fixed-size data (meta data of computer)
		- it define the virtual memory address
		- word size = 32 mean
			- the virtual momory address range 0 to 2^n-1 (unit is byte)
			- so the max virtual address space to 4GB (2^n-1)
			- where this meta data(word size) defined at?
			  ==CPU==
	- ## 3. Data Sizes
		- different data struct type has diff data size
	- ## 4. Adressing and Byte Ordering
		- What will the address of the Object?
		  ((62806678-ffa9-46bf-9789-a303f4bf703d))
		- How will we order the bytes in memory?
		  ((628066d4-9643-42ea-9d05-f09ea7dc7a89))
	- ## 5. Representing Strings
		- Char with encode rule ascii or unicode rule (utf-8 etc...)
		- string is a array of char
	- ## 6. Representing Code
		- char → string → code text → ... → .bin (binary file)
	- ## 7. Boolean Algebras and Rings
		- rings
		  ((628070bf-7706-4f0d-b0e0-aaeb7dbceca7))
		- vector {0, 1, 2 , ..., n-1}
		- bool operation is bit array vector operation
		  ((62807aba-8f49-44ff-9d15-b67609026908))
	- ## 8. Bit-Level Opearations in C
		- ((62807bfe-4455-4d59-9150-e6e5ca259430))
	- ## 9. Logical Operations in C
		- ((62807c48-4436-4d40-9de9-62c7ce284016))
	- ## 10. Shift Operations in C
		- logical
			- ((628086d6-14a6-44c8-adc3-6f96f7415abb))
		- Arithmetic
			- ((6280874c-13f4-4f74-b620-5f8d33d5b976))
		- ((62808792-ae30-4674-aba3-0c5639345cf3))
		- Golang use Logical Shift Opearation
		  ![image.png](../assets/image_1652590737811_0.png)
		- Most program language use logic shift operation.(JS、Go)