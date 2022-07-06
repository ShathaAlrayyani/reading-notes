# cryptography

## Encrypting a message

Imagine Caesar wants to send this message:

- SECRET MEETING AT THE PALACE
  Here's what that might look like encrypted:
- YKIXKZ SKKZOTM GZ ZNK VGRGIK
  That looks an awfully lot like gobbledygook at first, but this encrypted message is actually very related to the
  original text.

The Caesar Cipher is a simple substitution cipher which replaces each original letter with a different letter in the
alphabet by shifting the alphabet by a certain amount.

## Decrypting a message

According to historical records, Caesar always used a shift of 3. As long as his message recipient knew the shift
amount, it was trivial for them to decode the message.

Imagine Caesar sends this message to a comrade:
EHZDUH EUXWXV

## Cracking the cipher

Imagine that a very literate and savvy enemy intercepts one of Caesar's messages.
RZ VMZ WMDIBDIB VGG AJMXZN OJ EJDI RDOC XGZJKVOMV OJ YZAZVO OCZ ZIZHT LPZZI VO OCZ IDGZ YZGOV
That enemy does not know that Caesar always uses a shift of 3, so he must attempt to "crack" the cipher without knowing
the shift.
There are three main techniques he could use: frequency analysis, known plaintext, and brute force.

## Frequency analysis

Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English
language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down
the possible shift amounts based on that.

Understanding Ciphers: The Basis of All Cryptography
*Note: For the purposes of this article, I will refer to messages in an easily readable format as “plaintext” and
encrypted or unreadable messages as “ciphertext”. Please note that the words “encryption” and “cryptography” will also
be used interchangeably”*

Cryptography, at its most fundamental level, requires two steps: encryption and decryption. The encryption process uses
a cipher in order to encrypt plaintext and turn it into ciphertext. Decryption, on the other hand, applies that same
cipher to turn the ciphertext back into plaintext.

Here’s an example of how this works.

Let’s say that you wanted to encrypt a the simple message, “Hello”.

So our plaintext (message) is “Hello”.

We can now apply one of the simplest forms of encryption known as “Caesar’s Cipher” (also known as a shift cipher) to
the message.
