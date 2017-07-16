# CodeMakers-Advanced-Python-Cryptography
---
Python code used to review CS concepts with campers.

```python
### Filename: CaesarCipher
### Venture Codemakers Advanced
### Summer 2017

def encode(message, n):
    code = ""
    message = message.lower()
    for letter in message:
        c = ord(letter)- n
        if (c < 97):
            c = c + 26
        code = code + chr(c)

    return code

def decode(message, n):
    code = ""
    message = message.lower()
    for letter in message:
        c = ord(letter) + n
        if (c > 122):
            c = c - 26
        code = code + chr(c)

    return code

def brute(message):
    for i in range(26):
        code = ""
        for letter in message:
            c = ord(letter) + i
            if (c > 122):
                c = c - 26
            code = code + chr(c)
        print code

def main():
    cipherText = encode("venture", 3)
    print ("The coded message is: " + cipherText)

    plainText = decode(cipherText, 3)
    print ("The decoded message is: " + plainText)

    brute(cipherText)
    
main()
```

Created by [Andrew Berriault](https://github.com/ABerriault) for *McMaster Venture Engineering & Science*
