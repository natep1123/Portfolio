# [Cipher Encrypt](https://github.com/natep1123/Cipher-Encrypt)

_Tool for encrypting/decrypting messages using a custom letter-shift algorithm. Input a message and a shift value (1-144), then hit "Encrypt." Enjoy the encrypting animations!_

<table>
  <tr>
    <td style="padding-right: 20px;">
      <img src="https://drive.google.com/uc?export=view&id=1TpXQ6xmEiJO9nEEf5oZzPz1hZEg5SmSC" alt="Cipher Encrypt (on load)" style="height: 350px; width: 250px;" />
    </td>
    <td>
      <img src="https://drive.google.com/uc?export=view&id=1FJaPJO5BbIwCqlUkN6stxYqk0lPRZ3NS" alt="Cipher Encrypt (active)" style="height: 350px; width: 250px;" />
    </td>
  </tr>
</table>

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

Key Features:

- **Custom Letter-Shift Algorithm:** Encrypts and decrypts messages using a unique up/down letter-shifting method with random letter insertions.
- **Interactive UI:** Input your message and shift value, hit "Encrypt," and watch the encryption animation in action.
- **Modular Design:** Built with a clear separation of concerns.
- **Dynamic Text Animations:** Engaging animations are applied to the title continuously, and to buttons during encryption and decryption processes.
- **Flexible Shift Values:** Supports shift values between 1 and 144 for varied encryption results.
- **Handles Non-Letters:** Non-alphabetic characters (e.g., punctuation) are preserved unchanged, making it robust for real-world text.
- **Decryption:** Includes functionality to reverse the encryption process and retrieve the original message.

## Algorithms:

Side Notes:

- It takes advantage of the modulus operator (%) to "wrap" around the alphabet (e.g. "z", shift: 1 => "a")
- In the case of non-letters, it passes them directly to the new string without change (e.g. "a ?!", shift: 1 => "b ?!")

### Encryption:

Accepts a message and a shift value (1-144) and does the following:

1. Takes the first letter of the message and shifts **up** the alphabet by the given value (e.g. "a", shift: 1 => "b"), and adds that shifted letter to a new string
2. The second letter is then taken and shifted **down** the alphabet(e.g. "d", shift: 1 => "c"), and added to the new string
3. After the second shift, a **random** letter is then inserted (also randomized to be either capital or lowercase)
4. It repeats the sequence --**up shift, down shift, random letter**-- until the message length is achieved
5. Finally, it displays the new message

### Decryption:

Accepts a message and a shift value (1-144) and does the following:

1. It takes the first letter and shifts **down** the alphabet with the given shift value, then adds toa new string
2. It shifts the next letter **up** the alphabet and adds it to the new string
3. The third letter is **skipped** entirely to avoid random letters //--> Note: decrypting multiple times in a row will result in removal of non-random letters
4. It repeats the sequence --**down shift, up shift, skip**-- until the message length is achieved
5. Finaly, it displays the new message
