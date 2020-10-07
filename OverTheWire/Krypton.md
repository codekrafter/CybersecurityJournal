## Kyrpton - Crypotgraphy

# Level 0 - Base 64 Encoding

This level simply requires a base64 string to be decoded

The password for level 1 is `KRYPTONISGREAT`

# Level 1 - ROT13

This level uses simple ROT13 encoding, while mantaining plain text word boundries. By shifting all the letters you can easily get the password

The password for level 2 is `ROTTEN`

# Level 2 - More ROT13

This has a more advanced ROT13 cipher, with a non-13 offset. It has a binary that encodes the argument with the key, and a file that has the encoded password. I encoded `/etc/issue` (just a system text file) with the encode binary, then compared offsets to come up with the key. I then used that to get the password

The password for level 3 is `CAESARISEASY`

# Level 3 - Frequency tables

This level does not provide a way to encode text, and instead provides a few files of sample encoded text. This is crackable by performing a frequency analysis to generate the key.

The password for level 4 is `BRUTE`