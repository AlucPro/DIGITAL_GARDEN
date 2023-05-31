- {{renderer :toc_ecdfvrn}}
	- ## 1 Integral Data Types
		- in C: char, short, int, long, unsigned
	- ## 2 Unsigned and Two's Complements Encoding(补码)
		- Use vector to define an integer data type of w bits
		  ((62819ece-fecf-42de-b745-0a120e87137c))
		- Binary to Unsigned, length w
		  ((62819d2f-aef6-4e35-8f06-f2d43737bd37))
		- Binary to two's complement, length w
		  :LOGBOOK:
		  CLOCK: [2022-05-16 Mon 08:43:32]
		  :END:
		  ((62819e2d-144c-4c43-86c2-cc15e6414314))
		- The range of unsigned and two's complements
		  
		  ((62819fd3-b50d-4d91-a3c9-12ada2ded91c))
		  ((62819fef-dedd-496b-8075-53d207970d18))
		  ((6281a002-6422-4e0a-affc-1d653629f50b))
		- why use two's complement to sign signed number(espeical negative value)
			- add is always from left to right
			  ![IMG_FE7906285040-1.jpeg](../assets/IMG_FE7906285040-1_1652746213257_0.jpeg)
			  ((6282e859-2863-4c98-adde-7cc5e5ed12d6))
		- ```go
		  package main
		  
		  import "fmt"
		  
		  func show_binary(v any) {
		  	fmt.Printf("\n%b\n", v)
		  }
		  
		  func main() {
		  	var shrt int8 = -128
		  	show_binary(shrt)
		  }
		  
		  ```
	- ## 3 Conversions Between Signed and Unsigned
		- konw before
		  ((6282e2c2-144e-42c8-99ca-744a7ffaace8))
		  ((6282e2cf-3b6a-4600-9ee8-30fce5a81de9))
		- how conversion work
		  ((6282e414-1cf6-4a7f-97e6-b0948772c5f7))
		  ![IMG_09E569885198-1.jpeg](../assets/IMG_09E569885198-1_1652745273128_0.jpeg)
		- ((6282e6e3-beb4-491f-b2aa-5640c4e5b510))
		- T2U
		  ((6282ea2b-45bc-4f7e-8831-e372fe606c32))
		  ((6282ea53-a2e8-45c4-a072-3ade6e3a2726))
		- U2T
		  ((6282ea6a-e7ae-4d39-8074-c142a27ce329))
	- ## 4. Signed and Unsigned in Go
		- ```go
		  package main
		  
		  import "fmt"
		  
		  func main() {
		  	var ua uint8 = 0
		  	var ub uint8 = 255
		  	var uc uint8 = 128
		  	var ud uint8 = 1
		  	fmt.Printf("\n%d  == %b  ==  %d  ==  %b", ua, ua, int8(ua), int8(ua))
		  	fmt.Printf("\n%d  == %b  ==  %d  ==  %b", ub, ub, int8(ub), int8(ub))
		  	fmt.Printf("\n%d  == %b  ==  %d  ==  %b", uc, uc, int8(uc), int8(uc))
		  	fmt.Printf("\n%d  == %b  ==  %d  ==  %b", ud, ud, int8(ud), int8(ud))
		  
		  	fmt.Println("==============")
		  
		  	var ia int8 = -128
		  	var ib int8 = -1
		  	var ic int8 = 0
		  	var id int8 = 127
		  	fmt.Printf("\n%d  == %b  ==  %d  ==  %b", ia, ia, uint8(ia), uint8(ia))
		  	fmt.Printf("\n%d  == %b  ==  %d  ==  %b", ib, ib, uint8(ib), uint8(ib))
		  	fmt.Printf("\n%d  == %b  ==  %d  ==  %b", ic, ic, uint8(ic), uint8(ic))
		  	fmt.Printf("\n%d  == %b  ==  %d  ==  %b", id, id, uint8(id), uint8(id))
		  }
		  
		  0  == 0  ==  0  ==  0
		  255  == 11111111  ==  -1  ==  -1
		  128  == 10000000  ==  -128  ==  -10000000
		  1  == 1  ==  1  ==  1==============
		  
		  -128  == -10000000  ==  128  ==  10000000
		  -1  == -1  ==  255  ==  11111111
		  0  == 0  ==  0  ==  0
		  127  == 1111111  ==  127  ==  1111111
		  
		  ```
	- ## 5 Expanding the Bit Representation of a Number
		- Expand the bit for Unsigned
			- just add 0
		- Expand the bit for Two's Complement
			- positive: just add 0
			- negative: just add 1
			- ![IMG_F985AB5EDE93-1.jpeg](../assets/IMG_F985AB5EDE93-1_1652748861417_0.jpeg)
		- Summary
			- ((6282f2cf-79e2-4714-a95a-0c46c23e7c87))
	- ## 6 Truncating Number
		- ((6282f530-5d34-4ee2-ac16-64c754a98c9a))
		- ((6282f522-de2e-4ad4-88f0-2efbe917470a))
	- ## Refer Read
		- [Go Integer Conversion](https://medium.com/a-journey-with-go/go-cast-vs-conversion-by-example-26e0ef3003f0)