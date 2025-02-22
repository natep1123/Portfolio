# [Cipher Encrypt](https://github.com/natep1123/Cipher-Encrypt)

_Tool for encrypting/decrypting messages using a custom letter-shift algorithm. Input a message and a shift value (1-144), then hit "Encrypt" or "Decrypt" to see smooth button and title animations!_

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

HTML, CSS, and JavaScript practice with:

- Algorithmic problem-solving
- Asynchronous programming
- Modular design
- Separation of concerns
- DOM manipulation
- Array manipulation (ES6+) //--> Algorithms for animating title and button
- String manipulation //--> Algorithms for encrypting/decrypting messages
- Text animations
- UI design

Key Features:

- **Custom Letter-Shift Algorithm:** Encrypts and decrypts messages using a unique up/down letter-shifting method with random letter insertions.
- **Interactive UI:** Input your message and shift value, hit "Encrypt" or "Decrypt," and watch smooth animations in action.
- **Modular Design:** Built with a clear separation of concerns.
- **Dynamic Text Animations:** Continuous title animation and button animations during encryption/decryption, optimized for performance.
- **Flexible Shift Values:** Supports shift values between 1 and 144 for varied encryption results.
- **Handles Non-Letters:** Non-alphabetic characters (e.g., punctuation) are preserved unchanged, making it robust for real-world text.
- **Decryption:** Reverses the encryption process to retrieve the original message.

## Algorithms:

Side Notes:

- Uses the modulus operator (%) to "wrap" around the alphabet (e.g., "z", shift: 1 => "a").
- Non-letters pass directly to the new string unchanged (e.g., "a ?!", shift: 1 => "b ?!").

### Encryption:

Accepts a message and a shift value (1-144):

1. Shifts the first letter **up** the alphabet (e.g., "a", shift: 1 => "b"), adds to new string.
2. Shifts the second letter **down** (e.g., "d", shift: 1 => "c"), adds to new string.
3. Inserts a **random** letter (capital or lowercase).
4. Repeats **up shift, down shift, random letter** until message length is reached.
5. Displays the new message.

### Decryption:

Accepts a message and a shift value (1-144):

1. Shifts the first letter **down** the alphabet, adds to new string.
2. Shifts the next letter **up**, adds to new string.
3. **Skips** the third letter to avoid random insertions.
4. Repeats **down shift, up shift, skip** until message length is reached.
5. Displays the new message.

## Animation & Performance:

- **Title Animation**: Continuously shifts "Cipher Encrypt" letter-by-letter up the alphabet (1-12 shifts), looping every ~1.2s.
  - **Optimized**: Uses `requestAnimationFrame` with 100ms throttling—replaces `setTimeout` for smoother, frame-synced DOM updates.
- **Button Animation**: On click, "Encrypt" or "Decrypt" shifts forward then back to the original text (~0.56s).
  - **Optimized**: Uses `requestAnimationFrame` with 40ms throttling—cuts DOM updates from `setTimeout`’s rapid pace, prevents spam clicks with `disabled`.
  - **Note**: Button reverts to "Encrypt" or "Decrypt" after animation—no "Encrypted!" or "Decrypted!" flash in this version.
