## DYNAMIC MEMORY ALLOCATION

#### C malloc() method:

malloc - "memory allocation": 
- returns a point of type void(which can be cast into a pointer of any form)
- syntax: ptr(must be a pointer) = (cast-type*)malloc(byte-size)
- eg int *ptr = (int*)malloc(100 * sizeof(int));
	- allocates 100 * 4(int size) = 400byte of memory
	- ptr holds the address of the first byte of memory
	- ptr can therefore be used to access every other bytes of memory.

file:///C:/Users/vikmo/Desktop/Dynamic%20Memory%20Allocation%20in%20C%20using%20malloc(),%20calloc(),%20free()%20and%20realloc()%20-%20GeeksforGeeks_files/Malloc-function-in-c.png
>>> image ref: geek4geek

PS: If the space is insufficient, allocation fails and ***returns a NULL pointer***
	This phenomenon can be used to check and prevent program crash.


