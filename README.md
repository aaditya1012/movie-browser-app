# Documentation for Movie Browser Application

## How to Run the Application

### Prerequisites
1. Ensure you have **Node.js** (version 14 or higher) installed on your system.
2. Install a package manager, preferably **npm** or **yarn**.
3. Obtain an API key from [The Movie Database (TMDb)](https://www.themoviedb.org/) by signing up for a free account.

### Steps to Run

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/aaditya1012/movie-browser.git
   cd movie-browser
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   ```
   Or, if you are using Yarn:
   ```bash
   yarn install
   ```

3. **Set Up Environment Variables:**
   - Create a `.env` file in the root directory.
   - Add the following line to the `.env` file:
     ```
     VITE_TMDB_API_KEY=your_api_key_here
     ```
     Replace `your_api_key_here` with the API key you obtained from TMDb.

4. **Start the Development Server:**
   ```bash
   npm run dev
   ```
   Or, if you are using Yarn:
   ```bash
   yarn dev
   ```

5. **Open the Application:**
   - Navigate to `http://localhost:5173/` in your browser.

### Running the Production Build
1. **Build the Application:**
   ```bash
   npm run build
   ```
   Or, if you are using Yarn:
   ```bash
   yarn build
   ```

2. **Preview the Production Build:**
   ```bash
   npm run preview
   ```
   Or:
   ```bash
   yarn preview
   ```

## Design Decisions

### 1. Component-Based Architecture
The application uses a modular component-based structure with React, separating concerns like the header, movie list, and individual movie cards. This makes the application scalable and easier to maintain.

### 2. Responsive UI
The CSS is designed to provide a responsive layout. Components such as the movie cards and search bar adjust dynamically for different screen sizes using CSS flexbox and media queries.

### 3. Infinite Scrolling
Infinite scrolling is implemented on the homepage to fetch and display additional movie data as the user scrolls down. This improves user experience by reducing the need for pagination.

### 4. Favorites Management
Favorites are stored in the browser’s `localStorage`, ensuring persistence across page reloads. Users can mark movies as favorites, and their selection will persist until explicitly removed.

### 5. API Abstraction
API calls to TMDb are abstracted into a separate service (`movieApi.js`) to centralize the logic, making it easier to update or replace in the future.

## Features Implemented

1. **Search Functionality:**
   - Allows users to search for movies by title.
   - Dynamically updates results as the user types in the search bar.

2. **Movie Details Page:**
   - Displays detailed information about a selected movie, including:
     - Title
     - Overview
     - Release Year
     - Ratings
     - Genre
   - The page is styled to resemble Netflix-like movie cards with a background image and overlayed text.

3. **Favorites Management:**
   - Users can mark movies as favorites by clicking the star icon.
   - Favorites are saved in `localStorage` and loaded on application startup.

4. **Header and Navigation:**
   - A fixed header with navigation links to Home and Favorites pages.

## Possible Improvements

1. **Error Handling:**
   - Add comprehensive error messages for API failures (e.g., when the API key is invalid or the network is unavailable).

2. **Pagination Controls:**
   - While infinite scrolling is implemented, adding optional pagination controls can improve accessibility for users who prefer manual navigation.

3. **Favorites Page:**
   - Create a dedicated page to view all favorited movies, with an option to filter or sort them.

4. **Styling Enhancements:**
   - Improve the mobile layout to enhance usability on smaller screens.
   - Add animations or hover effects to the movie cards for a more polished user experience.

5. **Authentication:**
   - Integrate user authentication to allow multiple users to save their personalized favorites list.

6. **Better State Management:**
   - Replace `useState` and `useEffect` with `useReducer` or a state management library like Redux for complex state handling.

7. **Unit Testing:**
   - Add unit tests for critical components and utility functions using Jest or React Testing Library.

8. **Dark Mode:**
   - Provide a toggle for light and dark themes to enhance visual comfort.

## Conclusion
This application demonstrates a robust approach to building a modern movie browsing platform. By addressing the suggested improvements, it can evolve into an even more user-friendly and feature-rich application.

