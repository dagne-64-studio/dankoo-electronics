# DANKOO ELECTRONICS - Full E-Commerce Platform

## Overview

DANKOO ELECTRONICS is a professional, modern, responsive full-stack e-commerce platform for electronics, computers, networking equipment, CCTV/security systems, and technology accessories.

## 🎯 Key Features

### 👥 Customer Features
- 🛍️ Browse and search products across 30+ categories
- 💻 Advanced product filtering (price, brand, rating, availability)
- 🛒 Shopping cart with persistent storage
- 💳 Secure checkout with multiple payment methods
- 👤 User accounts with order history and tracking
- ❤️ Wishlist functionality
- ⭐ Product reviews and ratings
- 🔍 Product comparison tool
- 📱 Fully responsive design (mobile, tablet, desktop)
- 🤖 AI assistant for product recommendations

### 🔐 Admin Features
- 📊 Comprehensive dashboard with analytics
- 🛍️ Product management (CRUD operations)
- 📂 Dynamic category management
- 📦 Inventory management with low-stock alerts
- 📋 Order management and tracking
- 💰 Coupon and discount management
- 👥 Customer management
- 📈 Sales analytics and charts
- 📧 Notification system

## 🏗️ Technology Stack

### Frontend
- **Next.js 14+** - React framework with SSR/SSG
- **React 18+** - UI library
- **TypeScript** - Type safety
- **Tailwind CSS** - Utility-first styling
- **Redux Toolkit** - State management
- **NextAuth** - Authentication

### Backend
- **Node.js** - Runtime
- **NestJS** - Progressive Node.js framework
- **TypeScript** - Type safety
- **PostgreSQL** - Primary database
- **Redis** - Caching and sessions
- **JWT** - Authentication tokens

### DevOps
- **Docker** - Containerization
- **Docker Compose** - Multi-container orchestration

## 📁 Project Structure

```
dankoo-electronics/
├── frontend/                 # Next.js client application
├── backend/                  # NestJS API server
├── database/                 # Database migrations and seeds
├── docker/                   # Docker configuration
├── docs/                     # Documentation
├── docker-compose.yml        # Multi-container setup
├── .env.example              # Environment variables template
├── .gitignore                # Git ignore rules
├── package.json              # Root package.json
└── README.md                 # This file
```

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose
- Node.js 18+ (for local development)
- Git

### Setup with Docker (Recommended)

1. **Clone the repository**
   ```bash
   git clone https://github.com/dagne-64-studio/dankoo-electronics.git
   cd dankoo-electronics
   ```

2. **Configure environment**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

3. **Start the application**
   ```bash
   docker-compose up -d
   ```

4. **Initialize database**
   ```bash
   docker-compose exec backend npm run db:migrate
   docker-compose exec backend npm run db:seed
   ```

5. **Access the application**
   - Frontend: http://localhost:3000
   - Admin: http://localhost:3000/admin
   - API: http://localhost:3001/api

## 📚 Documentation

- [Setup Instructions](./docs/SETUP.md)
- [Database Schema](./docs/DATABASE.md)
- [API Reference](./docs/API.md)
- [Architecture](./docs/ARCHITECTURE.md)

## 🔒 Security Features

- ✅ Password hashing with bcrypt
- ✅ JWT authentication with refresh tokens
- ✅ CORS configuration
- ✅ Input validation and sanitization
- ✅ SQL injection protection via ORM
- ✅ XSS protection
- ✅ Rate limiting on API endpoints
- ✅ Secure file upload validation
- ✅ Environment-based secrets

## 💳 Payment Integration

Architecture supports:
- **Ethiopian Providers**: Telebirr, Chapa, CBE Birr
- **International**: Stripe, PayPal (future)

## 🌐 SEO Features

- Dynamic meta tags for all pages
- Sitemap generation
- Robots.txt configuration
- Open Graph tags
- Canonical URLs
- SEO-friendly URL slugs
- Structured data (Schema.org)

## ⚡ Performance

- 🚀 Server-side rendering (SSR) with Next.js
- 🖼️ Image optimization and lazy loading
- ⚡ Redis caching for frequently accessed data
- 📊 Database query optimization with indexes
- 📄 Pagination for large datasets
- 🗜️ Gzip compression
- 🌍 CDN-ready architecture

## 📞 Support

- Email: support@dankoo-electronics.com
- Phone: +251-9-XXXX-XXXX
- Website: https://dankoo-electronics.com

## 📄 License

All rights reserved. DANKOO ELECTRONICS © 2024

---

**Built with ❤️ for Ethiopian e-commerce**
