## Note: Binary, Hexadecimal, ASCII, Unicode

### What is Binary?

Computers use binary code to represent and store data. Every thing you see and do on a computer is stored as a massive list of zeros and ones.

### Bits and Bytes

* Each *b*inary dig*it* is called a **bit**.
* 8 bits is one **byte**.
* 1000 bytes is one **kilobyte** (KB).
* 1000 kilobytes is one **megabyte** (MB).
* 1000 megabytes is one **gigabyte** (GB).
* 1000 gigabytes is one **terabyte** (TB).

If you have a file that takes up just 12.5 MB, that is exactly **one billion binary digits**!

### Why do Computers use Binary?

This video thoroughly explains why computers use binary instead of base 10 (the number system we're all familiar with): https://www.youtube.com/watch?v=M41M9ATm49M.

### How do we Translate Numbers and Words into Binary?

The **binary** **numeral system** represents numeric values using only 0s and 1s. All positive integers in base 10 can be represented as a binary number in the binary numeral system.

#### How to convert from base 10 into binary:

1. Write the base 10 number as a sum of powers of 2 (i.e., $2^0$, $2^1$, $2^2$, $2^3$, $2^4$,...).
2. If $2^0$ is in the sum, write a 1. Otherwise write a 0.
3. If $2^1$ is in the sum, write a 1 to the left of the previous digit. Otherwise write a 0 to the left of the previous digit.
4. Repeat step 3 with $2^2$, then $2^3$, all the way up to the largest power of 2 in the sum.

e.g. 27 = 16 + 8 + 2 + 1 = $2^4$ + $2^3$ + $2^1$ + $2^0$, so 27 in binary is 11011.



>  For fun:
>
> Explain this "joke": *There are 10 types of people in this world: Those who understand binary and those who don't.*



#### How to convert from binary into base 10:

1. Label the bits with indices in decreasing order (i.e., ... 4, 3, 2, 1, 0) with the right-most index being 0.
2. For each bit that is a one, calculate two to the power of its index and add these powers of two together.

e.g. 10110 in binary can be represented as $2^4$ + $2^2$ + $2^1$ in base 10, so it's 21.

#### How to convert words into binary:

Every letter can be expressed as an 8-bit string. 

Uppercase letters: Start with 010, then the next 5 characters represent the letter's index in the alphabet.

Lowercase letters: Start with 011, then the next 5 characters represent the letter's index in the alphabet.

The index of A is 1, the index of B is 2, and so on.

#### How to write special characters in binary:

For common special characters such as punctuation marks, whitespace, and some letters with accent, we can look at the ASCII table: http://www.asciitable.com. ASCII stands for American Standard Code for Information Interchange.

For less common special characters, we can look up its Unicode value: https://unicodelookup.com. Unicode covers everything from uncommon punctuation marks to foreign alphabets to math symbols to wingdings to emojis.

### Hexadecimal

Hexadecimal is a base-16 number system. It is a more human-friendly form of binary, since hexadecimal values take up less characters than binary and can be parsed quicker.

The sixteen characters are the digits 0 through 9 and the letters A through F. The letters A through F are not case-sensitive – somestimes they are all upper case and sometimes they are all lower case. Hexadecimal values usually begin with `0x` or `#` or `%` to indicate that it is in hexadecimal.

Hexadecimal values can be used for:

* Addresses of locations in memory.
* Colours. For example, the colour orange is `#FFA500`.
* URLs. For example, `%20` represents a whitespace.
* IP addresses.



>  For fun:
>
>  *Hexspeak* is a collection of words and phrases that only only hexadecimal characters. Among the most popular hexspeak lingo, called "magic numbers" include:
>
>  * 0xDEADBEEF
>  * 0xBADF00D
>  * 0xCAFEBABE
>  * 0xFACEB00C
>
>  0xDEADBEEF is frequently used to indicate a software crash.

