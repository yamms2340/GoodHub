# Overview

Goodness Hub is a kindness empowerment platform designed to foster social good within communities. The platform connects people who want to help with those who need assistance, creating a positive ecosystem of giving and sharing. It features personalized good deeds suggestions, a gamified reward system, transparent donation tracking, and community resource matching. The application promotes social impact through technology by making kindness accessible, trackable, and rewarding.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The client-side is built with React and TypeScript, utilizing Vite as the build tool for fast development and optimized production builds. The UI framework leverages shadcn/ui components built on top of Radix UI primitives, providing a consistent and accessible design system. The application uses Wouter for lightweight client-side routing and TanStack Query for efficient data fetching and state management. Real-time features are implemented using Socket.io for live donation tracking and community updates. Styling is handled through Tailwind CSS with a warm, community-focused design theme.

## Backend Architecture
The server follows a Node.js/Express.js architecture with TypeScript for type safety. The application uses a layered approach with separate route handlers and storage abstractions, now utilizing PostgreSQL database with Drizzle ORM for persistent data storage. Socket.io integration provides real-time capabilities for donation tracking and community interactions. The API follows RESTful conventions with proper authentication middleware and comprehensive error handling.

## Data Storage Solutions
The database schema is defined using Drizzle ORM with PostgreSQL as the primary database. Main entities include: users (with karma points and achievement tracking), good deeds (personalized suggestions and completed actions), donations (both item and financial with transparency tracking), help requests (community needs matching), and hall of fame (gamified recognition system). The schema supports complex relationships between users, actions, and community impact metrics.

## Authentication and Authorization
The application implements comprehensive user authentication using session-based approaches with role-based access control. Users can create profiles, track their kindness journey, and build community reputation through verified good deeds and donations. The system supports both authenticated features (personalized suggestions, donation tracking) and public features (browse community needs, view hall of fame).

## External Dependencies
The application integrates with Firebase for additional authentication options and real-time database features. Socket.io enables real-time donation tracking and community updates. The platform includes integration capabilities for payment processing (donation handling) and notification systems. The frontend uses a comprehensive set of Radix UI components optimized for accessibility and positive user experience in community-focused interactions.