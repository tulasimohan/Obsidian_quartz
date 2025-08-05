
### PRAM = Prarallel RAM

### CRCW = Concurrent Read Concurrent Write model

### Cell probe

### WordRAM 
- The word-RAM model was designed to mimic what is possible in modern imperative programming languages such as C. 
- In the word-RAM, the memory is divided into words of $Θ(\log n)$ bits. 
- The words have integer addresses and we allow random access to any word in constant time. 
- We also assume all standard word operations from modern programming languages takes constant time.  This includes e.g. integer addition, subtraction, multiplication, division, bit-wise AND, OR, XOR, SHIFT etc. Having $Θ(\log n)$ bit words is a reasonable assumption since machine words on standard computers have enough bits to address the input and to store pointers into a data structure.
- Lower bounds in cell probe model imply lbs in the WRAM model. 

### Communication