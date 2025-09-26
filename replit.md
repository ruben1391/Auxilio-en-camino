# Auxilio en Camino - Roadside Assistance Platform

## Overview

Auxilio en Camino is a roadside assistance platform specifically designed for Argentina, focusing on connecting drivers in need with qualified mechanics. The platform serves three main Argentine provinces: Formosa, Buenos Aires, and Córdoba. It provides a comprehensive solution for emergency vehicle assistance, allowing users to request help and find nearby mechanics, while also enabling mechanics to register and offer their services.

The application features a mobile-first Progressive Web App (PWA) design with offline capabilities, optimized for use during roadside emergencies. It includes functionality for assistance request management, mechanic registration and verification, location-based services, and real-time communication between users and service providers.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The client-side application is built using React with TypeScript, implementing a component-based architecture. The UI framework utilizes shadcn/ui components built on top of Radix UI primitives, providing a consistent and accessible design system. The application uses Wouter for lightweight client-side routing and TanStack Query for efficient data fetching and state management.

The styling approach combines Tailwind CSS for utility-first styling with CSS custom properties for theming. The design system supports both light and dark modes through CSS variables, with a Material Design-inspired elevation system for depth and hierarchy.

### Backend Architecture
The server-side implementation uses Express.js with TypeScript, following a RESTful API design pattern. The architecture separates concerns through distinct layers: route handlers for HTTP request processing, a storage abstraction layer for data persistence, and middleware for request logging and error handling.

The current implementation includes an in-memory storage system for development purposes, with a well-defined interface that can be easily swapped for database persistence. The API follows RESTful conventions with proper HTTP status codes and JSON responses.

### Progressive Web App Features
The application is designed as a PWA with comprehensive mobile support, including a web app manifest for installation, service worker for offline functionality, and responsive design optimized for mobile devices. The PWA configuration includes custom shortcuts for emergency assistance and mechanic discovery.

### Form Handling and Validation
The application implements robust form handling using React Hook Form with Zod schema validation. This approach ensures type safety from the client through to the database layer, with shared schema definitions between frontend and backend for consistency.

### Component Structure
The UI components are organized into a hierarchical structure with reusable base components, compound components for complex interactions, and page-level components that orchestrate business logic. The component library includes specialized components for automotive data entry, location services, and emergency assistance workflows.

### State Management
Client-side state management combines React's built-in state management with TanStack Query for server state synchronization. This approach minimizes client-side state complexity while providing efficient data caching and background updates.

## External Dependencies

### Database and ORM
- **Drizzle ORM**: Type-safe database operations with PostgreSQL dialect
- **Neon Database**: Serverless PostgreSQL database hosting
- **Database Configuration**: Uses environment-based connection strings with migration support

### UI Framework and Styling
- **Radix UI**: Accessible component primitives for complex UI patterns
- **Tailwind CSS**: Utility-first CSS framework for responsive design
- **shadcn/ui**: Pre-built component library with consistent design tokens
- **Lucide React**: Icon library providing automotive and emergency-themed icons

### Development and Build Tools
- **Vite**: Fast build tool with development server and hot module replacement
- **TypeScript**: Static type checking for enhanced developer experience
- **ESBuild**: Fast JavaScript bundler for production builds

### Form and Validation Libraries
- **React Hook Form**: Performant form library with minimal re-renders
- **Zod**: Schema validation library for type-safe data validation
- **@hookform/resolvers**: Integration layer between React Hook Form and Zod

### Routing and Navigation
- **Wouter**: Lightweight React router optimized for mobile applications
- **Location Services**: Browser geolocation API integration for emergency assistance

### Communication Features
- **WhatsApp Integration**: Direct messaging capabilities for mechanic communication
- **Phone Integration**: Click-to-call functionality for emergency situations

### Progressive Web App Infrastructure
- **Service Worker**: Custom service worker for offline functionality and caching
- **Web App Manifest**: PWA configuration for mobile app-like experience
- **Push Notifications**: Browser notification support for assistance updates

### Session and Authentication
- **connect-pg-simple**: PostgreSQL session store for user session management
- **Express Session**: Server-side session handling middleware

The platform is designed to be deployed on modern cloud platforms with support for environment-based configuration and scalable database connections.