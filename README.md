# DARK JURASSIC

Welcome to the DARK JURASSIC network, a web-based interface for a fictional command and control center. This project is a simulation of a high-tech, dystopian world where users take on the role of agents monitoring a "Dark Jurassic" environment.

## The Concept

The DARK JURASSIC project is an immersive web experience with a dark, futuristic aesthetic. It combines elements of a command terminal, a social forum, a marketplace, and a dinosaur tracking system. The user interface is designed to be "glitchy" and visually unique, with animations, sound effects, and a responsive design that works on both desktop and mobile devices.

## Features

This project is a collection of interconnected pages, each with its own set of features:

- **`index.html`**: The main dashboard and command center. It provides a real-time overview of the system, including:
  - System metrics and server status
  - Live satellite feed and proximity radar
  - A command-line interface for interacting with the system
  - Drone surveillance and comms interception
  - Daily objectives and security alerts

- **`forum.html`**: A full-featured forum for agents to communicate and share intelligence. It includes:
  - User authentication (login, logout)
  - Real-time fetching of threads and comments
  - CRUD functionality for posts and comments
  - Search and filtering options
  - User profiles with avatars and ranks

- **`sightings.html`**: A map-based tracking system for dinosaur sightings.

- **`dinosaurs.html`**: A database of dinosaur species with detailed information.

- **`users.html`**: A directory of registered agents.

- **`blackmarket.html`**: A marketplace for buying and selling in-game items.

- **`vault.html`**: A secure storage area for files and data.

- **`profile.html`**: A page for users to manage their profiles and settings.

## Getting Started

To get started with the DARK JURASSIC project, you will need to set up a Firebase project and configure the application to use your Firebase credentials.

### Firebase Setup

1. **Create a Firebase Project:** If you don't already have one, create a new project in the [Firebase Console](https://console.firebase.google.com/).
2. **Enable Authentication:** In the Firebase Console, go to the "Authentication" section and enable the "Email/Password" sign-in method.
3. **Enable Realtime Database:** In the Firebase Console, go to the "Realtime Database" section and create a new database.
4. **Enable Storage:** In the Firebase Console, go to the "Storage" section and create a new storage bucket.
5. **Get Your Firebase Config:** In the Firebase Console, go to your project's settings and find your Firebase project's configuration object. It will look something like this:
```javascript
const firebaseConfig = {
  apiKey: "AIza...",
  authDomain: "your-project-id.firebaseapp.com",
  databaseURL: "https://your-project-id.firebaseio.com",
  projectId: "your-project-id",
  storageBucket: "your-project-id.appspot.com",
  messagingSenderId: "123...",
  appId: "1:123...:web:abc..."
};
```
6. **Update the Firebase Configuration:** The Firebase configuration is located in a `<script>` tag at the bottom of each HTML file. You will need to replace the placeholder values with your Firebase project's configuration.

### Running the Application

Once you have configured Firebase, you can run the application by opening any of the `.html` files in your web browser. It is recommended to start with `index.html` or `login.html`.

## File Structure

The project is organized into a series of HTML files, each representing a different page of the application. The main files are:

- **`index.html`**: The main dashboard.
- **`forum.html`**: The forum page.
- **`sightings.html`**: The dinosaur sightings tracker.
- **`dinosaurs.html`**: The dinosaur species database.
- **`users.html`**: The agent directory.
- **`dms.html`**: Direct messaging page.
- **`blackmarket.html`**: The black market page.
- **`vault.html`**: The secure vault page.
- **`profile.html`**: The user profile page.
- **`login.html`**: The login page.
- **`style.css`**: The main stylesheet (though some pages have inline styles).
- **`logo.png`**: The project logo.
