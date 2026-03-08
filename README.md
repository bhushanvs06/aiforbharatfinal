# 🧠 Debattlex - Real-Time AI Debate Platform

Debattlex is a **real-time AI-powered debate platform** where users can engage in structured debates with AI or other users in formats like **1v1 and 3v3**.  
The platform is designed to improve **communication, critical thinking, pronunciation, and argumentation skills** through live speech interaction, AI feedback, structured preparation tools, and collaborative debate environments.

---

# 🚀 Live Demo

🔗 **Try Debattlex**  
https://main.d395dqck1v36zk.amplifyapp.com/

**Login Credentials**

📧 Email: `aibh@gmail.com`  
🔒 Password: `aibhwinner`

---

# 🎥 Demo Video

🔗 https://www.youtube.com/watch?v=ulUQXAiJk5g

---

# 🔥 Features

### 🎤 Real-time Speech Recognition
Users interact with the platform using **live voice input** through Speech-to-Text technology.

### 🤖 AI Speakers & Summarization
AI participates in debates and generates **structured speeches and summaries** in real time.

### 🧑‍⚖️ AI Judge System
After debates end, AI analyzes:
- logic
- rebuttal strength
- clarity
- structure  

and gives **detailed feedback and scores**.

### 🧠 Case Preparation with AI
Users can collaborate with AI before debates to:
- build arguments
- generate structured points
- prepare role-specific speeches.

### 🏆 Ranking System
Users can track their:
- debates played
- wins
- performance ranking on the platform.

---

# 🎮 Playground (Pronunciation & Understanding Trainer)

Playground helps users **improve pronunciation and understanding skills**.

Workflow:

1. The user watches a **short educational or debate-related video**.
2. The **mic unlocks** after watching the video.
3. The user explains **what they understood** from the video.
4. AI evaluates:
   - pronunciation
   - fluency
   - clarity
   - understanding
5. AI provides:
   - improvement suggestions
   - pronunciation corrections
   - rating and feedback.

This feature helps users **develop speaking confidence and articulation skills.**

---

# 🧑‍🤝‍🧑 Hangout (Co-Learner Communication)

Hangout allows users to **connect with other learners on the platform**.

Users can:
- join **video calls**
- practice debates
- exchange ideas
- discuss debate motions
- collaborate on arguments

This creates a **community-driven learning environment**.

---

# ⚔️ Debate Modes

### 1️⃣ Arina 1v1
A **one-on-one debate format** where a user debates directly against AI.

### 2️⃣ Arina 3v3
A **full Asian Parliamentary debate simulation** including roles:

- PM
- LO
- DPM
- DLO
- GW
- OW

The interface resembles a **virtual debate room similar to online meeting platforms**.

---

# 📁 Project Structure

```bash
Debattlex/
│
├── client/
│   ├── public/
│   ├── src/
│   │   └── Components/
│   │       ├── Aijudge/        # AI judge feedback module
│   │       ├── Arina/          # Debate UI components
│   │       ├── Caseprep/       # AI case preparation
│   │       ├── Dashboard/      # User dashboard
│   │       ├── Hangout/        # Co-learner communication & video call feature
│   │       ├── Playground/     # Pronunciation & understanding training
│   │       ├── React_bits/     # Reusable components
│   │       ├── dropdown/       # Topic/role selectors
│   │       └── login/          # Authentication
│   │
│   └── package.json
│
├── server/        # Main backend server
├── server2/       # Secondary backend server (testing)
```

---

# 🧰 Technologies Used

## 💻 Frontend

- React.js
- React Router DOM
- Axios
- Web Speech API

---

## 🧪 Backend

- Node.js
- Express.js

Two backend servers are used:

| Server | Port | Purpose |
|------|------|------|
| server | 5000 | Main API server |
| server2 | 5001 | Secondary / testing server |

---

## 🗄️ Database

**AWS DynamoDB**

Used for storing:

- user profiles
- debate transcripts
- summaries
- prep points
- judge feedback
- rankings

---

## 🤖 AI Integration

- Sarvam AI
- Speech-to-Text (STT)
- Text-to-Speech (TTS)

Used for:

- AI speeches
- feedback generation
- pronunciation analysis
- real-time interaction

---

## ☁️ Hosting & Infrastructure

Debattlex is deployed using **AWS cloud services**.

| Service | Purpose |
|------|------|
| AWS Amplify | Frontend hosting |
| AWS EC2 | Backend servers |
| AWS DynamoDB | Database |
| Cloudflare | CDN & performance |

---

# 🧪 Local Development Setup

Follow these steps to run Debattlex locally.

---

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/bhushanvs06/Debattlex.git
cd Debattlex
```

---

## 2️⃣ Configure Server Environment

Create a `.env` file inside **server** and **server2**.

Example:

```env
SARVAM_API_KEY=your_sarvam_api_key_here
SARVAM_API_URL=https://api.sarvam.ai/v1/chat/completions
PORT=5000
```

For **server2**:

```env
PORT=5001
```

---

## 3️⃣ Update Frontend API URL

Inside frontend components:

```
client/src/Components/
```

Find:

```javascript
const url = "https://your-production-api-url";
```

Change to:

```javascript
const url = "http://localhost:5000";
```

---

## 4️⃣ Install Dependencies

### Backend

```bash
cd server
npm install
```

```bash
cd ../server2
npm install
```

### Frontend

```bash
cd ../client
npm install
```

---

## 5️⃣ Start Development Servers

### Start Backend Servers

Server 1:

```bash
cd server
npm run dev
```

Server 2:

```bash
cd server2
npm run dev
```

---

### Start Frontend

```bash
cd client
npm start
```

---

## 6️⃣ Access the Application

Frontend  
http://localhost:3000

Backend API (Main)  
http://localhost:5000

Backend API (Testing)  
http://localhost:5001

---

# 🧠 What's New

✨ Revamped **Debate UI** for 1v1 and 3v3 debates  
🎮 Added **Playground for pronunciation and comprehension training**  
🧑‍🤝‍🧑 Added **Hangout for co-learner interaction**  
🏆 Introduced **Ranking System**

---

# 💡 Goal

Debattlex aims to help learners **develop strong communication, reasoning, and debate skills** using AI-powered interactive learning tools.
