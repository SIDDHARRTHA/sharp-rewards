📱 Sharp Rewards – Gamified Daily Challenge Rewards System

A full-stack rewards platform where users earn tokens by solving daily challenges.
Includes Android app (Java) and Node.js + Express + MongoDB backend.

🚀 Features
🟦 Android App (Java + Retrofit)

User Registration & Login

JWT-based authentication

Daily challenge with answer submission

Tokens & streak tracking

Global / Area / City / Country leaderboards

Unlock & redeem rewards

Auto-update user tokens/streak locally

Clean UI with RecyclerViews & Adapters

Uses Retrofit + Gson + OkHttp Logging

🟩 Node.js Backend

User authentication (JWT + bcrypt)

Daily challenge generation & reset cron job

Challenge submission logic

Leaderboard:

Today leaderboard

Global leaderboard (all-time tokens)

Area leaderboard

City leaderboard

Country leaderboard

Rewards listing & redemption

MongoDB (Mongoose models)

CORS + dotenv configured

🧱 Tech Stack
🔹 Frontend (Android)

Java (Android)

Retrofit2 + OkHttp

Gson

RecyclerView / Adapter

SharedPreferences

🔹 Backend

Node.js

Express.js

MongoDB + Mongoose

Bcrypt

JSON Web Token (JWT)

Cron Scheduler

📁 Project Structure
SharpRewards/
│── backend/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── cron/
│   ├── server.js
│   └── package.json
│
└── android-app/
    ├── app/src/main/java/com/example/sharprewards/
    ├── activities/
    ├── adapters/
    ├── models/
    ├── api/
    ├── AndroidManifest.xml
    └── build.gradle

⚙️ Installation & Setup
1️⃣ Clone the repository
git clone https://github.com/YOUR_USERNAME/sharp-rewards.git
cd sharp-rewards

2️⃣ Backend Setup
Install dependencies:
cd backend
npm install

Create .env file:
JWT_SECRET=your_secret_here
MONGO_URI=mongodb://localhost:27017/sharprewards

Start backend:
node server.js


Backend Default URL → http://192.168.X.X:5000

3️⃣ Android App Setup

Inside Android Studio:

Open the android-app directory

Update RetrofitClient.java base URL:

private static final String BASE_URL = "http://YOUR_LOCAL_IP:5000/";


Run the app on a device/emulator connected to same WiFi.

🏆 Leaderboard Logic
Global Leaderboard

Sorted by:

Total tokens earned (all-time)

Area / City / Country Leaderboards

Filters today’s leaderboard based on user’s location

Real-time updated

🎁 Rewards System

Users can redeem rewards with:

Unique coupon codes

Token deduction

Immediate DB update

🔐 Authentication Flow

✔ Register → Save User → Login
✔ JWT returned
✔ Token saved in SharedPreferences
✔ Sent in each secure request (optional upgrade)

🌙 Cron Jobs

Daily reset of:

Challenge question

Leaderboard for the current day

💻 Screenshots (Optional)

Add screenshots of your app interface here.

👨‍💻 Author

Siddharrtha Shankar
📍 India

⭐ Contribute

Fork

Create branch

Commit changes

Create PR

📝 License

MIT License
