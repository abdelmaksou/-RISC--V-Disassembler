This project represents a trial to implement a RISC-V disassemble.

# How to use:
If you want to run it online and open it from your mobile phone, the required statement to run it is (Ngrok http 18080)
The program is implemented as a Web-based application. You can find a friendly Graphical User interface that is easy to interact with. Simply, you can enter the name of the binary file you want to test in the shown text box. Afterwards, you press the "Submit" button to submit the results to the program. Finally, to show the results, you can press the "Show" button.
![alt text](https://i.imgur.com/xOfZLbo.png)

# Dependencies and required libraries
- boost c++
- crow c++
- Ngrok

# Programming Languages Used
- C++
- HTML
- CSS
- JS

# Implementation:
- It depends mainly on reveiving a .bin file with the main function parameters. 
- Afterwards, the program keeps taking input and loading half words while checking whether the current instruction is a half word or not. This is done using the different in the first two bits of the two types of instructions (C, 32 bit). 
- Afterwards, the program calls the corresponding function that processes the 32-bit or the 16-bit instruction based on the output of the previous function. 
- The program begins dividing the instruction word into fields and begins to differentiate between them using fileds like (Opcode, funct2, funct3, funct4 and funct7). 
- Finally, the program outputs a certain command based on the specific case it reaches in the switch case at the end of the call tree.

# Limitations:
The program is limited only to 8KB of memory according to what is stated in the handout.

# Known Issues:
There are no issues.

# Contributions:
- Ibrahim Gohar:
    - Developing and testing the instDecExec32() function that processes the RV32C instructions.
    - Developing Web-based UI and Deploy it online using ngrok
    - Developing the function responsible for diffrentiating between 16-bit and 32-bit instructions as well as reading them
    - Using bitmasks to load different immediate values
    - Developing function to map the register to its names
    - Developing function to Label different addresses using maps
- Moneer Maged:
    - managing the project implementation process. 
    - defining a huge map for compressed and non-compressed istruction 
    - defining tasks and assigning deadlines for them. 
    - Developing the function responsible for diffrentiating between 16-bit and 32-bit instructions.
- Abdelaaty Rehab:
    - Developing and testing the instDecExec16() function that processes the RV32C instructions.
    - Maintaining a consistent indentation style across the .cpp files.
    - Testing and fixing issues when faced during manipulating the available test cases.
    - Signing the immediate values when loaded as bytes from the input arguments and when written as output to the user. 
