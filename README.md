# 🎭 IMS Connect — Theater Seat Booking App

A web application for browsing shows and booking theater seats, built with React 19 and backed by Firebase. Users can view available seating, select and reserve seats, and manage their bookings through a clean, responsive interface.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Firebase Setup](#firebase-setup)
- [Available Scripts](#available-scripts)
- [Deployment](#deployment)

---

## Overview

IMS Connect is a single-page application that allows theater-goers to browse upcoming shows, view a seat map, and book seats in real time. Authentication is handled via JWT tokens, and seat availability is persisted through Firebase Firestore, ensuring bookings are reflected instantly across all sessions.

---

## Features

- **Show Listings** — Browse available performances with show details
- **Interactive Seat Map** — Visual seat grid with real-time availability status (available / booked / selected)
- **Seat Selection & Booking** — Select one or more seats and confirm a booking in a single flow
- **User Authentication** — Secure login and registration with JWT-based session management
- **Booking Management** — View and cancel existing reservations
- **Responsive Design** — Works across desktop and mobile using Bootstrap 5

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 19, React Router v7 |
| UI | Bootstrap 5, React-Bootstrap |
| Backend / DB | Firebase (Firestore + Hosting) |
| Auth | JSON Web Tokens (jsonwebtoken) |
| HTTP | Axios |
| Runtime | Node.js (Express — `server.js`) |

---

## Getting Started

### Prerequisites

- Node.js v18 or higher
- npm v9 or higher
- A Firebase project (see [Firebase Setup](#firebase-setup))

### Installation

```bash
# Clone the repository
git clone https://github.com/Tonyksebastian/ims_react_app.git
cd ims_react_app

# Install dependencies
npm install
```

### Running Locally

```bash
npm start
```

Opens the app at [http://localhost:3000](http://localhost:3000). The page reloads automatically on file changes.

---

## Project Structure

```
ims_react_app/
├── public/               # Static assets and index.html
├── src/
│   ├── components/       # Reusable UI components (SeatMap, BookingCard, etc.)
│   ├── pages/            # Route-level pages (Home, Shows, Booking, Profile)
│   ├── services/         # Firebase and API service modules
│   ├── context/          # React context for auth and booking state
│   ├── App.js            # Root component and route definitions
│   └── index.js          # Entry point
├── server.js             # Express server (for token handling / API proxy)
├── firebase.json         # Firebase Hosting configuration
├── apphosting.yaml       # Firebase App Hosting configuration
└── package.json
```

---

## Firebase Setup

1. Create a project at [https://console.firebase.google.com](https://console.firebase.google.com)
2. Enable **Firestore Database** and **Authentication** (Email/Password)
3. Copy your Firebase config and create a `.env` file in the project root:

```env
REACT_APP_FIREBASE_API_KEY=your_api_key
REACT_APP_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
REACT_APP_FIREBASE_PROJECT_ID=your_project_id
REACT_APP_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
REACT_APP_FIREBASE_APP_ID=your_app_id
```

4. Install the Firebase CLI if you haven't already:

```bash
npm install -g firebase-tools
firebase login
```

---

## Available Scripts

| Script | Description |
|---|---|
| `npm start` | Start the development server at `localhost:3000` |
| `npm test` | Run the test suite in interactive watch mode |
| `npm run build` | Create an optimised production build in `/build` |
| `npm run eject` | Eject from Create React App (irreversible) |

---

## Deployment

The app is configured for **Firebase Hosting**.

```bash
# Build the production bundle
npm run build

# Deploy to Firebase
firebase deploy
```

The `firebase.json` and `apphosting.yaml` files in the root handle routing and hosting configuration automatically.

---

## Author

**Tony K Sebastian**  
MSc Software Engineering — University of West London  
[GitHub](https://github.com/Tonyksebastian)

---

## License

This project is open source. Feel free to fork and adapt for your own use.
