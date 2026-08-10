📸 KP Insta

<p align="center">
  <strong>A modern, mobile-first Instagram-style social media web application.</strong>
</p><p align="center">
  Built with HTML, CSS, JavaScript and Firebase.
</p><p align="center">"HTML5" (https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
"CSS3" (https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
"JavaScript" (https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
"Firebase" (https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
"Firestore" (https://img.shields.io/badge/Cloud%20Firestore-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)

</p>---

📖 About

KP Insta is a browser-based social media application inspired by modern photo and video sharing platforms.

The project focuses on delivering a mobile-app-like experience directly inside a web browser.

It includes authentication, user profiles, posts, Reels, search, direct messaging, group chats, notifications, followers/following, notes and extensive privacy/settings controls.

The current application uses Firebase Authentication for account authentication and Cloud Firestore for application data and realtime functionality.

---

✨ Features

<div align="center">🔐 Authentication| 👤 Profiles| 📸 Posts
Register & Login| Custom Profiles| Image Posts
Firebase Auth| Followers| Likes & Comments
Password Support| Following| Captions

🎬 Reels| 💬 Messaging| 🔔 Notifications
Full-screen Videos| Direct Chat| Likes
Autoplay| Image Messages| Comments
Reels Controls| Group Chats| Follows

🔎 Search| ⚙️ Settings| 📱 UI
User Search| Privacy Controls| Mobile-first
Profiles| Notification Controls| Responsive
Social Discovery| Chat Controls| Dark UI

</div>---

🚀 Core Functionality

🔐 Authentication

KP Insta provides a multi-step account creation and login system.

Included

- Username registration
- Username availability checking
- Password validation
- Password confirmation
- Firebase Authentication
- Login/logout
- Persistent authentication state
- Password change
- Authentication error handling

User accounts are created through Firebase Authentication and a corresponding user profile is stored in Firestore.

---

👤 Profiles

Each account has a customizable profile.

Profile information

- Username
- Avatar
- Bio
- Birthday
- Followers
- Following
- Notes
- Posts
- Reels
- Follow requests

The profile interface also includes dedicated Posts and Reels tabs.

---

📸 Posts

The application includes a social feed for image-based posts.

Supported functionality

- Create posts
- Image media
- Captions
- Likes
- Comments
- Post deletion
- User profiles
- Feed rendering

---

🎬 Reels

KP Insta provides a dedicated Reels experience.

Reels features

- Full-screen video viewing
- Vertical scrolling
- Autoplay
- Sound controls
- Reel interactions
- Reel comments
- Reel sharing
- Reel deletion
- Profile Reels tab

The Reels section uses a dedicated application view separate from the normal home feed.

---

💬 Direct Messages

Realtime messaging is powered by Firestore.

Features

- One-to-one conversations
- Text messages
- Image messages
- Emoji support
- Message reactions
- Typing indicators
- Read receipts
- Unread message indicators
- Online/presence functionality

The code creates Firestore chat documents containing participants and message metadata, while individual messages are stored beneath the conversation.

---

👥 Group Chats

KP Insta also supports group conversations.

Group features

- Create groups
- Select members
- Add members
- Group names
- Group messages
- Group images
- Group member management

---

🔔 Notifications

The notification system supports social interactions such as:

- ❤️ Likes
- 💬 Comments
- 👥 Follows
- 📩 Follow requests
- 💬 Messages

Users can control notification preferences from Settings.

---

🔎 User Search

Users can search for other accounts and access their profiles.

The application includes a dedicated Search page in the main navigation.

---

📝 Notes

Users can create short notes that are associated with their profile/message experience.

---

⚙️ Settings

KP Insta includes an extensive Settings interface.

Account & Security

- Log out
- Change password
- Switch character profile

Privacy

- Active status
- Private account
- Blocked players

Notifications

- Likes
- Comments
- Follows

Chat

- Reactions
- Typing indicators
- Read receipts
- Font size

Reels

- Reels sound
- Autoplay

Display

- Dark/light appearance
- Custom wallpaper
- Custom logo text

These settings are implemented through the application's Settings interface and persisted through Firestore and/or local storage depending on the setting.

---

📱 Screenshots

«Add your screenshots to "assets/screenshots/" and update the filenames below.»

🏠 Home Feed

<p align="center">
  <img src="assets/screenshots/home.png" width="280" alt="KP Insta Home Feed">
</p>👤 Profile

<p align="center">
  <img src="assets/screenshots/profile.png" width="280" alt="KP Insta Profile">
</p>🎬 Reels

<p align="center">
  <img src="assets/screenshots/reels.png" width="280" alt="KP Insta Reels">
</p>💬 Messages

<p align="center">
  <img src="assets/screenshots/messages.png" width="280" alt="KP Insta Messages">
</p>⚙️ Settings

<p align="center">
  <img src="assets/screenshots/settings.png" width="280" alt="KP Insta Settings">
</p>---

🏗️ Architecture

KP Insta currently uses a lightweight client-side architecture:

Browser
   │
   ├── HTML
   ├── CSS
   └── JavaScript
          │
          ├── Firebase Authentication
          │
          └── Cloud Firestore
                 │
                 ├── Users
                 ├── Posts
                 ├── Comments
                 ├── Likes
                 ├── Chats
                 ├── Group Chats
                 └── Notifications

The current implementation keeps the application UI, styling and JavaScript logic inside "index.html".

---

🔥 Firebase Setup

1. Create a Firebase Project

Open the Firebase Console and create a new project.

Then create/register a Web App inside the Firebase project.

---

2. Enable Authentication

Go to:

Firebase Console
→ Authentication
→ Sign-in method

Enable:

Email/Password

The application uses Firebase's email/password authentication API while presenting usernames to the user.

---

3. Create Firestore Database

Go to:

Firebase Console
→ Firestore Database
→ Create database

Choose the appropriate production/security configuration for your deployment.

---

4. Add Firebase Configuration

Add your Firebase configuration to the application:

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.firebasestorage.app",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};

Then initialize Firebase:

const app = initializeApp(firebaseConfig);
const auth = getAuth(app);
const db = getFirestore(app);

«Never commit private server credentials, service-account keys, or other secrets to GitHub.»

---

🗄️ Firestore Data Structure

The exact complete Firestore schema should be treated as implementation-specific. The structure below represents the collections/entities used or implied by the current application and is also a recommended production organization.

users/
  {uid}

posts/
  {postId}

reels/
  {reelId}

chats/
  {chatId}
    messages/
      {messageId}

groupChats/
  {groupId}
    messages/
      {messageId}

notifications/
  {notificationId}

---

👤 "users"

Example profile document:

{
  uid: "USER_UID",
  username: "username",
  email: "username@kpinsta.local",
  bio: "My bio",
  emoji: "😀",
  avatarUrl: "",
  note: "",
  birthday: "YYYY-MM-DD",

  followers: [],
  following: [],
  followRequests: [],

  notificationSettings: {
    likes: true,
    comments: true,
    follows: true
  },

  createdAt: serverTimestamp(),

  online: false,
  lastSeen: null
}

The current registration code creates a user profile with fields including "uid", "username", "email", "bio", "emoji", "avatarUrl", "note", "birthday", followers/following arrays, follow requests, notification settings and presence fields.

---

💬 "chats"

A direct conversation document can contain:

{
  participants: [
    "USER_UID_1",
    "USER_UID_2"
  ],

  lastMessage: "Hello!",
  lastSender: "USER_UID_1",
  lastAt: serverTimestamp(),

  unreadFor: "USER_UID_2"
}

The current code uses a "chats" collection with participant information and unread-message metadata.

---

✉️ "chats/{chatId}/messages"

Example:

{
  from: "USER_UID",
  to: "OTHER_USER_UID",

  text: "Hello!",

  imageUrl: "",

  createdAt: serverTimestamp()
}

---

👥 "groupChats"

Recommended group document:

{
  name: "My Group",

  members: [
    "USER_UID_1",
    "USER_UID_2",
    "USER_UID_3"
  ],

  lastMessage: "Hello group!",
  lastAt: serverTimestamp()
}

The current application writes group messages under "groupChats/{groupId}/messages".

---

🔒 Firestore Security

Before deploying publicly, configure Firestore Security Rules.

A production application should ensure that:

- Users can only modify their own profiles where appropriate.
- Users cannot delete another user's posts.
- Private-account data is protected.
- Chat messages are readable only by conversation participants.
- Group messages are readable only by group members.
- Notification data is protected.
- Client-side checks are not treated as security boundaries.

«Important: Firebase client configuration is not a substitute for Firestore Security Rules.»

---

🛠️ Local Development

Clone the repository:

git clone https://github.com/YOUR_USERNAME/kp-insta.git
cd kp-insta

Start a local server:

python -m http.server 8000

Open:

http://localhost:8000

Because the project uses JavaScript modules and Firebase, serving the application through a local HTTP server is recommended instead of opening the HTML file directly with "file://".

---

🚀 Deployment

KP Insta can be deployed as a static web application.

Option 1 — Firebase Hosting

Install Firebase CLI:

npm install -g firebase-tools

Login:

firebase login

Initialize Hosting:

firebase init hosting

Choose your Firebase project.

For a single-page application, configure the hosting rewrite appropriately.

Deploy:

firebase deploy

Your application will then be available through your Firebase Hosting URL.

---

Option 2 — GitHub Pages

For a static frontend deployment:

1. Push the project to GitHub.
2. Open repository Settings.
3. Select Pages.
4. Select the deployment branch.
5. Save the configuration.

«Firebase Authentication and Firestore Security Rules must still be configured separately.»

---

Option 3 — Other Static Hosting

The project can also be deployed to a static hosting platform capable of serving HTML/CSS/JavaScript.

Typical deployment flow:

GitHub Repository
       ↓
Static Hosting
       ↓
index.html
       ↓
Firebase Authentication
       ↓
Cloud Firestore

---

📂 Project Structure

Recommended repository structure:

KP-Insta/
│
├── index.html
│
├── assets/
│   └── screenshots/
│       ├── home.png
│       ├── profile.png
│       ├── reels.png
│       ├── messages.png
│       └── settings.png
│
├── README.md
│
└── firebase/
    └── firestore.rules

The current application itself is primarily contained in "index.html".

---

🧪 Development Checklist

Before production deployment:

- [ ] Configure Firebase project
- [ ] Enable Email/Password Authentication
- [ ] Create Firestore Database
- [ ] Configure Firestore Security Rules
- [ ] Test registration
- [ ] Test login/logout
- [ ] Test profile editing
- [ ] Test posts
- [ ] Test comments
- [ ] Test likes
- [ ] Test Reels
- [ ] Test direct messages
- [ ] Test group chats
- [ ] Test notifications
- [ ] Test follow requests
- [ ] Test private-account behavior
- [ ] Test blocked-user behavior
- [ ] Test mobile layouts
- [ ] Test desktop layouts
- [ ] Test Firebase errors
- [ ] Test network/offline behavior
- [ ] Remove development/debug information
- [ ] Verify Firestore security rules
- [ ] Deploy production build

---

📊 Feature Overview

Feature| Status
Firebase Authentication| ✅
User Registration| ✅
Username Availability| ✅
User Profiles| ✅
Posts| ✅
Likes| ✅
Comments| ✅
Reels| ✅
Direct Messaging| ✅
Image Messages| ✅
Group Chats| ✅
User Search| ✅
Followers / Following| ✅
Follow Requests| ✅
Notifications| ✅
Notes| ✅
Online / Presence| ✅
Privacy Settings| ✅
Chat Settings| ✅
Reels Settings| ✅
Responsive UI| ✅

---

🎯 Roadmap

Potential future improvements:

- [ ] Firebase Storage integration
- [ ] Real media upload instead of URL-only media
- [ ] Image compression
- [ ] Video compression
- [ ] Push notifications
- [ ] Advanced content moderation
- [ ] Hashtags
- [ ] Explore page
- [ ] Saved posts
- [ ] Story system
- [ ] Story viewer
- [ ] Advanced profile customization
- [ ] Better offline support
- [ ] Progressive Web App support
- [ ] Improved accessibility
- [ ] Automated testing
- [ ] Production Firestore security rules

---

📜 License

This project is intended primarily for personal and educational development.

Before using or distributing KP Insta commercially, review all third-party libraries, assets, media, trademarks and Firebase configuration associated with your deployment.

---

⭐ Support the Project

If you find this project useful:

⭐ Star the repository

🍴 Fork the project

🐛 Report bugs

💡 Suggest improvements

📖 Improve the documentation

---

👨‍💻 KP Insta

<p align="center"><strong>KP Insta — A social media experience built for the web.</strong>

<br>Made with ❤️ using HTML, CSS, JavaScript & Firebase.

</p>
