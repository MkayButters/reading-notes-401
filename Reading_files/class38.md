# Cryptography

- In cryptography, a Caesar cipher, also known as Caesar's cipher, the shift cipher, Caesar's code or Caesar shift, is one of the simplest and most widely known encryption techniques. It is a type of substitution cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet. For example, with a left shift of 3, D would be replaced by A, E would become B, and so on. The method is named after Julius Caesar, who used it in his private correspondence.

- The encryption step performed by a Caesar cipher is often incorporated as part of more complex schemes, such as the Vigenère cipher, and still has modern application in the ROT13 system. As with all single-alphabet substitution ciphers, the Caesar cipher is easily broken and in modern practice offers essentially no communications security.

- The Caesar cipher can be easily broken even in a ciphertext-only scenario. Two situations can be considered:

    1. an attacker knows (or guesses) that some sort of simple substitution cipher has been used, but not specifically that it is a Caesar scheme;
    2. an attacker knows that a Caesar cipher is in use, but does not know the shift value.

- In the first case, the cipher can be broken using the same techniques as for a general simple substitution cipher, such as frequency analysis or pattern words. While solving, it is likely that an attacker will quickly notice the regularity in the solution and deduce that a Caesar cipher is the specific algorithm employed.

- In the second instance, breaking the scheme is even more straightforward. Since there are only a limited number of possible shifts (25 in English), they can each be tested in turn in a brute force attack. One way to do this is to write out a snippet of the ciphertext in a table of all possible shifts – a technique sometimes known as "completing the plain component". The example given is for the ciphertext "EXXEGOEXSRGI"; the plaintext is instantly recognisable by eye at a shift of four. Another way of viewing this method is that, under each letter of the ciphertext, the entire alphabet is written out in reverse starting at that letter. This attack can be accelerated using a set of strips prepared with the alphabet written down in reverse order. The strips are then aligned to form the ciphertext along one row, and the plaintext should appear in one of the other rows.


- Another brute force approach is to match up the frequency distribution of the letters. By graphing the frequencies of letters in the ciphertext, and by knowing the expected distribution of those letters in the original language of the plaintext, a human can easily spot the value of the shift by looking at the displacement of particular features of the graph. This is known as frequency analysis. For example, in the English language the plaintext frequencies of the letters E, T, (usually most frequent), and Q, Z (typically least frequent) are particularly distinctive. Computers can also do this by measuring how well the actual frequency distribution matches up with the expected distribution; for example, the chi-squared statistic can be used.

- For natural language plaintext, there will typically be only one plausible decryption, although for extremely short plaintexts, multiple candidates are possible. For example, the ciphertext MPQY could, plausibly, decrypt to either "aden" or "know" (assuming the plaintext is in English); similarly, "ALIIP" to "dolls" or "wheel"; and "AFCCP" to "jolly" or "cheer" (see also unicity distance).

- With the Caesar cipher, encrypting a text multiple times provides no additional security. This is because two encryptions of, say, shift A and shift B, will be equivalent to a single encryption with shift A + B. In mathematical terms, the set of encryption operations under each possible key forms a group under composition.



[<===BACK](../README.md)
