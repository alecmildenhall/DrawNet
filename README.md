# DrawNet
WIP: Real-time collaborative drawing platform built with Go and WebSockets, enabling multiple users to draw together on a shared canvas. Features microservices architecture and cloud deployment for scalability and performance.

# Plan for Arichitecture
/Drawnet
|-- /backend
|   |-- /websocket-server
|   |   |-- main.go             # Entry point for WebSocket server
|   |   |-- /handlers           # WebSocket handlers
|   |   |-- /models             # Data models for drawing events
|   |   `-- /utils              # Utility functions
|
|   |-- /api-gateway            # Handles RESTful API requests
|   |   |-- main.go             # Entry point for API Gateway
|   |   |-- /controllers        # API controllers for routing
|   |   |-- /services           # Business logic for session, user management
|   |   `-- /models             # Data models for API requests/responses
|
|   |-- /session-service        # Microservice for session management
|   |   |-- main.go             # Entry point for session service
|   |   `-- /services           # Session related business logic
|
|   |-- /user-service           # Microservice for user management
|   |   |-- main.go             # Entry point for user service
|   |   `-- /services           # User related business logic
|
|   `-- /drawing-service        # Microservice for drawing storage
|       |-- main.go             # Entry point for drawing service
|       `-- /services           # Drawing related business logic
|
|-- /frontend
|   |-- index.html              # Main HTML document
|   |-- /css                    # CSS files
|   |   `-- main.css            # Main stylesheet
|   |-- /js                     # JavaScript files
|   |   |-- app.js              # Main JS logic for interacting with the WebSocket
|   |   `-- api.js              # JS for handling API requests
|
|-- /config                     # Configuration files and environment variables
|   `-- default.json            # Default configuration settings
|
|-- /scripts                    # Utility scripts, e.g., for deployment
|   `-- deploy.sh               # Deployment script
|
|-- /test                       # Test files for backend and frontend
|   |-- /backend                # Backend tests
|   `-- /frontend               # Frontend tests
|
|-- .gitignore                  # Specifies intentionally untracked files to ignore
|-- README.md                   # Project overview and setup instructions
`-- Dockerfile                  # Docker configuration for containerization