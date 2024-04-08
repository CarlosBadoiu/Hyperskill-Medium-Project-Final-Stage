Objectives stage 2
----------------------------------------
Write a program that reads an English message and an integer number (key) from
the standard input and shifts each letter by the specified number according to its order in the alphabet.
If you reach the end of the alphabet, start back at the beginning (a follows z).

Objectives stage 3
----------------------------------------
Objectives
Write a program that reads three lines from the standard input: a target operation (enc for encryption, dec for
decryption), a message or a cyphertext, and a key to encrypt/decrypt messages.
All non-letter characters should be encrypted as well as regular letters.
We recommend you get an integer representation of each character (according to the Unicode table) to shift it.
Decompose your program using functions to make it easy to understand and edit later.
One method should encrypt a message and another one should decrypt it according to a key.

Objectives stage 4
-----------------------------------------
Description
Modify the previous program to work with command-line arguments instead of the standard input.
You need to put it in quotes to pass an argument that contains spaces as a single argument.
So "Welcome to hyperskill!" becomes a single Welcome to hyperskill! argument without quotes. You need quotes to pass this argument, but you don't need to remove these quotes in the actual code!

Objectives
The program must parse three arguments: -mode, -key, and -data. The first argument should determine the program's mode (enc for encryption, dec for decryption). The second argument is an integer key to modify the message, and the third is a text or ciphertext to encrypt/decrypt.
Arguments are guaranteed to be passed to the program. If, for some reason, they turn out to be wrong:
If there is no -mode, the program should work in the enc mode;
If there is no -key, the program should consider that it is 0;
If there is no -data, the program should assume that data is an empty string.
Keep in mind that the order of the arguments might be different.
For example, -mode enc maybe at the end, at the beginning, or in the middle of the array.


Objectives stage 5
-------------------------------------------
X-files
Description
In this stage, add the ability to read and write the original and cipher data into files.

Objectives
The program must parse two additional arguments -in and -out to specify the full name of a file to read the data and write the result. Arguments -mode, -key, and -data must work as before.
Your program should read data from -data or from a file specified in the -in argument. That's the reason why you can't have both -data and -in arguments simultaneously.
If there is no -mode, the program should work in the enc mode;
If there is no -key, the program should consider that key is 0;
If there is no -data and no -in the program should assume that the data is an empty string;
If there is no -out argument, the program must print data to the standard output;
If there are both -data and -in arguments, your program should prefer -data over -in.
If there is something strange (an input file does not exist, or an argument doesn't have a value), the program should not fail. Instead, it must display a clear message about the problem and
stop successfully.
The message should contain the word Error.

Objectives stage 6
--------------------------------------------
Choices, choices
Description
Extend your program by adding different algorithms for encoding/decoding. The first one is the shifting algorithm — it shifts each letter by the specified number according to its order in the alphabet.
The second one is based on the Unicode table, like in the previous stage.

Objectives
When starting the program, the necessary algorithm should be specified by an argument (-alg). Name the first algorithm as shift, the second one as unicode. If there is no -alg argument, default it to shift.
Remember that in case of shift, encode only English letters — from "a" to "z" and from "A" to "Z". In other words, after "z" comes "a", after "Z" comes "A".


Explaination
--------------------------------------------------------
For the 2 algorithms shift and unicode(caesar in my code)
I've created 3 maps, one for lowercase letters, and one for
uppercase letters in order to retrieve elements easier
for the encode/decode process of the shift algorithm, and the last
map the ascicode map in which I've put as keys the 128 numbers in the ascii
code and as values the coresponding ascii code so I can retrieve the elements
based on the encoding/decoding of the unicode algorithm(caesar cypher in my code)
With the help of a switch I've handled the inputs corectly for the arguments
-mode -key etc.
In case of missing arguments I've handled the errors or the default values.
Created a file reading/writing mechanism in the process as required in the stage
5.
All 6 stages have been solved and the problem is complete.
I've implemented 4 tests 3 for argument parsed input and 1 for reading from a file
input and writing it to the destination file, the tets are covering
82% of the lines and 87% of the methods as the coverage tool in IntelliJ says.
