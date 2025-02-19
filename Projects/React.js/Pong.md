# [Pong](https://github.com/natep1123/Pong)

_Classic Pong game! Includes animated start screen, dynamic gameplay with variable ball velocity and score tracking, plus a "Game Over" screen. Soon to add paddle controls and database integration._

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=15esx3HIMqiOalXXts_Ty3qfKSA_4-Nyp" alt="Start Screen" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1Vos0BpDOfvzknfCN15jpFVi6bxT_M_9C" alt="Gameplay" width="500px" />
    </td>
  </tr>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=123fr5iKsECr_o28_CZj1ePtZiC4UU9Pt" alt="Dynamic Velocity Values" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1hO1X1AEMrTVH8NcIrMDJF7rBU6Ig_N26" alt="GameOver" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1g_6Vl6GvapNK7SHdZ1wttoHfsBQFVKOP/view?usp=drive_link)

## **Summary**

_In progress_

This is a React-based Pong game featuring dynamic animations, interactive gameplay, and a responsive UI. The game consists of multiple states, including a start screen, a loading countdown, the game field, and a game-over screen. Key mechanics include ball physics, score tracking, and increasing difficulty through velocity changes. Soon to integrate paddles and corresponding game logic, as well as database to score high scores.

## **Game Structure & Components**

### **1. App.jsx (Top-Level Component)**

- Manages game state (`start`, `loading`, `playing`, `gameOver`).
- Handles dynamic title changes and score tracking.
- Uses `useState` for game state updates and `useRef` for score tracking to avoid unnecessary re-renders.

### **2. StartScreen.jsx**

- Initial screen with a "Start" button.
- Clicking the button transitions the game state to `loading`.

### **3. LoadingScreen.jsx**

- Displays a 3-second countdown before transitioning to the game field.

### **4. GameField.jsx (Core Gameplay)**

- Renders the game board, including the ball.
- Uses `.getBoundingClientRect()` to dynamically retrieve boundary sizes.
- Implements ball movement logic, collision detection, and scoring system.

### **5. GameOver.jsx**

- Displays the final score and buttons for "Restart" and "Start Screen", resetting the game state upon click.

### **6. Paddle.jsx**

- **Will** control paddle movement based on user input.

### **7. Ball.jsx**

- Renders ball based on position (x,y) passed down from GameField component.

## **Game Mechanics & Logic**

- Ball starts in the center with a random trajectory (NW, NE, SW, SE).
- Vertical collisions reverse the vertical velocity (`dy`).
- Horizontal collisions reverse horizontal velocity (`dx`).
- Each left/right wall collision incrememnts the score and accelerates the ball.
  - On scores 1-25, velocity increases either 5% or 10% (50/50 chance)
  - After 25, velocity changes every 5 (score = 30, 35, 40, etc.).
  - Late-game velocity has logic to ensure it stays reasonable for user experience (10-20 units).
  - **Comments pulled from GameField.jsx regarding dynamic late-game velocity logic:**
    - {
      - //Quick checks to keep velocity within bounds
      - //--> Keep V between 10-20 to improve user experience while maintaining challenge
      - //--> Higher values can cause frame issues and make the game too difficult
      - //--> If negative, keep V between -10 and -20
      - //--> If positive, keep V between 10 and 20
      - //--> Vx and Vy have different ranges to allow for more horizontal movement
      - //--> Vx stays between 14 and 20 (or neg equivalent); Vy stays between 10 and 16 (or neg equivalent)
      - //--> If Vx or Vy is too high/low, new random value between 15-17 (Vx) or 12-16 (Vy) is assigned
    - }

## **Animation & State Management**

### **GameField Animation (State-Based)**

- Uses `useState` to track ball position and velocity.
- Necessary for handling side effects like score updates and velocity changes.

### **Start Screen Animation (useRef-Based)**

- Uses `useRef` instead of `useState` for smooth animations without triggering re-renders.
- Ideal since this animation doesn't affect UI state changes.

## **Technical Highlights**

- **React Hooks** (`useState`, `useEffect`, `useRef`) for managing game logic and performance optimizations.
- **Modular Component Structure** for reusability and scalability.
