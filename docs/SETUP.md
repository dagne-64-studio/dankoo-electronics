# DANKOO ELECTRONICS - Setup Guide

## Prerequisites

- Docker & Docker Compose (recommended)
- Node.js 18+ (for local development)
- npm or yarn
- PostgreSQL 16+ (for local development)
- Redis 7+ (for local development)
- Git

## Quick Start with Docker

### 1. Clone the Repository

```bash
git clone https://github.com/dagne-64-studio/dankoo-electronics.git
cd dankoo-electronics
```

### 2. Configure Environment

```bash
cp .env.example .env
```

Edit `.env` file with your settings.

### 3. Start the Application

```bash
# Start all services
docker-compose up -d

# View logs
docker-compose logs -f
```

### 4. Initialize Database

```bash
# Run migrations
docker-compose exec backend npm run db:migrate

# Seed demo data
docker-compose exec backend npm run db:seed
```

### 5. Access the Application

- **Frontend**: http://localhost:3000
- **Admin Dashboard**: http://localhost:3000/admin
- **API**: http://localhost:3001/api
- **API Docs**: http://localhost:3001/api/docs

## Local Development Setup

### Backend Setup

1. Navigate to backend directory
   ```bash
   cd backend
   npm install
   ```

2. Configure environment
   ```bash
   cp .env.example .env.local
   ```

3. Start development server
   ```bash
   npm run start:dev
   ```

### Frontend Setup

1. Navigate to frontend directory
   ```bash
   cd frontend
   npm install
   ```

2. Configure environment
   ```bash
   cp .env.example .env.local
   ```

3. Start development server
   ```bash
   npm run dev
   ```

## Available Commands

```bash
npm run dev              # Start both frontend and backend
npm run build            # Build both projects
npm run test             # Run all tests
npm run lint             # Lint all code
npm run format           # Format all code

npm run docker:up        # Start Docker containers
npm run docker:down      # Stop Docker containers
npm run docker:logs      # View Docker logs
```

## Demo Accounts

After seeding:
- **Customer**: customer@example.com / Password123!
- **Admin**: admin@dankoo-electronics.com / AdminPassword123!
