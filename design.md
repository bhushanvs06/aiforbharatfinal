# Debattlex - Design Document

## System Architecture

### High-Level Overview
- **Frontend**: React.js with real-time UI components
- **Backend**: Node.js/Express API with WebSocket support
- **Database**: MongoDB for user data and debate records
- **AI Integration**: Sarvam AI for speech generation and judging
- **Speech Processing**: Web Speech API for voice recognition

### System Flow Chart

```
┌─────────────────┐
│   User Login    │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐    ┌─────────────────┐
│   Dashboard     │───►│  Case Prep      │
│   - History     │    │  - AI Help      │
│   - Stats       │    │  - Save Points  │
└─────────┬───────┘    └─────────────────┘
          │
          ▼
┌─────────────────┐
│  Start Debate   │
│  - Topic Select │
│  - Role Select  │
└─────────┬───────┘
          │
          ▼
┌─────────────────┐    ┌─────────────────┐
│  Live Debate    │◄──►│   AI Speaker    │
│  - Speech→Text  │    │  - Generate     │
│  - Real-time UI │    │  - Text→Speech  │
│  - Timer        │    │  - Respond      │
└─────────┬───────┘    └─────────────────┘
          │
          ▼
┌─────────────────┐    ┌─────────────────┐
│  Save to DB     │◄──►│   AI Judge      │
│  - Transcripts  │    │  - Score        │
│  - Summaries    │    │  - Feedback     │
└─────────┬───────┘    └─────────────────┘
          │
          ▼
┌─────────────────┐
│  Show Results   │
│  - Scores       │
│  - Winner       │
│  - Feedback     │
└─────────────────┘
```

## Frontend Components

### Main Components
- **Arina3v3**: Google Meet-style debate interface with speaker grid
- **Dashboard**: User profile and debate history
- **Caseprep**: AI-assisted argument preparation
- **Aijudge**: Post-debate feedback and scoring display
- **Login/Signup**: User authentication forms

### Key Features
- Real-time speech transcription display
- Live debate timers and speaker transitions
- Responsive design for desktop and mobile
- Audio controls for mic and speaker management

## Backend Design

### API Endpoints
```
Authentication:
POST /api/auth/register
POST /api/auth/login

Debates:
GET /api/debates
POST /api/debates
GET /api/debates/:id

AI Services:
POST /api/ai/generate-speech
POST /api/ai/judge
```

### WebSocket Events
- Real-time transcript updates
- Speaker change notifications
- AI response broadcasting
- Debate status synchronization

## Database Schema

### User Collection
```javascript
{
  email: String,
  displayName: String,
  entries: {
    [slug]: {
      topic: String,
      stance: String,
      userRole: String,
      proposition: { pm: {...}, dpm: {...}, gw: {...} },
      opposition: { lo: {...}, dlo: {...}, ow: {...} },
      winner: String
    }
  }
}
```

### Role Data Structure
```javascript
{
  prepPoints: [String],
  transcript: String,
  summary: String,
  judgeFeedback: {
    feedbackText: String,
    scores: { logic: Number, clarity: Number, ... }
  }
}
```

## AI Integration

### Speech Generation
- Topic and role-based argument creation
- Difficulty level adaptation (Beginner/Intermediate/Advanced)
- Real-time response generation during debates

### Judging System
- Multi-criteria scoring (logic, clarity, relevance, etc.)
- Role-specific feedback generation
- Winner determination based on argument strength

## Real-time Features

### WebSocket Implementation
- Live transcript streaming
- Synchronized speaker timers
- Real-time AI responses
- Multi-user debate coordination

### Speech Processing
- Continuous speech recognition
- Live summarization of speeches
- Audio playback for AI responses

## Deployment

### Production Setup
- **Hosting**: Render.com for full-stack deployment
- **Database**: MongoDB Atlas cloud hosting
- **Environment**: Secure configuration with environment variables
- **Monitoring**: Basic health checks and error logging