# YourHost - Luxury Vacation Rentals & Serviced Apartments

## Overview

YourHost is a modern vacation rental and serviced apartments booking website built as a single-page application. The platform focuses on providing a luxury accommodation booking experience with features like property search, date selection, booking management, and property filtering. The website emphasizes a clean, professional design with smooth user interactions and responsive layouts suitable for both desktop and mobile users.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Single-page application (SPA)** built with vanilla HTML, CSS, and JavaScript
- **Bootstrap 5.3.2** framework for responsive grid system and UI components
- **Component-based CSS** using CSS custom properties (CSS variables) for consistent theming
- **Mobile-first responsive design** ensuring optimal experience across all device sizes
- **Modular JavaScript architecture** with separate initialization functions for different features

### UI/UX Design Patterns
- **Fixed navigation bar** with backdrop blur effect for modern aesthetic
- **CSS custom properties** for centralized theme management with primary colors, shadows, and spacing
- **Smooth scrolling** and animations for enhanced user experience
- **Progressive enhancement** approach ensuring core functionality works without JavaScript

### Booking System Architecture
- **Multi-step booking flow** with form validation and user feedback
- **Date range selection** with constraint validation (checkout after checkin, no past dates)
- **Real-time booking summary** updates based on user selections
- **Property filtering system** for search and discovery functionality

### Data Management
- **Client-side state management** for booking flows and user interactions
- **Form validation system** with real-time feedback and error handling
- **Local date manipulation** for booking constraints and availability checking

## External Dependencies

### CSS Frameworks & Libraries
- **Bootstrap 5.3.2** - UI framework for responsive layouts and components
- **Font Awesome 6.4.0** - Icon library for consistent iconography throughout the site

### JavaScript Libraries
- **Flatpickr** - Advanced date picker component for check-in/check-out date selection with custom styling and validation rules

### Font Resources
- **Inter font family** - Primary typography with fallbacks to system fonts for optimal performance and readability

### CDN Services
- **Bootstrap CDN** for framework delivery
- **Cloudflare** for Font Awesome icon library
- **JSDelivr CDN** for Flatpickr date picker component

Note: The current implementation is a static frontend application. Integration with backend services for property data, booking management, and user authentication would require additional API development and database systems.