# Space Battle Simulator

_Click the 'Fire!' button to unleash random damage on your enemy—and brace for the counterattack! This simple React app pits player against enemy in a turn-based battle until one reaches 0 health!_

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1Tpt1zUiOqred92t4PIJ1NwvmzKv3Szwk" alt="Start Screen" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1mTZHvuMJdsW5T_ICGKewMvjX8zioBL2D" alt="Active" width="500px" />
    </td>
  </tr>
    <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1Xa6JJJByChKLCL2o_ssxtYUkTG3sjB3v" alt="Victory" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=15VaU0rg_kRAWvBCcLnxIVB0bRsklRVhb" alt="Defeat" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1mgnTI7akA_MmlFHomhu1XwJfTCJxdrc2/view?usp=drive_link)

## Practice with React.js:

- State Management
- Component Design
- Prop Drilling
- Event Handling

## Component Design

- Main --> renders App comp
- App --> manages gameState ("active", "gameOver"); renders title (h1) and GameField comp
- GameField --> renders either Active comp or GameOver comp (exclusive) and Message comp --> initializes states for playerHealth, enemyHealth and message
- Active --> active gameplay; dynamically change health values upon click of fire button, message at bottom
- GameOver --> when a health value reaches 0, renders restart button and changes message
- Player --> renders "Player" and health value
- Enemy --> renders "Enemy" and health value
- Message --> renders message bottom of GameField comp
