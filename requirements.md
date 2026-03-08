# Debattlex - Requirements Document

## Project Overview

Debattlex is a real-time AI-powered debate platform where users engage in structured debates with AI or other users in 1v1 and 3v3 formats following Asian Parliamentary structure.

## Core Features Required

### User System
- User registration and login
- Personal dashboard with debate history
- Profile management

### Debate Platform
- Support for 1v1 and 3v3 debate formats
- Asian Parliamentary roles (PM, LO, DPM, DLO, GW, OW)
- Real-time speaker transitions with timers
- Google Meet-style UI with active speaker focus

### Speech & AI Integration
- Real-time speech-to-text conversion
- Live speech summarization
- AI participants that can debate in any role
- Text-to-speech for AI responses
- Multiple difficulty levels (Beginner, Intermediate, Advanced)

### Case Preparation
- AI-assisted argument preparation
- Save prep points by topic and role
- Role-specific suggestions

### Data Management
- Store debate transcripts and summaries
- Organize by topic, stance, and speaker role
- User statistics and history

### AI Judge System
- Automated post-debate judging
- Scoring on multiple criteria (logic, clarity, relevance, etc.)
- Personalized feedback and improvement tips

## Technical Requirements

### Technology Stack
- Frontend: React.js
- Backend: Node.js with Express
- Database: MongoDB with Mongoose
- AI: Sarvam AI integration
- Speech: Web Speech API

### Performance
- Real-time speech processing
- Concurrent debate support
- Responsive design for all devices

### Deployment
- Render.com hosting
- MongoDB Atlas database
- Secure environment configuration