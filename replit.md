# Smart Community Health Monitoring - Early Warning System

## Overview

SafeSip is a comprehensive health monitoring platform designed for early detection and prevention of water-borne diseases in communities. The system enables multiple user roles (ASHA workers, health clinics, community members, and health officials) to report health cases, monitor outbreaks, access health awareness content, and manage community health responses through role-based interfaces.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Library**: Shadcn/UI components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom health-themed color palette (blues for trust, greens for health indicators, reds for alerts)
- **Routing**: Wouter for client-side routing
- **State Management**: TanStack React Query for server state management, React Context for role-based access control
- **Forms**: React Hook Form with Zod validation for type-safe form handling
- **Animations**: Framer Motion for smooth transitions and interactions

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ESM modules
- **Database ORM**: Drizzle ORM for type-safe database operations
- **Session Management**: Express sessions with PostgreSQL session store (connect-pg-simple)
- **Development**: Hot module replacement via Vite integration in development mode

### Role-Based Access Control
The system implements a sophisticated role hierarchy:
- **Community Members**: Can report symptoms and water quality issues
- **ASHA Workers**: Community health workers with reporting capabilities
- **Health Clinics**: Access to patient management and clinical reporting
- **Health Officials**: Full dashboard access with analytics and outbreak management

### Database Design
- **Primary Database**: PostgreSQL with Neon Database serverless hosting
- **Schema Management**: Drizzle Kit for migrations and schema management
- **Type Safety**: Drizzle-Zod integration for runtime validation of database schemas
- **Current Schema**: Basic user authentication table (expandable for health case reporting, water quality data, and outbreak tracking)

### Component Design System
- **Design Philosophy**: Health-focused UI inspired by WHO dashboards and emergency response systems
- **Typography**: Inter font family for accessibility and readability
- **Responsive Design**: Mobile-first approach with Tailwind breakpoints
- **Accessibility**: ARIA labels, keyboard navigation, and screen reader support through Radix UI primitives
- **Theming**: Light/dark mode support with CSS custom properties

## External Dependencies

### Database & Infrastructure
- **Neon Database**: Serverless PostgreSQL hosting for production scalability
- **Drizzle ORM**: Type-safe database operations with PostgreSQL dialect

### UI & Component Libraries
- **Radix UI**: Accessible, unstyled UI primitives for complex components (dialogs, dropdowns, forms)
- **Tailwind CSS**: Utility-first CSS framework for consistent styling
- **Lucide React**: Feather-inspired icon library for consistent iconography
- **Framer Motion**: Animation library for enhanced user experience

### Form Management & Validation
- **React Hook Form**: Performant form library with minimal re-renders
- **Zod**: TypeScript-first schema validation for forms and API data
- **@hookform/resolvers**: Integration between React Hook Form and Zod validation

### Development & Build Tools
- **Vite**: Fast build tool with hot module replacement for development
- **TypeScript**: Type safety across the entire application
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS processing with Tailwind integration

### Query & State Management
- **TanStack React Query**: Server state management with caching, background updates, and error handling
- **React Context**: Client-side state management for user roles and application settings

The architecture prioritizes type safety, accessibility, and scalable health data management while maintaining a clean separation between public health information access and secure clinical data handling.