# Star Destroyer

_Stars appear every two seconds, click to destroy! Simple React app to practice using useEffect with setInterval and cleanup functions for periodic updates and event handling._

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1ZImksXAO9AxI4SwRHPp_r0PfyzU3kQ9F" alt="Early Game" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1b34tXwqZk7lc-jJ7AWozUvClzQ80e8ii" alt="Late Game" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1fZi8nZyqMjvYI-c0nSIuHrzniStiL27S/view?usp=drive_link)

## React Hooks:

- **useState** to track and set stars
- **useEffect** to: 1) create new stars every 2 seconds, and 2) focus the stars on mount
- **useRef** to acess star element for focus

## Component Design:

- **Space Component** for: 1) managing state for stars, 2) passing props to child star components, 3) rendering the stars array, and 4) creating a new star every 2 seconds
- **Star Component** which: 1) renders a single star with a random position passed down from Space component, and 2) calls the destroy function on click of that star
