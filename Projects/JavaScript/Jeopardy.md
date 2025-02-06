# Jeopardy

_Interactive Jeopardy gameboard. Practice fetching, using and displaying data from an API._

[Click here to watch the demo video](https://drive.google.com/file/d/1QjL2YST3bc7izdY8WS7jbWUanypN1s8l/view?usp=drive_link)

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
