# McHez - Authentic Nigerian Cuisine Website

## Overview

McHez is a restaurant website for an authentic Nigerian cuisine establishment. The application is built as a simple Flask web application serving a single-page website with modern styling and interactive features. The site showcases the restaurant's menu, gallery, and contact information with a focus on user experience and visual appeal.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Single Page Application (SPA)**: The website uses a single HTML page with JavaScript-driven navigation and interactions
- **Bootstrap Framework**: Utilizes Bootstrap 5.3.0 for responsive grid system and UI components
- **Custom Styling**: Enhanced with custom CSS using CSS custom properties for consistent theming
- **Progressive Enhancement**: Core content accessible without JavaScript, enhanced with interactive features

### Backend Architecture
- **Flask Framework**: Lightweight Python web framework serving as the application server
- **Template Engine**: Uses Jinja2 (Flask's default) for server-side HTML rendering
- **Static File Serving**: Flask serves CSS, JavaScript, and other static assets
- **Environment Configuration**: Uses environment variables for configuration (session secret)

## Key Components

### Web Server
- **Flask Application**: Main application server (`app.py`)
- **Entry Point**: `main.py` imports the Flask app for deployment
- **Development Server**: Configured to run on host `0.0.0.0`, port `5000`

### Frontend Components
- **Navigation System**: Fixed navbar with smooth scrolling and active section highlighting
- **Menu Filter System**: JavaScript-powered menu category filtering
- **Image Gallery**: Interactive photo gallery with loading optimization
- **Contact Forms**: Client-side form handling and validation
- **Scroll Animations**: Progressive content reveal on scroll
- **Responsive Design**: Mobile-first approach with Bootstrap grid system

### Styling System
- **CSS Custom Properties**: Centralized color scheme and typography variables
- **Color Palette**: Nigerian-inspired colors (orange, green, gold) reflecting cultural authenticity
- **Typography**: Playfair Display for headings, Inter for body text
- **Component Library**: Reusable UI components with consistent styling

## Data Flow

1. **Request Handling**: Flask receives HTTP requests and routes them to appropriate handlers
2. **Template Rendering**: Server renders HTML templates with any dynamic content
3. **Static Asset Delivery**: CSS, JavaScript, and images served directly by Flask
4. **Client-Side Interactions**: JavaScript handles navigation, filtering, and animations without server communication
5. **Form Submission**: Contact forms processed client-side (backend integration ready)

## External Dependencies

### CDN Resources
- **Bootstrap 5.3.0**: UI framework for responsive design and components
- **Font Awesome 6.4.0**: Icon library for visual elements
- **Google Fonts**: Playfair Display and Inter font families

### Python Dependencies
- **Flask**: Web framework for request handling and template rendering
- **Standard Library**: Uses `os` for environment variables and `logging` for debugging

## Deployment Strategy

### Development Environment
- **Debug Mode**: Enabled for development with automatic reloading
- **Host Configuration**: Bound to `0.0.0.0` for container/cloud deployment compatibility
- **Environment Variables**: Session secret configured via environment variable with fallback

### Production Readiness
- **WSGI Compatible**: Flask app structure supports WSGI deployment
- **Static File Strategy**: Currently served by Flask (production would benefit from CDN/reverse proxy)
- **Configuration Management**: Environment-based configuration pattern established
- **Security**: Session secret externalized, debug mode configurable

### Scalability Considerations
- **Stateless Design**: No database or session storage, easily horizontally scalable
- **CDN Integration**: Static assets can be moved to CDN for better performance
- **Caching Strategy**: Template caching and static file optimization opportunities
- **Database Ready**: Architecture supports adding database integration if needed

## Technical Decisions

### Framework Choice: Flask
- **Problem**: Need lightweight, flexible web framework
- **Solution**: Flask chosen for simplicity and minimal overhead
- **Rationale**: Perfect for static content serving with room for future API expansion

### Frontend Approach: Enhanced Static Site
- **Problem**: Balance between performance and interactivity
- **Solution**: Server-rendered HTML enhanced with progressive JavaScript features
- **Benefits**: Fast initial load, SEO-friendly, accessible without JavaScript

### Styling Strategy: Bootstrap + Custom CSS
- **Problem**: Need professional design with development efficiency
- **Solution**: Bootstrap base with custom CSS variables and overrides
- **Benefits**: Responsive design, consistent components, brand customization