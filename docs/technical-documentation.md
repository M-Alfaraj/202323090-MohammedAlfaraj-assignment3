# Technical Documentation

## Project Overview
This assignment is an improved version of my portfolio website from Assignments 1 and 2. It adds interactive features, API integration, stronger JavaScript logic, performance improvements, and uses localStorage to save the current theme, includes a project search feature, and a form validation system that gives feedback while keeping the design responsive and user-friendly.

## Technologies and Tools Used
- HTML: used to create the structure of the website.
- CSS: The styles for the page, create responsive layouts, and add transitions and animations.
- JavaScript: used to add interactivity, validation, API integration, filtering, sorting, state management, and dynamic updates.
- ChatGPT: Used to assist with debugging and suggestions for tasks.

## Features and Functionalities

### 1. Responsive Layout
The website adjusts its layout based on the screen size using media queries to improve usability on different devices.

### 2. Light and Dark Mode Theme Toggle with localStorage
A button in the navigation bar allows the user to switch between light and dark mode.
JavaScript is used to:
- switch between light and dark mode.
- update the button icon.
- save the selected theme using localStorage.
- load the saved theme when the page is reloaded.

### 3. Form Validation and Feedback
The contact form is validated using JavaScript.
The form checks if all fields are filled and if the email format is correct.
If validation fails, an error message is shown. If validation succeeds, a success message is shown.

### 4. Animations and Transitions
The website uses CSS transitions and animations to improve user experience by:
- Adding a hover effect on cards and buttons.
- Animating success and error messages.
- Smooth visual transitions.

### 5. Project Search, Filter, and Sort
The Projects section allows the user to:
- search projects by keyword
- filter projects by type
- sort projects by title

JavaScript compares the entered keyword with each project's `data-search` value and also checks the selected filter and sort options before displaying the results.

Example:
- `FPGA` will show the first project
- `BFS` will show the second project
- selecting `Game` will show the JavaFX project
- using a search or filter with no match will show the `No projects found` message

### 6. Greeting Message Based on the Time of Day
A greeting message is displayed above the navigation bar depending on the time of day.

### 7. GitHub API Integration
The website connects to the GitHub API to fetch public repositories dynamically.

JavaScript is used to:
- send a request using `fetch()` and returns repository data
- sort repositories by the most recently updated
- display up to 6 repositories
- show an error message if the API request fails

### 8. Visitor Name Saving with localStorage
the visitor’s name is saved using `localStorage`, when the contact form is submitted successfully

### 9. Site Viewing Counter
A counter is displayed in the About section to show how long the visitor has been viewing the site.

### 10. Performance Improvements
- using `loading="lazy"` for project images
- keeping image sizes small
- removing repeated CSS and cleaning JavaScript issues like `;;`

## JavaScript Functions

### `toggleTheme()`
Switches between light and dark mode and saves the selected theme in `localStorage`.

### `themeDataHandling()`
Loads the last theme selected by the user when the page reloads.

### `greetingMessage()`
Displays a greeting message based on the time of day.

### `projectSearchControls()`
Handles project search, filtering, and sorting based on user input and selected options.

### `formValidation()`
Validates the contact form and shows either a success message or an error message.

### `loadGitHubRepos()`
Fetches repository data from the GitHub API, sorts it, and displays it in the GitHub section.

### `loadVisitorName()`
Loads the saved visitor name from `localStorage` and displays it in the About section.

### `siteCounter()`
Displays and updates a counter showing how long the visitor has been on the website.

## Learning Outcome
In this assignment, I improved my understanding of JavaScript by learning how to connect to an external API, combine searching, filtering, and sorting logic, use `localStorage` for multiple features, and to create a counter with `setInterval()`. I also improved my understanding of debugging code, state management, and how small performance improvements can make a website more efficient and user-friendly.
