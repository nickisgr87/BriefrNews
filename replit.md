# Brief.r - AI-Powered News Compriser

## Overview

Brief.r is a modern web application that aggregates news from multiple RSS feeds and provides intelligent summaries using AI. The application features a clean, responsive design with categorized news sections including global news, economy, health, sports, pop culture, and editorial content. It integrates with OpenAI's GPT-4 for content summarization and categorization.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter (lightweight client-side routing)
- **State Management**: TanStack Query (React Query) for server state
- **Styling**: Tailwind CSS with custom CSS variables
- **UI Components**: Radix UI primitives with custom shadcn/ui components
- **Build Tool**: Vite with hot module replacement

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **Cloud Database**: Neon Database (serverless PostgreSQL)
- **Session Management**: Built-in session handling with connect-pg-simple
- **Development Server**: Custom Vite integration for SSR-like development experience

### Key Design Decisions
1. **Monorepo Structure**: Shared schema and types between client and server
2. **TypeScript Throughout**: Full type safety across the entire stack
3. **Modern React Patterns**: Hooks, functional components, and query-based state management
4. **Responsive Design**: Mobile-first approach with Tailwind CSS
5. **AI Integration**: OpenAI GPT-4 for content processing and enhancement

## Key Components

### Database Schema
- **Articles Table**: Stores news articles with metadata (title, summary, content, category, source, etc.)
- **Market Data Table**: Stores financial market information
- **Categories**: Predefined news categories (popculture, global, economy, health, sports, editorial)

### News Aggregation System
- **RSS Parser**: Fetches content from multiple news sources (Reuters, BBC, CNN, Bloomberg)
- **AI Processing**: OpenAI integration for summarization and categorization
- **Cron Jobs**: Scheduled news fetching and market data updates
- **Content Filtering**: Duplicate detection and quality filtering

### UI Components
- **Header**: Navigation with search functionality
- **Hero Section**: Featured articles and breaking news
- **News Sections**: Category-specific article grids
- **Market Overview**: Real-time market data display
- **Editorial Section**: Opinion and analysis pieces
- **Search Bar**: Real-time search with query suggestions

## Data Flow

1. **News Ingestion**: RSS feeds are parsed on a scheduled basis
2. **AI Processing**: Articles are summarized and categorized using OpenAI
3. **Database Storage**: Processed articles are stored in PostgreSQL
4. **Frontend Queries**: React Query fetches data from REST endpoints
5. **Real-time Updates**: Market data is updated via scheduled jobs
6. **User Interaction**: Search, filtering, and navigation update the UI state

## External Dependencies

### Core Dependencies
- **Database**: Neon Database (PostgreSQL)
- **AI Services**: OpenAI GPT-4 API
- **UI Framework**: Radix UI components
- **Date Handling**: date-fns for time formatting
- **HTTP Client**: Native fetch API with React Query

### Development Tools
- **Build System**: Vite with TypeScript
- **Code Quality**: ESLint configuration
- **Database Management**: Drizzle Kit for migrations
- **Development Server**: Custom Vite + Express integration

## Deployment Strategy

### Production Build
- **Frontend**: Vite builds static assets to `dist/public`
- **Backend**: esbuild bundles server code to `dist/index.js`
- **Database**: Drizzle handles schema migrations
- **Environment**: Production mode with optimized builds

### Development Environment
- **Hot Reload**: Vite dev server with Express middleware
- **Database**: Local or cloud PostgreSQL instance
- **API Keys**: OpenAI API key for content processing
- **Port Configuration**: Flexible port assignment for development

### Environment Variables
- `DATABASE_URL`: PostgreSQL connection string
- `OPENAI_API_KEY`: OpenAI API authentication
- `NODE_ENV`: Environment mode (development/production)

## Changelog

- July 03, 2025. Initial setup and deployment ready
- Added "Created by Nikunjan" attribution to footer
- Configured domain as briefr-news.com for deployment

## User Preferences

Preferred communication style: Simple, everyday language.
Additional requests: Add attribution to Nikunjan, prepare for deployment with .com domain