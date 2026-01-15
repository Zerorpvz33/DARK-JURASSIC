# DARK JURASSIC - Forum Expansion

This document outlines the recent expansion of the `forum.html` page and provides instructions on how to set up the Firebase integration.

## Changes Made

The `forum.html` page has been completely overhauled to provide a modern, feature-rich, and visually unique experience. The following changes have been made:

- **Expanded HTML Structure:** The `forum.html` file has been expanded to include a more complex and feature-rich layout.
- **Mobile-Friendly Design:** The forum is now fully responsive and optimized for mobile devices.
- **Glitchy & Updated Layout:** The user interface has been updated with a "glitchy" aesthetic, including animations and visual effects.
- **New Features:** The forum now includes a variety of new features, such as:
    - User authentication (login, logout)
    - Real-time fetching of threads and comments
    - Create, read, update, and delete (CRUD) functionality for posts and comments
    - Search and filtering options
    - User profiles with avatars and ranks
    - File attachments for posts
    - Markdown support in posts and comments
    - Notifications for user actions
- **Firebase Integration:** The forum is fully integrated with Firebase for authentication, real-time database, and storage.

## File Structure

The following files have been created or modified:

- `forum.html`: The main HTML file for the forum.
- `style.css`: The CSS file containing all the styles for the forum.
- `firebase-config.js`: The Firebase configuration file.
- `forum.js`: The JavaScript file containing all the logic for the forum.

## Firebase Setup

To use the forum, you will need to set up a Firebase project and update the `firebase-config.js` file with your project's credentials.

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
6. **Update `firebase-config.js`:** Copy your Firebase project's configuration object and paste it into the `firebase-config.js` file, replacing the placeholder values.

## Running the Forum

Once you have set up your Firebase project and updated the `firebase-config.js` file, you can run the forum by opening the `forum.html` file in your web browser.