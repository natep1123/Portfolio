# Space Travel

_React app for managing spacecraft and planets with Context API and React Router. Users can build, move, and destroy spacecraft, dynamically updating planet populations._

<table>
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1qa6LmircvmjO-fTFYNIB7MyQGvm8y-xK" alt="Home Page" width="500px" />
    </td>
        <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1nB2Dpz9GfYSZM43E538RMyoIDNkMN_wj" alt="Loader" width="500px" />
    </td>
  </tr>

  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1OWSkpWo6qrSYtg0p8POhqPwxsxp7ECPa" alt="Spacecrafts Page" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1Za1DXbbSg5PrkK_VDrWZ6JJLAMutBZD7" alt="Spacecraft Page" width="500px" />
    </td>
  </tr>
 
  <tr>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1adlaOllLNfQOwNd9-0GClFTMPfpZRrRR" alt="Build Spacecraft Form" width="500px" />
    </td>
    <td style="padding: 10px;">
      <img src="https://drive.google.com/uc?export=view&id=1DhuFyvByT29BGQ8UISJQGWlzPhwUkr5q" alt="Planets Page" width="500px" />
    </td>
  </tr>
</table>

[Click here to watch the demo video](https://drive.google.com/file/d/1tfC6vW2x2j1bXtO4CFDQHUlXoQ2jF3DC/view?usp=sharing)

## Graded by Hatchways Code Reviewer

### _Score: 93/100_

### Comments:

- The code makes an appropriate use of context for sharing data across components, allowing the components to remain focused on their logic without worrying about state management.

- Good job implementing error handling for API calls. This is important for providing a smooth user experience and making the app more robust. The catch blocks ensure that errors are logged for debugging.

- The routing structure is organized and easy to follow. By using the createBrowserRouter with nested routes under the root path ("/"), it makes the app structure clear and manageable. Each page has a well-defined route, and the child routes are correctly nested under the App component.

- While there is a wildcard (\*) for undefined routes, there’s no fallback UI for failed routes. If any of the pages or components fail to load due to an error, there’s no user-friendly error message or UI to display. Implementing an error boundary for the routes would ensure that the app can gracefully handle errors in specific routes.

- While the inline styling like style={{ marginTop: "1rem", fontStyle: "italic" }} works, it's generally better practice to define styles in an external or internal CSS file. This will improve maintainability, especially as the app scales.

---

## React.js Breakdown

### Components

#### **NavBar**

A navigation bar linking to `HomePage`, `SpacecraftsPage`, and `PlanetsPage`. Active links are highlighted with smooth hover transitions.

#### **BuildSpacecraftForm**

Form for creating spacecraft with inputs for name, capacity, and an optional image URL. Submission triggers the `buildSpacecraft` function to add the spacecraft and redirects to the `SpacecraftsPage`.

#### **Loader**

A spinner indicating loading states. Used on `SpacecraftsPage` and `PlanetsPage`.

#### **SpacecraftCard**

Displays spacecraft details (name, capacity, image). Clicking navigates to the `SpacecraftPage`. A destroy button removes the spacecraft and adjusts the planet’s population via `destroySpacecraft`.

#### **PlanetCard**

Displays planet details (name, population, associated spacecraft). Allows spacecraft assignment or removal with dynamic population updates.

---

### Context: **ApiDataContext**

Global state management for planets and spacecraft. Key functions include:

- `fetchPlanets` & `fetchSpacecrafts`: Load data into the state.
- `buildSpacecraft`: Adds a new spacecraft to the state.
- `destroySpacecraft`: Removes spacecrafts.
- `moveSpacecraft`: Transfers spacecraft between planets and adjusts populations.
- `resetData`: Clears local storage and reloads data.

Data is loaded on app initialization by calling `fetchPlanets` and `fetchSpacecrafts`.

---

### Pages

#### **HomePage**

Main entry point providing an app overview with navigation links.

#### **SpacecraftsPage**

Displays a list of spacecraft with a navigation button to `BuildSpacecraftPage`. Uses `Loader` if data is fetching. Includes button to reset the data for the app back to initial state.

#### **BuildSpacecraftPage**

Form for spacecraft creation. Submission calls `buildSpacecraft` and redirects to `SpacecraftsPage`.

#### **SpacecraftPage**

Detailed view of a spacecraft. Options to destroy or move the spacecraft are provided.

#### **PlanetsPage**

Displays a list of planets and spacecraft interactions. Populations update dynamically with spacecraft movements. Includes button to reset the data for the app back to initial state.

---

### Routing & Configuration

The app uses `react-router-dom` for route management, with `App` as the root component.

#### Routes:

- **`"/"`** --> `HomePage`
- **`"/spacecrafts"`** --> `SpacecraftsPage`
- **`"/spacecrafts/buildspacecraft"`** --> `BuildSpacecraftPage`
- **`"/spacecrafts/:id"`** --> `SpacecraftPage`
- **`"/planets"`** --> `PlanetsPage`
- **Fallback**: Redirects unknown routes to `HomePage`.

`main.jsx` wraps the app in `ApiDataProvider` and `RouterProvider` for state management and routing.

---

### Services

#### **SpaceTravelApi**

Handles API calls to the mock database.

#### **SpaceTravelMockApi**

Simulates server-side behavior with mock data for planets and spacecraft.
