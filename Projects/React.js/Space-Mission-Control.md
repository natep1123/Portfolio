# Space Mission Control

_React interface for managing space missions by filtering based on status and launching/completing missions._

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1lk3zFxI3Q-qCueyQVQL_bUEScSOIl_-s" alt="All Screen" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1GTfbAlpfhtMZLahJuWi7ZNqlHBNOFHUt" alt="Planned Screen" width="500px" />
    </td>
  </tr>
    <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=13aXryqIqk52MTzbkbCcNKqkhkl0IvKxl" alt="Ongoing Screen" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1fpG38svHmuvtGVq_TYFHSbXPzwQurXvz" alt="Completed Screen" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1Sg8SXUVA1gnwNSlDYcdk-DqJDIR6oWa7/view?usp=drive_link)

## React.js practice with...

- Component design
- State management
- Passing functions as props to child components
- JSX syntax
- CSS styling in React

## Component Design

MissionControl --> MissionFilter, MissionCard, MissionAction

**Details:**

- MissionControl --> top-level component, manages state for missions and filter, renders child components
- MissionFilter --> stores state for STATUSES ["All", "Planned", "Ongoing", "Completed"] and renders a button for each
- MissionCard --> renders a card with mission data
- MissionAction --> renders two buttons for "Launch" and "Complete"
