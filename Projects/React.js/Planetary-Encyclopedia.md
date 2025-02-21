# Planetary Encyclopedia

_A simple React app for exploring key facts about the planets in our solar system. Built with React Router for seamless navigation._

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1KbXDzlv3u7vkNZtJTWtgbWk6egjcKYpF" alt="Home Page" width="500px" />
    </td>
        <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1gChSWVgXaTLi1IfObqD3vxoDWuoRW47_" alt="Venus Page" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1vWNKsYjl3ivx3iFnuM3GfEujLvmXu42H/view?usp=drive_link)

## React Router practice using:

- `BrowserRouter` for routing structure
- `Routes` and `Route` for dynamic page rendering
- `Link` for navigation between pages
- `useNavigate` for programmatic navigation
- Dynamic route generation based on a dataset

## Component Design:

- **App** --> foundation of app, integrates router setup to manage navigation
- **NavBar** --> structures links for users to move between pages
- **HomePage** --> initial landing page
- **ContentPage** --> dynamic component for displaying content based on user selection/navigation; adapts to show different information based on the route
- **NavigateBackButton** --> utility component that allows users to return to previous pages
