# Rural STEM Games

An educational platform designed for rural communities to learn science, technology, engineering, and mathematics through engaging games.

## Features

- 🎮 Interactive STEM games
- 🏆 Leaderboard system with coin rewards
- 👨‍🎓 Separate login for students and teachers
- 🌍 Multi-language support (English/Spanish)
- 📱 Progressive Web App (PWA) support
- 🎯 Class-based filtering for students (Grades 1-12)

## Setup Instructions

### Prerequisites
- Node.js (v18 or higher)
- PostgreSQL database

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd rural-stem-games
```

2. Install dependencies:
```bash
npm install
```

3. Set up the database:
   - Create a PostgreSQL database named `rural_stem_games`
   - Copy `.env.example` to `.env` and update the database connection string

4. Start the development servers:
```bash
npm run dev:full
```

This will start both the backend server (port 5000) and the frontend development server (port 5173).

### Database Schema

The application automatically creates the following tables:

- `users`: Stores user information (students/teachers)
- `game_scores`: Records game completion and coins earned

### API Endpoints

- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/leaderboard` - Get leaderboard data
- `POST /api/game/complete` - Record game completion
- `GET /api/user/profile` - Get user profile

### User Types

**Students:**
- Must specify their class (1-12)
- Can earn coins by playing games
- Appear on class-specific leaderboards

**Teachers:**
- Can monitor student progress
- Access to all leaderboard views
- Can earn coins through games

## Development

- Frontend: React + TypeScript + Tailwind CSS
- Backend: Node.js + Express + PostgreSQL
- Authentication: JWT tokens
- Internationalization: react-i18next

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License