# Project Management Application

A modern, full-stack project management application built with Next.js, tRPC, Prisma, and NextAuth.js. The application allows teams to manage projects, tasks, and collaborate effectively.

## Features

- 🔐 Secure authentication with NextAuth.js
- 📊 Project and task management
- 👥 Team collaboration
- 🎯 Task assignment and tracking
- 🏷️ Task categorization with tags
- 📱 Responsive design

## Tech Stack

- **Frontend**: Next.js, TailwindCSS, React Query
- **Backend**: tRPC, Prisma, PostgreSQL
- **Authentication**: NextAuth.js
- **Deployment**: SST (Serverless Stack), AWS
- **Testing**: Jest, React Testing Library
- **Type Safety**: TypeScript

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL database
- AWS account (for deployment)
- npm or yarn package manager


```

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd project-management-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up the database:
   ```bash
   npm run db:generate   # Generate Prisma client
   npm run db:push      # Push schema to database
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

## Testing

The project uses Jest and React Testing Library for testing. Run tests with:

```bash
npm run test           # Run all tests
npm run test:watch    # Run tests in watch mode
npm run test:coverage # Run tests with coverage report
```

## Project Structure

```
project-management-app/
├── src/
│   ├── components/    # React components
│   ├── pages/         # Next.js pages
│   ├── server/        # Backend API and database
│   ├── styles/        # Global styles
│   └── utils/         # Utility functions
├── prisma/
│   └── schema.prisma  # Database schema
├── public/            # Static assets
└── tests/            # Test files
```

## API Routes

The application uses tRPC for type-safe API routes:

- `/api/trpc/*` - tRPC API endpoints
- `/api/auth/*` - NextAuth.js authentication endpoints

## Deployment

The application is deployed using SST (Serverless Stack) to AWS.

1. Configure AWS credentials:
   ```bash
   aws configure
   ```

2. Deploy to production:
   ```bash
   npm run sst:deploy -- --stage prod
   ```

3. Remove deployment:
   ```bash
   npm run sst:remove -- --stage prod
   ```

## Database Schema

The application uses the following main models:

- User
- Project
- Task
- Team
- Tag

Refer to `prisma/schema.prisma` for the complete schema.

## Authentication

Authentication is handled by NextAuth.js with the following features:

- Credential authentication
- JWT sessions
- Protected API routes
- Protected pages

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

