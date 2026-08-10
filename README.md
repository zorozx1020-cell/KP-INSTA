KP Insta

A modern, mobile-first Instagram-style social media web application built with HTML, CSS, JavaScript, and Firebase.

KP Insta is designed to provide a familiar social-media experience directly in the browser, including user authentication, profiles, posts, reels, messaging, groups, notifications, search, and customizable settings.

---

✨ Features

🔐 Authentication

- User registration
- Username-based login
- Birthday/date-of-birth setup
- Password creation and confirmation
- Username availability checking
- Firebase Authentication integration
- Persistent login state
- Logout support
- Password change support

The registration flow is divided into multiple steps, including birthday, username, password, and profile setup.

---

👤 User Profiles

Each user can create and customize their own profile.

Features include:

- Username
- Profile avatar
- Custom profile photo
- Bio
- Followers count
- Following count
- Posts count
- Profile notes
- Edit profile
- Profile photo presets
- Custom profile photo URL
- Profile photo cropping
- Posts/Reels profile tabs
- Follow requests

---

📝 Posts

KP Insta includes an Instagram-style post system.

Users can:

- Create posts
- Add image URLs
- Add captions
- Like posts
- Comment on posts
- Delete their own posts
- View post authors
- Open user profiles
- Display posts in the home feed

Posts support image media with responsive layouts and captions.

---

🎬 Reels

A dedicated full-screen Reels experience is included.

Features:

- Full-screen vertical video feed
- Scroll/snap navigation
- Autoplay support
- Video controls
- Mute/unmute
- Like reels
- Comment on reels
- Share/send reels
- Reel captions
- Reel view information
- Delete own reels
- Reel profile section
- Full-screen reel viewer

The application implements a dedicated full-screen reel stage with vertical scroll snapping and responsive video rendering.

---

💬 Direct Messaging

KP Insta includes real-time chat functionality powered by Firebase Firestore.

Users can:

- Send text messages
- Send image URLs
- View chat history
- See unread messages
- Open individual conversations
- Use emoji
- Send images
- View typing indicators
- View seen/read status
- React to messages
- Access chat options

The application stores chat messages in Firestore and uses realtime listeners for message updates.

---

👥 Group Chats

Users can create group conversations.

Group features include:

- Create groups
- Set a group name
- Search users
- Select members
- Add members
- View group members
- Send messages
- Send images
- Group conversation management

---

🟢 Online & Presence System

KP Insta includes user presence functionality.

The application can track:

- Online status
- Last seen information
- Active status
- Unread message indicators

Unread conversations are monitored using Firestore realtime listeners.

---

🔎 Search

The application includes a people-search interface.

Users can:

- Search for people
- Find usernames
- Open user profiles
- Follow users
- Message users

---

🔔 Notifications

KP Insta includes a notification system for social interactions.

Supported notification categories include:

- Likes
- Comments
- Follows
- Follow requests
- Message notifications

Users can also mark notifications as read.

Notification preferences can be controlled from Settings.

---

🗒️ Notes

Users can create short profile notes.

Notes can appear:

- Above the Messages section
- On the user's profile

Users can create, update, or remove their note.

---

⚙️ Settings

The application includes a large settings section.

Account & Security

- Log out
- Change password
- Switch character profile

Privacy & RP Controls

- Active status
- Private account
- Blocked players

Notifications & Sound

- Like notifications
- Comment notifications
- Follow notifications
- Message/ringtone sounds
- Do Not Disturb

Reels & Video

- Reels sound
- Reel autoplay

Display

- Dark mode
- Light mode
- Custom wallpaper URL

Chat

- Message reactions
- Typing indicator
- Read/seen receipts
- Adjustable font size

These options are exposed directly through the application's Settings interface.

---

🎨 UI & Design

KP Insta is designed primarily for mobile devices.

Design characteristics

- Dark modern interface
- Instagram-inspired layout
- Mobile-first design
- Responsive UI
- Rounded cards
- Bottom navigation
- Smooth transitions
- SVG icon system
- Full-screen Reels
- Responsive chat interface
- Safe-area support for modern mobile devices

