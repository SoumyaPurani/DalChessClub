# Dalhousie Chess Club

This repository contains the source code for the official website of the Dalhousie University Chess Club. It is a full-stack application built with React for the frontend and a Node.js/Express backend, connected to a MySQL database. The website serves as a central hub for club members and enthusiasts, providing information on tournaments, news, events, and educational resources.

## Features

- **Tournament Management:** View current, future, and past tournaments. Users can register for upcoming tournaments, and admins can manage participants.
- **Live Tournament Data:** Display live pairings and standings for ongoing tournaments via embedded iframes.
- **Grand Prix Standings:** A dedicated page to track player points and rankings in the Dalhousie Grand Prix competition.
- **News & Events:** A blog-like section for club news and a schedule for special events like workshops or lectures.
- **Club Information:** Pages for club executives ("Our Members"), a Frequently Asked Questions (FAQ) section, and a list of club champions.
- **Educational Resources:**
    - A digital **Library** of chess books that can be borrowed.
    - A **Daily Tips** page offering strategies for different phases of the game.
    - An integrated daily **Chess Puzzle** from chesspuzzle.net.
- **Admin Dashboard:** A secure, password-protected area for administrators to manage all website content, including:
    - Adding, editing, and deleting tournaments, news, events, FAQs, library books, and club members.
    - Managing mailing list subscribers.
    - Updating links for live tournament data and Grand Prix standings.

## Tech Stack

- **Frontend:** React, React Router, Material-UI, Swiper.js, Axios
- **Backend:** Node.js, Express.js
- **Database:** MySQL / MariaDB
- **Authentication:** JSON Web Tokens (JWT), bcrypt
- **File Uploads:** Multer
- **Email:** Nodemailer

## Getting Started

Follow these instructions to get a local copy of the project up and running.

### Prerequisites

You must have Node.js and npm (Node Package Manager) installed on your system.

- [Node.js](https://nodejs.org/) (which includes npm)

### Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/SoumyaPurani/DalChessClub.git
    ```

2.  **Navigate to the project directory:**
    ```sh
    cd DalChessClub
    ```

3.  **Install dependencies:**
    This command will install both the frontend and backend dependencies listed in `package.json`.
    ```sh
    npm install
    ```

4.  **Database Configuration:**
    The backend server in `src/server.js` is configured to connect to a specific remote database via an SSH tunnel. To run this project with your own data, you will need to modify the MySQL and SSH connection details within `src/server.js` to point to your own database instance.

## Available Scripts

In the project directory, you can run the following commands:

### `npm start`

Runs both the React client and the Express backend server concurrently.
- The React app will run in development mode. Open [http://localhost:3000](http://localhost:3000) to view it in your browser.
- The Node.js server will run on [http://localhost:5001](http://localhost:5001).

The page will reload when you make changes to the frontend. The server will restart automatically when you make changes to the backend files, thanks to `nodemon`.

### `npm run client`

Runs only the frontend React application on `http://localhost:3000`.

### `npm run server`

Runs only the backend Express server on `http://localhost:5001`.

### `npm run build`

Builds the React app for production to the `build` folder. It correctly bundles React in production mode and optimizes the build for the best performance.

### `npm test`

Launches the test runner in the interactive watch mode for the React components.

## Project Structure

The project follows a standard Create React App structure with the backend server integrated into the `src` directory.

```
/
├── public/              # Public assets and index.html
└── src/
    ├── components/      # Reusable React components (AuthGuard, etc.)
    ├── contexts/        # React Context providers (AuthContext)
    ├── forms/           # Admin forms for adding/editing content
    ├── images/          # Static image assets
    ├── pages/           # Top-level page components for each route
    ├── styles/          # CSS stylesheets for components and pages
    ├── App.js           # Main application component with routing
    ├── server.js        # Backend Express server logic and API endpoints
    └── ...              # Other configuration and utility files
