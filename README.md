# Goodness Hub

A kindness empowerment platform designed to foster social good within communities. The platform connects people who want to help with those who need assistance, creating a positive ecosystem of giving and sharing.

## Features

### 🌟 Core Functionality
- **Personalized Good Deeds**: AI-powered suggestions based on user preferences and community needs
- **Community Help Requests**: Connect those who need help with willing volunteers
- **Transparent Donations**: Track donations with real-time transparency and impact metrics
- **Hall of Fame**: Gamified recognition system celebrating top contributors

### ⚡ Real-time Features
- Live activity feed showing community actions
- Real-time donation tracking
- Instant notifications for help requests
- Socket.io powered live updates

### 🎮 Gamification
- Karma point system for good deeds
- Achievement badges and categories
- Community leaderboards
- Progress tracking and milestones

## Tech Stack

### Frontend
- **React 18** with TypeScript
- **Vite** for fast development and optimized builds
- **Tailwind CSS** for responsive styling
- **shadcn/ui** components built on Radix UI
- **Framer Motion** for smooth animations
- **TanStack Query** for efficient data fetching
- **Socket.io Client** for real-time features

### Backend
- **Node.js** with Express.js and TypeScript
- **PostgreSQL** database with Drizzle ORM
- **Socket.io** for real-time communication
- **Session-based authentication**
- **RESTful API** design

### Database Schema
- Users with karma tracking and achievements
- Good deeds with categorization and difficulty levels
- Help requests with urgency and financial support
- Donations with transparency tracking
- Hall of fame entries with dynamic rankings

## Getting Started

### Prerequisites
- Node.js 18+ and npm
- PostgreSQL database
- Environment variables (see below)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yamms2340/goodness-hub.git
cd goodness-hub
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
# Database
DATABASE_URL=your_postgresql_connection_string
PGHOST=your_db_host
PGPORT=5432
PGUSER=your_db_user
PGPASSWORD=your_db_password
PGDATABASE=your_db_name
```

4. Push database schema:
```bash
npm run db:push
```

5. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5000`

## Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── lib/            # Utility functions
│   │   ├── pages/          # Page components
│   │   └── main.tsx        # App entry point
│   └── index.html
├── server/                 # Express backend
│   ├── db.ts              # Database connection
│   ├── index.ts           # Server entry point
│   ├── routes.ts          # API routes
│   ├── storage.ts         # Data access layer
│   └── vite.ts            # Vite middleware
├── shared/
│   └── schema.ts          # Database schema and types
└── package.json
```

## API Endpoints

### Good Deeds
- `GET /api/good-deeds` - Get personalized good deed suggestions
- `POST /api/good-deeds/complete` - Mark a good deed as completed

### Help Requests
- `GET /api/help-requests` - Get community help requests
- `POST /api/help-requests` - Create new help request
- `PATCH /api/help-requests/:id` - Update help request status

### Donations
- `GET /api/donations` - Get donation history
- `POST /api/donations` - Create new donation
- `PATCH /api/donations/:id/status` - Update donation status

### Community
- `GET /api/hall-of-fame` - Get hall of fame rankings
- `GET /api/community/stats` - Get community statistics

## Real-time Events

The application uses Socket.io for real-time updates:

- `good_deed_completed` - When someone completes a good deed
- `donation_created` - When a new donation is made
- `help_request_created` - When someone needs help
- `help_request_updated` - When help request status changes

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes and commit: `git commit -m "Add feature"`
4. Push to your branch: `git push origin feature-name`
5. Submit a pull request

## Database Migrations

Use Drizzle ORM for schema changes:

```bash
# Push schema changes to database
npm run db:push

# Generate migrations (if needed)
npm run db:generate

# Apply migrations
npm run db:migrate
```

## Deployment

### Replit Deployment
The project is optimized for Replit deployment with automatic database provisioning and environment setup.

### Other Platforms
For deployment on other platforms:
1. Set up PostgreSQL database
2. Configure environment variables
3. Build the project: `npm run build`
4. Deploy both frontend and backend

## License

MIT License - see LICENSE file for details

## Support

For questions or support, please open an issue on GitHub or contact the maintainers.

---

Made with ❤️ for building stronger communities through technology