# Family Fitness Challenge

A 12-week fitness tracking app for family members to log exercise, earn points, and compete on leaderboards.

## Features

- **User Profiles**: Select your name from a dropdown or create a new profile
- **Exercise Logging**: Log minutes with Low/Medium/High intensity (1x/2x/3x points)
- **Weekly Goals**: Start at 150 pts, increasing 15 pts/week
- **Leaderboards**: Individual and team rankings (weekly + all-time)
- **Teams**: Create or join teams to compete together

## Setup

### 1. Create a Firebase Project

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click "Add project" and follow the prompts
3. Name it something like "family-fitness-tracker"

### 2. Enable Realtime Database

1. In your Firebase project, go to "Build" > "Realtime Database"
2. Click "Create Database"
3. Choose your region
4. Start in **test mode** (for family use)

### 3. Get Your Config

1. Go to Project Settings (gear icon)
2. Scroll down to "Your apps"
3. Click the web icon (`</>`) to add a web app
4. Register your app (no hosting needed)
5. Copy the `firebaseConfig` object

### 4. Update index.html

Open `index.html` and replace the placeholder config:

```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT.firebaseapp.com",
    databaseURL: "https://YOUR_PROJECT-default-rtdb.firebaseio.com",
    projectId: "YOUR_PROJECT",
    storageBucket: "YOUR_PROJECT.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

### 5. Set Database Rules (Optional)

For a family app, test mode rules are fine. If you want basic protection:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

## Hosting Options

### GitHub Pages (Free)

1. Create a new GitHub repository
2. Push this folder to the repo
3. Go to Settings > Pages
4. Set source to "main" branch
5. Your site will be at `https://yourusername.github.io/repo-name`

### Local

Just open `index.html` in a browser!

## Challenge Details

- **Start Date**: Monday, February 2, 2026
- **Duration**: 12 weeks
- **Weekly Goals**: 150 pts (Week 1) to 315 pts (Week 12)

### Intensity Levels

| Level | Points/Min | Examples |
|-------|-----------|----------|
| Low | 1x | walking, yoga, errands, bowling |
| Medium | 2x | jogging, rowing, moderate biking, circuit training |
| High | 3x | running, vigorous biking, HIIT |

## Tech Stack

- React 18 (via CDN)
- Tailwind CSS (via CDN)
- Firebase Realtime Database
