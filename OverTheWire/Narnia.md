## Narnia - Binary Exploitation

# Level 0 - Overflow

This problem creates a variable with a special value, creates a buffer (sized to 20 characters), then reads 24 characters into that buffer. It then checks the value of the first variable. Because there is 4 characters of overflow, it can be exploited. Putting a value that is 20 characters long then messing around with bytes to get the right modification yeilds a shell in narnia1, which can be used to find the password.

The password to level 1 is `efeidiedae`

# Level 1 - Basic Shell Codes

This file declares a basic function pointer, and then attempts to fill it up with data in an enviromental variable. It then attempts to execute that function. This is basically executing whatever machine code is in the enviroment variable, so searching a shellcode database with the machine type finds the right shell code, which pops me into a shell where I can `cat` the password file.

The password to level 2 is `nairiepecu`