🦖 Dark Jurassic Network | Technical Briefing

Welcome to the central intelligence hub. This documentation outlines the architecture, features, and security protocols of the Dark Jurassic web ecosystem.

🛰️ Core Infrastructure

Frontend: HTML5, CSS3 (Tailwind-inspired custom styles), JavaScript (ES6+).

Backend: Firebase (Authentication & Real-time Database).

Mapping: Leaflet.js (JS-based interactive geographical tracking).

Design Aesthetic: High-contrast "Cyber-Terminal" (Dark mode, neon red accents, scanline overlays).

📂 Page Directory

1. login.html (Authentication Gate)

Purpose: The entry point for all users.

Logic: Uses Firebase Auth for email/password validation.

Registration: New users are automatically initialized in the database upon account creation.

2. index.html (Command Center)

Purpose: The main dashboard providing an overview of system health.

Features:

Live Intel Feed: Displays recent announcements or global alerts.

Quick Links: Navigation to all sub-modules.

Radar Status: Shows a live summary of the most recent dinosaur sighting.

3. profile.html (Agent Dossier)

Purpose: Personal identity management and career progression.

Key Features:

Name Changer: Allows agents to update their operational codename and bio.

XP Progress Bar: Visualizes distance to the next clearance level.

Rank System: Dynamically calculates titles (e.g., Lab Assistant → Apex Predator) based on XP.

4. sightings.html (Live Tracker)

Purpose: Real-time geographical tracking of escaped biological assets.

Integrations: * Leaflet Map: Renders active markers on a global map.

Live Feed: Displays a chronological list of sightings.

Expiration Logic: Markers and feed items automatically flag as "Expired" after a set duration.

5. dinosaurs.html (Species Database)

Purpose: Collaborative wiki for biological data.

Features:

Public Contributions: Any agent can upload new species data (Name, Diet, Image URL).

Incentive: Users gain +100 XP for every verified database entry.

6. vault.html (Classified Vault)

Purpose: Gated content accessible only to high-ranking agents.

Logic: Compares the user's current XP against the requiredXP of specific files. Locked files remain unreadable until the threshold is met.

7. users.html (Agent Directory)

Purpose: Leaderboard and social proof.

Features: Displays all registered agents sorted by XP, showing their current clearance level and rank.

8. dms.html (Secure Messaging)

Purpose: Encrypted communication between agents.

Logic: Generates a unique chatId based on two usernames (alphabetically sorted) to create private channels.

Mobile Support: Uses visualViewport listeners to ensure the keyboard doesn't break the layout.

9. cards.html (Dino Stones)

Purpose: Tactical training simulation (Mini-game).

Gameplay: A grid-based card battle game where card stats (top, bottom, left, right) determine territory capture.

10. blackmarket.html (XP Exchange)

Purpose: Resource spending module.

Logic: Allows users to trade accumulated XP for "Role Upgrades" or vanity titles, updating the Firebase role field.

🛠️ Database Schema (Firebase)

Node

Purpose

users/{username}

Stores displayName, bio, xp, and role.

sightings/

Stores geolocation data, timestamps, and reporting agent info.

shared_dinos/

Publicly contributed species data.

direct_messages/{chatId}/

Historical message logs between two users.

intel/

Global announcements managed by admin.

⚠️ Security Protocols

Auth Guard: Every sensitive page includes a script to redirect unauthenticated users back to login.html.

Sanitization: Usernames are sanitized (dots to underscores) to comply with Firebase key path restrictions.

Dossier Sync: Profile updates use atomic update() calls to prevent accidental data overwrites.

[END OF BRIEFING]
