# c4ptur3-th3-fl4g
## [Task 1] Translation & Shifting

## Question 1: c4n y0u c4p7u23 7h3 f149?
*13375p34k is, as I’m sure you’ll know, “a system of modified spellings used primarily on the Internet”, where some letters are replaced by numbers and other spellings (as in hax0rz, pwned, and n00b). This is clearly in 1337, no question about it.*
### Flag: can you capture the flag?

## Question 2: 01101100 01100101 01110100 01110011 00100000 01110100 01110010 01111001 00100000 01110011 01101111 01101101 01100101 00100000 01100010 01101001 01101110 01100001 01110010 01111001 00100000 01101111 01110101 01110100 00100001
*Does the series of 1’s and 0’s give it away? This is binary, the “language of computers” as journalists correctly, but all too frequently, point out for the benefit of those not terribly technologically inclined.
I made use of [RapidTables’s Binary to Text Translator.](https://www.rapidtables.com/convert/number/binary-to-ascii.html)for this question, which worked a treat.*

![Example](binary.png?raw=true )
### Flag: lets try some binary out!

## Question 3: MJQXGZJTGIQGS4ZAON2XAZLSEBRW63LNN5XCA2LOEBBVIRRHOM======
*This question deals with Base32 values, base 32 being a number system that is made up of the 26 letters of the English alphabet (A-Z) AS WELL AS the numbers 2–7, allowing for a total of 32 usable characters in each position.*

I used [Base32 Decode Online.](https://emn178.github.io/online-tools/base32_decode.html)

![Example2](https://github.com/y4ssr/c4ptur3-th3-fl4g/blob/main/base%2032.png?raw=true )
### Flag: base32 is super common in CTF’s

## Question 4: RWFjaCBCYXNlNjQgZGlnaXQgcmVwcmVzZW50cyBleGFjdGx5IDYgYml0cyBvZiBkYXRhLg==
*This is in Base64, you can tell because lower case characters are included this time, pretty cut and dry.*
I used  [Base64 Decode and Encode.](https://www.base64decode.org/)

![Example3](https://github.com/y4ssr/c4ptur3-th3-fl4g/blob/main/base64.png?raw=true )
### Flag: Each Base64 digit represents exactly 6 bits of data

## Question 5: 68 65 78 61 64 65 63 69 6d 61 6c 20 6f 72 20 62 61 73 65 31 36 3f
*This is in Hexadecimal, or Base16. Each character is always 1 byte, or 8 bits long, helpfully each hexadecimal number is 4 bits, meaning 2 hex digits can ALWAYS represent a character in ASCII.*
*The way you can tell it’s in hex is the spacing between each couplet and the character set, that is 0–9 then a-f, adding to 16*
I used [RapidTables](https://www.rapidtables.com/convert/number/hex-to-ascii.html) again for this conversion.

![Example](https://github.com/y4ssr/c4ptur3-th3-fl4g/blob/main/HextoASXII.png?raw=true )
### Flag: hexadecimal or base16?

## Question 6: Ebgngr zr 13 cynprf!
*ROT13 is an extremely simple cipher where each letter in a phrase is “rotated” 13 times, so that a letter becomes the letter 13 places after it, for example A <-> N, I <-> V, and so on (my name is Vfnnp, as an extra example you didn’t ask for.) Rot13 is its own inverse because 13 is half 26, there are 26 letters in the alphabet, meaning that the letter A will translate to N and the letter N will translate back to A, making the cipher trivial to break.*
*To speed things up, I used [rot13.com](https://rot13.com/)*

![Example](https://github.com/y4ssr/c4ptur3-th3-fl4g/blob/main/rot13.png?raw=true )
### Flag: Rotate me 13 places!

## Question 7: *@F DA:? >6 C:89E C@F?5 323J C:89E C@F?5 Wcf E:>6DX
*This is a Rot47 cipher, it’s the same basic principle as the Rot13 but instead of using just the letters A-Z, it uses all characters in the ASCII encoding table, A-Z, 0–9, punctuation, and so on.*
*I used [dcode’s decoder](https://www.dcode.fr/rot-47-cipher) for this cipher*

![Example](https://github.com/y4ssr/c4ptur3-th3-fl4g/blob/main/dcode's.png?raw=true )
### Flag: You spin me right round baby right round (47 times)

## Question 8: — . .-.. . -.-. — — — — ..- -. .. -.-. .- — .. — — -. . -. -.-. — — -.. .. -. — .
*It’s Morse code, Dots and dashes, you know? Just obvious I suppose, not much more else to say here
I used [browserling’s Morse code decoder](https://www.browserling.com/tools/morse-to-text)*

![Example](https://github.com/y4ssr/c4ptur3-th3-fl4g/blob/main/morse.png?raw=true )
### Flag: telecommunication encoding

## Question 9: 85 110 112 97 99 107 32 116 104 105 115 32 66 67 68
*This is much the same as the previous translation and decoding questions (using hex and base64 and whatnot) but instead this time we’re using good ol’ reliable base 10, 0–9, what’s known as BCD, or Binary Coded Decimal, where each number represents its value in binary, which is then converted to ASCII and spat out as a series of letters and numbers. Regardless, Base10 is what we’re used to, great stuff.
I returned used [Cryptii’s](https://cryptii.com/pipes/text-decimal) decoder for this task*

![Example](https://github.com/y4ssr/c4ptur3-th3-fl4g/blob/main/crypti.png?raw=true )
### Flag: Unpack this BCD

## Question 10: LS0tLS0gLi0tLS0gLi0tLS0gLS0tLS0gLS0tLS0gLi0tLS0gLi0tLS0gLS0tLS0KLS0t……….
*This question was designed to make sure you were paying attention, the original message was in Base 64, as one can tell from the mixture of upper and lower case characters. this decoded into Morse, which itself decoded into Binary, which then decoded into a ROT47 cipher, which THEN decoded to decimal, and FINALLY spat out…*
### Flag: Let’s make this a bit trickier…
