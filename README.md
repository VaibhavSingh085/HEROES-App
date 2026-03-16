# HEROES – Community Help & Complaint Reporting App

HEROES is a mobile application that enables citizens to report local issues, request help, and collaborate with nearby helpers in real time. The app aims to build a community-driven system where people can report problems (such as damaged infrastructure, safety issues, or emergencies) and receive assistance from verified volunteers nearby.

The application is built using React Native (Expo) and Firebase services, enabling real-time updates, secure authentication, and location-based filtering.

---

## Features

### Complaint Reporting
Users can create complaints describing local problems in their area.  
Each complaint includes:
- Title and description
- Image proof
- Location data
- Timestamp

This allows other users to view and respond to issues happening nearby.

### Real-time Updates
Complaints and updates appear instantly across devices using Firebase Firestore real-time listeners (`onSnapshot`).  
Users can immediately see newly reported issues or updates without refreshing.

### Helper System
Users can volunteer to help resolve complaints.  
Helpers can mark issues as resolved after assisting the reporter.

### Spam Detection
Users can vote if a complaint appears to be spam or invalid.  
If enough spam votes are received, the complaint can be flagged and hidden from normal users.

### Verification System
Verified users have increased privileges in the system such as improved credibility and expanded access to complaints.

### Leaderboard
A leaderboard ranks users based on their helpful contributions to encourage community participation and recognition.

### Location-based Filtering
Complaints are filtered using location distance:
- Non-verified users can view complaints within **10 km**
- This ensures relevance to the user’s local area.

### Image Upload
Users can attach images while reporting complaints.  
Images are uploaded using the **ImgBB API**.

---

## Tech Stack

**Frontend**
- React Native (Expo)
- React Native Maps
- Expo Location API

**Backend & Services**
- Firebase Authentication
- Firebase Firestore (Real-time database)

**Media Storage**
- ImgBB Image Hosting API

---

## Architecture Overview

The application follows a mobile-first architecture:

User → React Native App → Firebase Authentication → Firestore Database  
                                             ↓  
                                     Real-time updates to users

Key architectural characteristics:
- Real-time database synchronization
- Location-based filtering
- Scalable cloud backend
- Secure user authentication

---

## Core Functional Modules

### Authentication Module
Handles secure login and registration using Firebase Authentication.

### Complaint Management Module
Allows users to:
- Create complaints
- View nearby complaints
- Update complaint status

### Helper Module
Allows volunteers to assist with reported issues and mark them as resolved.

### Spam Moderation Module
Implements community moderation through spam voting.

### Reputation System
Tracks contributions and updates the leaderboard accordingly.

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/heroes-app.git
cd heroes-app

2. Install dependencies
npm install
3. Start the Expo server
npx expo start
4. Run the app

You can run the app on:

Android Emulator

iOS Simulator

Physical device using the Expo Go app

Environment Setup

Create a Firebase project and enable:

Firebase Authentication

Cloud Firestore

Then add your Firebase configuration inside the project.

You will also need an ImgBB API key for image uploads.

Future Improvements

Push notifications for complaint updates

Admin moderation dashboard

Complaint categorization

AI-based spam detection

Heatmap of reported issues

Contributors

Vaibhav Singh

Team Members

License

This project is intended for educational and research purposes.
