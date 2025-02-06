# [Cipher Encrypt](https://github.com/natep1123/Cipher-Encrypt)

_Tool for encrypting/decrypting messages using a custom letter-shift algorithm. Input a message and a shift value (1-144), then hit "Encrypt." Enjoy the encrypting animations!_

[Click here to watch the demo video](https://drive.google.com/file/d/1ufQQWFktzuHCu78mM49wB1hEYVBSkeKw/view?usp=sharing)

## Summary:

HTML, CSS and JavaScript Practice with:

- Algorithmic problem-solving
- Asynchronous programming
- Modular desgin
- Separation of concerns
- DOM manipulation
- Array manipulation (ES6+) //--> algorithms for animating title and button
- String manipulation //--> algorithmsfor encrypting/decrypting messages
- Text animations
- UI design

## Algorithms:

Notes:

- It takes advantage of the modulus operator (%) to "wrap" around the alphabet (e.g. "z", shift: 1 => "a")
- In the case of non-letters, it passes them directly to the new string without change (e.g. "a ?!", shift: 1 => "b ?!")

### Encryption:

Accepts a message and a shift value (1-144) and does the following:

- Takes the first letter of the message and shifts **up** the alphabet by the given value (e.g. "a", shift: 1 => "b"), and adds that shifted letter to a new string
- The second letter is then taken and shifted **down** the alphabet(e.g. "d", shift: 1 => "c"), and added to the new string
- After the second shift, a **random** letter is then inserted (also randomized to be either capital or lowercase)
- It repeats the sequence --**up shift, down shift, random letter**-- until the message length is achieved
- Finally, it displays the new message

### Decryption:

Accepts a message and a shift value (1-144) and does the following:

- It takes the first letter and shifts **down** the alphabet with the given shift value, then adds toa new string
- It shifts the next letter **up** the alphabet and adds it to the new string
- The third letter is **skipped** entirely to avoid random letters //--> Note: decrypting multiple times in a row will result in removal of non-random letters
- It repeats the sequence --**down shift, up shift, skip**-- until the message length is achieved
- Finaly, it displays the new message
