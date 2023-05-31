- {{renderer :toc_mhyztpa}}
	- ## 0 Introduce
		- when $|V| << 1$，it's an approximation value
		- IEEE Standard 754, defined how to represent floating-point numbers and the operations performed on them
	- ## 1　Fractional Binary Numbers
		- ((62883b4c-6ce0-4008-aaac-ca0fe250bfb5))
		  ((62885317-964a-41af-acae-bea3963e7398))
	- ## 2　IEEE Floating-Point Representation
		- Exponent: 指数
		- Fraction: 分数
		- ((62885615-3e17-4255-b46d-dfc1944b6d6f))
		- ![IMG_A4F1E846BB05-1.jpeg](../assets/IMG_A4F1E846BB05-1_1653102116138_0.jpeg)
		- ![image.png](../assets/image_1653103157844_0.png)
		- when $exp==0000$, $M=0.ffff$
			- when k-bit $exp==0000$, when 32-bit value ,it means  $V = M \times 2^{-126}$
				- $M_{max}=0.(2^{23}-1) < 1$ ,
				- so $V_{max} =2^{-126}$
				- t means the value is so small , so it means
		- else $exp != 0000$  $M=1.ffff$
			- when k-bit $exp=1111$ , when 32-bit value ,it means  $V = M \times 2^{127}$
				- when $friction=0000$ , meas $M=1$ close to 1
					- so $V=2^{127}$ , it's max value
				- becuse we define max value, when $friction != 0000$, it will be bigger then max value, is's not allowed
					- so is $NaN$
			- when $exp != 1111$
				- it's normalized value
		- ![IMG_B40885B890B0-1.jpeg](../assets/IMG_B40885B890B0-1_1653104972099_0.jpeg)
		-
	- ## 3　Example Numbers
		- ((628d8331-a68a-4fa6-b7fa-d73a290aa3ee))
		- ((628d881b-da4c-4a41-a210-8b98e20f9ee9))
		- ![IMG_1AD5BED3BA5C-1.jpeg](../assets/IMG_1AD5BED3BA5C-1_1653443397743_0.jpeg)
	- ## 4　Rounding
		- ![image.png](../assets/image_1653448020914_0.png)
		- even: 偶数
		- odd: 奇数
	- ## 5　Floating-Point Operations
		- ![image.png](../assets/image_1653449687255_0.png)
		- ![image.png](../assets/image_1653449710010_0.png)
		- 参考：[浮点数处理](https://www.jianshu.com/p/a7700923780d)
		-
	- ## 6　Floating Point in C
-