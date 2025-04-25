# Jeopardy

_Interactive Jeopardy gameboard. Practice fetching, using and displaying data from an API._

_[Click here to play!](https://jeopardy-wheat.vercel.app/)_

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=18gmGb-n91dfAcRCOq-9wyXiwBy_EIF4J" alt="Game Load" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1SwPCSKh6CNHQndSHcGbJEdB9To7Sp8Bo" alt="Active" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1QjL2YST3bc7izdY8WS7jbWUanypN1s8l/view?usp=drive_link)

## Summary:

**HTML, CSS and JavaScript practice with:**

- DOM manipulation
- Async/Await
- Event handling
- Array and object manipulation
- Error handling
- API integration
- CSS styling

**Key Features:**

- Fetches data from an API for categories and clues.
- Dynamically builds a gameboard with clickable cells that reveal questions and answers.
- Implements the Fisher-Yates shuffle for randomizing categories.
- Manages loading states with spinners and button interactions.
- Handles errors and disables user input to prevent multiple requests.
- Vercel deployment

## Graded by Hatchways Code Reviewer

### _Score: 96/100_

### Comments:

- Consider encapsulating the game logic into a class or module to improve code organization and maintainability.
- The shuffle function could be moved outside of the fillTable function to keep the code DRY if you need to use it elsewhere.
- It's good practice to handle potential errors from API requests with try-catch blocks, which you've done well in the fillTable function.
- You've done a great job separating concerns by having distinct functions for different parts of the game logic.
- To further improve the user experience, consider adding a feature that prevents clicking on the same question multiple times or indicates that a question has already been answered.
- Since the btn event listener is not removed after it's clicked, the user could click the "Start" button multiple times, which would trigger multiple API requests and table renderings. You could disable the button while loading or remove the event listener once the table has been generated.

### Status on Reviewer Recommendations:

[x] Improvements Added
