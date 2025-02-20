# Pokedex

_Displays 10 pokemon cards at a time. Click the button to refresh and get a new set from the pokeAPI._

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1veTJLv9SJEsFr7me8QW_eg-4JmskfriS" alt="Example 1" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1ijinfgkLRLzq0PL0pRirJYgrExnYil8I" alt="Example 2" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1s8RSGV-ya3ueOOhdbU5taEhe9rmcJGki/view?usp=drive_link)

## React.js App practicing:

- State management
- Component design (Pokedex.jsx and PokeCard.jsx)
- Fetcing data from an API
- useEffect hook

## Component Design:

- App --> Pokedex
  - Manages state for pokemon array and loading
  - Initializes function to fetch data from pokeAPI
  - Passes function to child component
  - Renders title, button and either "Loading..." or Pokedex component
- Pokedex --> Pokecard
  - Renders a PokeCard component for each object in the pokeon array
- PokeCard --> renders individual card with pokemon data
