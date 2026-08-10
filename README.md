# 📸 KP Insta

<p align="center">
  <strong>A modern, mobile-first social media web application.</strong>
</p>

<p align="center">
  Built with HTML, CSS, JavaScript and Firebase.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase">
  <img src="https://img.shields.io/badge/Firestore-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Cloud Firestore">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Web-111111?style=flat-square" alt="Platform">
  <img src="https://img.shields.io/badge/Responsive-Mobile%20First-111111?style=flat-square" alt="Responsive">
  <img src="https://img.shields.io/badge/Status-Active-111111?style=flat-square" alt="Status">
</p>

---

## 📖 About

**KP Insta** is a browser-based social media application designed with a modern, mobile-first interface.

The project brings social networking features into a single web application, including user authentication, profiles, posts, Reels, search, direct messaging, group conversations, followers, follow requests, notifications, notes and customizable settings.

The application uses **Firebase Authentication** for user authentication and **Cloud Firestore** for application data and realtime functionality.

---

## ✨ Features

| Feature | Description |
| --- | --- |
| 🔐 Authentication | User registration and login |
| 👤 Profiles | Custom user profiles and profile information |
| 📸 Posts | Create and interact with social posts |
| 🎬 Reels | Full-screen vertical video experience |
| ❤️ Likes | Like posts and Reels |
| 💬 Comments | Comment on Reels and social content |
| 🔎 Search | Search for users |
| 👥 Following | Followers, following and follow requests |
| ✉️ Direct Messages | Realtime one-to-one conversations |
| 👥 Group Chats | Group conversations and group messages |
| 📝 Notes | User notes |
| 🔔 Notifications | Social interaction notifications |
| 🟢 Presence | Online and last-seen functionality |
| ⚙️ Settings | Privacy, notification, chat and display controls |
| 📱 Responsive UI | Designed for mobile and desktop browsers |

---

# 🔐 Authentication

KP Insta uses Firebase Authentication for account management.

### Included

- Account registration
- Username validation
- Username availability checking
- Password validation
- Password confirmation
- Login
- Logout
- Persistent authentication state
- Password change
- Firebase authentication error handling

The application presents a username-based experience while using Firebase Email/Password Authentication internally.

---

# 👤 User Profiles

Users can create and customize their profiles.

### Profile information

- Username
- Avatar
- Emoji profile character
- Bio
- Birthday
- Followers
- Following
- Notes
- Posts
- Reels
- Follow requests

Profiles also include dedicated **Posts** and **Reels** tabs.

---

# 📸 Posts

KP Insta includes a social feed for user-generated posts.

### Post functionality

- Create posts
- Add media
- Add captions
- Like content
- View authors
- Open user profiles
- Delete owned content
- Display content in the home feed

---

# 🎬 Reels

KP Insta includes a dedicated Reels experience for vertical video content.

### Reels features

- Full-screen video viewing
- Vertical scrolling
- Video autoplay
- Sound controls
- Like Reels
- Comment on Reels
- Share Reels
- Send Reels through messages
- Reel profile section
- Delete owned Reels

The current implementation stores Reels in Firestore and supports Reel likes, comments and sharing.

---

# 💬 Direct Messaging

KP Insta includes realtime direct messaging using Cloud Firestore.

### Messaging features

- One-to-one conversations
- Text messages
- Image messages
- Emoji support
- Message reactions
- Typing indicators
- Read receipts
- Unread message indicators
- Online presence
- Last seen information

Messages are stored under individual chat documents and updated using Firestore realtime listeners.

---

# 👥 Group Chats

The application also supports group conversations.

### Group features

- Create groups
- Select members
- Add people
- Group messages
- Group images
- Group information
- Realtime group messaging

Group messages are stored under:

```text
groupChats/{groupId}/messages