The application uses a centered mobile layout with a maximum width of approximately 520px while remaining responsive on smaller screens.

---

🧭 Main Navigation

The application provides five main navigation sections:

Section| Description
🏠 Home| Social feed and posts
🔍 Search| Search for users
🎬 Reels| Full-screen video feed
💬 Messages| Direct and group messaging
👤 Profile| User profile and content

The bottom navigation is hidden while viewing the full-screen Reels experience to provide a more immersive interface.

---

🔥 Firebase Integration

KP Insta uses Firebase as its backend.

Firebase services used

- Firebase Authentication
- Cloud Firestore

The project initializes Firebase and imports Firebase Authentication and Firestore modules directly into the application.

Firestore is used for

- User profiles
- Posts
- Comments
- Likes
- Followers/following
- Notifications
- Chats
- Group chats
- Messages
- Presence information

Realtime Firestore listeners are used for functionality such as unread messages and live updates.

---

🛠️ Technologies

Technology| Purpose
HTML5| Application structure
CSS3| UI, responsive design and animations
JavaScript| Application logic
Firebase Authentication| User authentication
Firebase Firestore| Database and realtime data
SVG| Interface icons
LocalStorage| Local application preferences
ES Modules| Firebase module imports

---

📱 Responsive Design

KP Insta is optimized for mobile browsers but also supports larger screens.

The application uses:

- Responsive layouts
- Mobile-first components
- "viewport-fit=cover"
- Safe-area support
- Responsive video rendering
- Mobile bottom navigation
- Responsive chat composer
- Full-screen mobile Reels

On larger displays, the main application is constrained to a mobile-style width for a consistent experience.

---

🚀 Getting Started

1. Download the project

Clone or download this repository.

git clone https://github.com/YOUR_USERNAME/kp-insta.git

2. Open the project

The main application is contained in:

index.html

3. Configure Firebase

Create a Firebase project and enable:

- Firebase Authentication
- Email/Password authentication
- Cloud Firestore

Then replace the Firebase configuration in the JavaScript section with your own project configuration.

4. Run the application

Because the project uses JavaScript modules and Firebase, it is recommended to run it through a local development server.

For example:

python -m http.server 8000

Then open:

http://localhost:8000

---

📂 Project Structure

Current project structure:

KP-Insta/
│
├── index.html
└── README.md

The current implementation keeps the HTML, CSS, UI components, and JavaScript application logic inside "index.html".

---

🔐 Security Note

Firebase configuration is included in the client-side application because Firebase web applications normally expose their client configuration.

However, Firestore Security Rules and Firebase Authentication rules must be configured correctly before deploying the application publicly.

Do not rely on client-side JavaScript alone for authorization or data protection.

---

⚠️ Important

This project currently uses direct media URLs for certain image and video features.

For example, posts and reels can accept direct media URLs from the application's creation interfaces.

For a production application, a dedicated media-storage solution such as Firebase Storage or another secure object-storage service would be recommended.

---

🌟 Project Highlights

KP Insta combines several social-media features into a single browser application:

- 🔐 Authentication
- 👤 Profiles
- 📸 Posts
- 🎬 Reels
- ❤️ Likes
- 💬 Comments
- ✉️ Direct messages
- 👥 Group chats
- 🔔 Notifications
- 🔎 User search
- 📝 Notes
- 👥 Followers/following
- ⚙️ Privacy controls
- 🌙 Dark/Light mode
- 📱 Mobile-first UI
- 🔥 Firebase backend

---

📌 Current Project

Project Name: KP Insta

Platform: Web Browser

Frontend: HTML / CSS / JavaScript

Backend: Firebase

Database: Cloud Firestore

Authentication: Firebase Authentication

UI: Mobile-first social media interface

---

👨‍💻 Author

Created as a personal social-media web application project.

KP Insta

---

📄 License

This project can be adapted and modified for personal or educational use.

Before distributing or deploying it publicly, review the Firebase configuration, database security rules, authentication configuration, and any third-party assets used by the project.
