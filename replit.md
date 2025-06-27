# Burger Justice League

## Overview

This is a React-based idle clicker game called "Burger Justice League" that combines superhero themes with burger production. The game features an incremental gameplay loop where players click to produce burgers, hire superhero characters to automate production, unlock achievements, and progress through a prestige system.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite with custom configuration
- **Styling**: Tailwind CSS with custom theme variables
- **3D Graphics**: React Three Fiber (@react-three/fiber) with Drei utilities
- **State Management**: Zustand with subscribeWithSelector middleware
- **UI Components**: Radix UI primitives with custom styling
- **Audio**: Native HTML5 Audio API integration

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (@neondatabase/serverless)
- **Session Management**: In-memory storage with optional database persistence
- **Development**: Hot module replacement via Vite middleware

### Build System
- **Development**: TSX for TypeScript execution
- **Production**: ESBuild for server bundling, Vite for client bundling
- **Asset Handling**: Support for GLTF/GLB models, audio files, and GLSL shaders

## Key Components

### Game State Management
- **useBurgerGame**: Main game state store managing burgers, heroes, achievements, and prestige
- **useAudio**: Audio state management for background music and sound effects
- **useGame**: Core game phase management (ready/playing/ended)

### Game Mechanics
- **Click System**: Manual burger production with upgrade capabilities
- **Hero System**: Automated production units with scaling costs and abilities
- **Achievement System**: Goal-based progression with rewards
- **Prestige System**: Meta-progression allowing game resets for permanent bonuses
- **Particle System**: Visual effects for enhanced user experience

### UI Components
- **BurgerGame**: Main game container component
- **HeroCard**: Individual hero purchase and management interface
- **AchievementToast**: Achievement notification system
- **PrestigeModal**: Prestige system interface
- **ParticleSystem**: Background animation system

## Data Flow

1. **Game Initialization**: Load saved game state from localStorage
2. **User Input**: Click events trigger burger production and audio feedback
3. **State Updates**: Zustand stores manage all game state changes
4. **Auto-save**: Periodic saves to localStorage every 30 seconds
5. **Achievement Checking**: Continuous monitoring for achievement completion
6. **Prestige Flow**: Reset mechanics with bonus calculation and persistence

## External Dependencies

### Core Dependencies
- **React Ecosystem**: React, React-DOM for UI framework
- **Three.js Ecosystem**: React Three Fiber, Drei for 3D graphics
- **State Management**: Zustand for predictable state updates
- **UI Framework**: Radix UI for accessible component primitives
- **Styling**: Tailwind CSS for utility-first styling
- **Database**: Drizzle ORM with PostgreSQL dialect

### Development Dependencies
- **TypeScript**: Full type safety across client and server
- **Vite**: Fast development server and optimized builds
- **ESBuild**: High-performance bundling for production
- **PostCSS**: CSS processing with Tailwind integration

## Deployment Strategy

### Development Environment
- **Local Development**: Vite dev server on port 5000
- **Hot Reload**: Full HMR support for React components
- **Error Handling**: Runtime error overlay for debugging

### Production Deployment
- **Platform**: Replit with autoscale deployment target
- **Build Process**: 
  1. Vite builds client assets to `dist/public`
  2. ESBuild bundles server code to `dist/index.js`
- **Static Assets**: Served via Express static middleware
- **Database**: Neon PostgreSQL with connection pooling

### Environment Configuration
- **DATABASE_URL**: PostgreSQL connection string (required)
- **NODE_ENV**: Environment detection for conditional behavior
- **Port Configuration**: Express server on port 5000 (configurable)

## Changelog

- June 27, 2025. Initial setup
- June 27, 2025. Redesigned UI to match user's clean, simple layout preference with white background
- June 27, 2025. Created custom SVG avatars for all heroes (Spider-Man, Thor, Transformer, Captain America, Iron Man inspired designs)
- June 27, 2025. Added hidden achievements system, popup notifications, and endgame scenario from user's HTML reference
- June 27, 2025. Updated achievement name from "Burger Billionaire" to "McBillionaire" per user request

## User Preferences

Preferred communication style: Simple, everyday language.
UI Design: Clean, simple layout with white background, centered burger button, heroes on left, achievements on right.