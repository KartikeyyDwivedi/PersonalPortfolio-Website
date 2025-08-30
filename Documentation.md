# Overview

This is a modern professional portfolio website for Kartikey Dwivedi, a Data Engineer and Web Developer. The application is built as a single-page application (SPA) featuring a comprehensive showcase of skills, projects, certifications, and contact information. The portfolio emphasizes responsive design with both dark and light mode themes, professional typography, and smooth animations to create an engaging user experience.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The frontend is built using React with TypeScript, following a component-based architecture. The application uses modern React patterns including functional components with hooks and follows a clean separation of concerns.

**Key Technologies:**
- React 18 with TypeScript for type safety and modern development
- Vite as the build tool for fast development and optimized production builds
- Wouter for lightweight client-side routing
- TanStack Query for state management and API communication
- Tailwind CSS for utility-first styling with custom design system

**Component Structure:**
- Modular component design with reusable UI components from shadcn/ui
- Custom theme provider for dark/light mode switching
- Responsive navigation with smooth scrolling between sections
- Form handling with validation for contact functionality

**Design System:**
- Custom color palette based on psychological color theory
- Typography using Montserrat for headings and Lato for body text
- CSS custom properties for theme switching
- Consistent spacing and component styling through Tailwind configuration

## Backend Architecture
The backend follows a lightweight Express.js architecture designed to serve the static portfolio and handle specific API endpoints.

**Server Structure:**
- Express.js server with TypeScript for type safety
- Modular route handling with separation of concerns
- Development and production build configurations
- Static file serving for the compiled frontend

**API Endpoints:**
- Resume download endpoint for serving PDF files
- Contact form submission endpoint with validation
- Error handling middleware for graceful error responses

## Data Storage Solutions
The application uses a hybrid storage approach suitable for a portfolio website:

**Database Setup:**
- Drizzle ORM configured for PostgreSQL with Neon Database
- Schema defined for user management (prepared for future authentication)
- Migration system using Drizzle Kit for database versioning

**Current Storage:**
- In-memory storage implementation for development
- File-based asset storage for resume and images
- Prepared for database integration when user features are needed

## Authentication and Authorization
The application has a prepared authentication system using a clean interface pattern:

**Architecture:**
- Storage interface abstraction allowing easy switching between implementations
- User schema with username/password fields
- Session management preparation with connect-pg-simple
- Zod validation schemas for type-safe data handling

**Current State:**
- Authentication routes prepared but not actively used
- Portfolio content is publicly accessible
- Contact form doesn't require authentication

## External Dependencies

**UI and Styling:**
- shadcn/ui component library for consistent, accessible UI components
- Radix UI primitives for low-level accessible components
- Tailwind CSS for utility-first styling
- Lucide React for consistent iconography

**Development Tools:**
- TypeScript for type safety across the application
- ESBuild for production bundling
- PostCSS with Autoprefixer for CSS processing
- Replit-specific plugins for development environment integration

**Database and ORM:**
- Drizzle ORM for type-safe database operations
- @neondatabase/serverless for PostgreSQL connection
- Drizzle Kit for schema migrations and management

**Form and Validation:**
- React Hook Form with Hookform Resolvers for form management
- Zod for runtime type validation and schema definition
- Custom validation logic for email and required fields

**Utilities:**
- date-fns for date manipulation
- clsx and tailwind-merge for conditional styling
- nanoid for generating unique identifiers
- Class Variance Authority for component variant management