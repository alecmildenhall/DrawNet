# Real-Time Collaborative Drawing Platform Architecture

## Overview

This project is a real-time collaborative drawing platform where multiple users can draw together on a shared canvas. The platform is built using **Go** for the backend, **WebSockets** for real-time communication, and a **microservices architecture** to ensure scalability, modularity, and maintainability.

## File Structure

```bash
Drawnet/
│
├── backend/                     # Backend services
│   ├── websocket-server/         # Handles real-time communication via WebSockets
│   │   ├── main.go               # Entry point for the WebSocket server
│   │   ├── handlers/             # WebSocket handlers
│   │   ├── models/               # Data models for drawing events
│   │   └── utils/                # Utility functions
│   │
│   ├── api-gateway/              # API Gateway for handling RESTful requests
│   │   ├── main.go               # Entry point for the API Gateway
│   │   ├── controllers/          # API route handlers
│   │   ├── services/             # Business logic
│   │   └── models/               # Data models for API requests/responses
│   │
│   ├── session-service/          # Microservice for managing drawing sessions
│   │   ├── main.go               # Entry point for the session service
│   │   └── services/             # Session-related business logic
│   │
│   ├── user-service/             # Microservice for user authentication and management
│   │   ├── main.go               # Entry point for the user service
│   │   └── services/             # User-related business logic
│   │
│   └── drawing-service/          # Microservice for storing and retrieving drawings
│       ├── main.go               # Entry point for the drawing service
│       └── services/             # Drawing-related business logic
│
├── frontend/                     # Frontend files (HTML, CSS, JavaScript)
│   ├── index.html                # Main HTML file for the drawing interface
│   ├── css/                      # CSS files for styling
│   │   └── main.css              # Main stylesheet
│   └── js/                       # JavaScript files
│       ├── app.js                # Main logic for connecting to WebSocket and drawing
│       └── api.js                # Logic for handling API requests
│
├── config/                       # Configuration files for environment settings
│   └── default.json              # Default configuration file (e.g., ports, API URLs)
│
├── scripts/                      # Scripts for deployment and setup
│   └── deploy.sh                 # Deployment script
│
├── test/                         # Test files for backend and frontend
│   ├── backend/                  # Unit tests for backend services
│   └── frontend/                 # Tests for frontend functionality
│
├── .gitignore                    # List of files and directories to ignore in Git
├── README.md                     # Project overview and setup instructions
├── ARCHITECTURE.md               # Architecture overview
└── Dockerfile                    # Dockerfile for containerizing the application