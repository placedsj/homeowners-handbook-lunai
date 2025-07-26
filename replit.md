# PlACED: The Homeowner's Handbook

## Overview

This is a modern blog application focused on home ownership advice, contractor spotlights, and maintenance guides. The project is built as a full-stack web application using React for the frontend and Express.js for the backend, with a PostgreSQL database managed through Drizzle ORM.

The application serves "The Homeowner's Handbook" - a humorous yet practical guide to home ownership featuring articles, contractor directories, and interactive content.

## User Preferences

Preferred communication style: Simple, everyday language.

## Project Status (January 2025)

✅ **COMPLETED** - Content marketing homeowner's handbook with unlimited SEO-optimized content
✅ **VERIFIED** - User confirmed they love the implementation
✅ **READY** - For business licensing model to other companies

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Styling**: Tailwind CSS with shadcn/ui component library
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state
- **Build Tool**: Vite for development and production builds

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **API Design**: RESTful API endpoints
- **Environment**: Node.js with ES modules
- **Development**: Hot reload with tsx for TypeScript execution

### Database Architecture
- **Database**: PostgreSQL (configured via Drizzle)
- **ORM**: Drizzle ORM with type-safe schema definitions
- **Hosting**: Neon Database (serverless PostgreSQL)
- **Migrations**: Drizzle Kit for schema management

## Key Components

### Content Management
- **Articles**: Blog posts with categories, tags, SEO metadata, and like functionality
- **Categories**: Organized content sections (DIY Disasters, Contractor Chronicles, etc.)
- **Contractors**: Professional directory with ratings and specialties
- **Newsletter**: Email subscription system for weekly tips

### User Interface
- **Navigation**: Sticky header with responsive mobile menu
- **Search**: Full-text search across articles with category filtering
- **Cards**: Responsive article cards with social sharing
- **SEO**: Dynamic meta tags and structured data

### Storage System
- **Memory Storage**: Development-friendly in-memory data store with seeded content
- **Database Ready**: Prepared for PostgreSQL integration via Drizzle schema

## Data Flow

1. **Content Delivery**: Express serves static React build in production
2. **API Requests**: Frontend queries REST endpoints for articles, contractors, categories
3. **Real-time Updates**: TanStack Query manages caching and background refetching
4. **Search & Filtering**: Client-side and server-side filtering for content discovery
5. **Newsletter**: Form submissions handled via API with email validation

## External Dependencies

### Core Technologies
- **Neon Database**: Serverless PostgreSQL hosting
- **Radix UI**: Accessible component primitives
- **Tailwind CSS**: Utility-first styling framework
- **Font Awesome**: Icon library for UI elements

### Development Tools
- **Replit Integration**: Development environment with runtime error overlay
- **TypeScript**: Type safety across the full stack
- **ESLint/Prettier**: Code quality and formatting (implied)

### Third-party Services
- **Unsplash**: Stock photography for articles and hero sections
- **Google Fonts**: Inter and Playfair Display typography

## Deployment Strategy

### Development
- **Local Development**: Vite dev server with Express API proxy
- **Hot Reload**: Both frontend and backend support live reloading
- **Environment Variables**: DATABASE_URL for database connection

### Production
- **Build Process**: Vite builds frontend, esbuild bundles backend
- **Static Serving**: Express serves built React app from dist/public
- **Database**: PostgreSQL via Neon with connection pooling
- **Process Management**: Node.js process serving both API and static files

### Configuration
- **Environment Detection**: NODE_ENV-based configuration
- **Asset Handling**: Separate static asset directory for uploads
- **Path Aliases**: TypeScript path mapping for clean imports

The application follows a monorepo structure with shared TypeScript types between frontend and backend, ensuring type safety across the entire stack. The architecture supports both development flexibility and production scalability.