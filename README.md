# Real-time Chat Application

A beautiful real-time chat application built with Spring Boot and WebSockets.

## Features

- Real-time messaging with WebSockets
- User presence (join/leave notifications)
- Timestamps for messages
- Responsive design for all devices
- Message notification sounds
- User avatars with consistent colors

## Technology Stack

- Java 17
- Spring Boot 3.2.3
- Spring WebSockets with STOMP
- Thymeleaf templates
- SockJS and STOMP.js for client-side WebSocket support
- Custom CSS for a beautiful UI

## Running the Application

### Using Docker

1. Build the Docker image:
   ```
   docker build -t chat-app .
   ```

2. Run the container:
   ```
   docker run -d -p 9999:9999 --name chatapp-container chat-app
   ```

3. Access the application at http://<VM-PublicIP>:9999

### Pushing Image to DockerHub
Login to DockerHub using "docker login" command

4. Tagging the Image:
   ```
   docker tag chat-app kastrov/chat-app:latest
   ```

5. Pushing the Image to DockerHub:
   ```
   docker push kastrov/chat-app:latest
   ```

## Project Structure

- `src/main/java/com/example/chatapp/` - Java source files
  - `ChatApplication.java` - Main application class
  - `config/WebSocketConfig.java` - WebSocket configuration
  - `controller/ChatController.java` - Controller for handling chat messages
  - `model/ChatMessage.java` - Model for chat messages
  - `model/MessageType.java` - Enum for message types
  - `event/WebSocketEventListener.java` - Handles WebSocket events
- `src/main/resources/` - Resources
  - `static/css/main.css` - Custom CSS
  - `static/js/main.js` - JavaScript for WebSocket interaction
  - `static/sounds/` - Sound files for notifications
  - `templates/index.html` - Main page
