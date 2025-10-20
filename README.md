
# Real-Time Chat Application

A modern, real-time chat application built with Flask and Socket.IO. Create or join chat rooms and communicate instantly with others.

![Chat App](https://img.shields.io/badge/Flask-v2.0+-blue.svg)
![Socket.IO](https://img.shields.io/badge/Socket.IO-v4.0+-green.svg)
![Python](https://img.shields.io/badge/Python-3.7+-yellow.svg)

## Features

- 🚀 Real-time messaging using WebSockets
- 💬 Create and join chat rooms with unique codes
- 👥 Multiple users can chat simultaneously
- 🎨 Modern, responsive UI with dark theme
- 📱 Mobile-friendly design
- ⏰ Timestamp for each message
- 🔐 Session-based user management

## Screenshots

### Home Page
Enter your name and either create a new room or join an existing one with a room code.

### Chat Room
Real-time messaging interface with message history and timestamps.

## Prerequisites

- Python 3.7 or higher
- pip (Python package installer)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Denotess/chat-app.git
cd chat-app
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv

# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate
```

3. Install required dependencies:
```bash
pip install flask flask-socketio
```

## Usage

1. Start the application:
```bash
python main.py
```

2. Open your web browser and navigate to:
```
http://localhost:5000
```

3. Enter your name and either:
   - **Create a Room**: Click "Create a Room" to generate a unique 4-character room code
   - **Join a Room**: Enter an existing room code and click "Join a Room"

4. Share the room code with others to chat together!

## Project Structure

```
chat-app/
│
├── main.py                 # Flask application and Socket.IO logic
├── templates/
│   ├── base.html          # Base template
│   ├── home.html          # Landing page with login form
│   └── room.html          # Chat room interface
├── static/
│   └── style.css          # Styling for the application
└── README.md              # This file
```

## How It Works

1. **Room Creation**: When a user creates a room, a unique 4-character code is generated
2. **Joining**: Users can join existing rooms by entering the room code
3. **Real-time Communication**: Socket.IO enables bidirectional, event-based communication between the server and clients
4. **Message Persistence**: Messages are stored per room during the session
5. **Room Management**: Rooms are automatically deleted when the last user leaves

## Technologies Used

- **Backend**: Flask (Python web framework)
- **Real-time Communication**: Flask-SocketIO
- **Frontend**: HTML, CSS, JavaScript
- **WebSockets**: Socket.IO client library

## Configuration

The application uses a secret key for session management. In production, change this to a secure random key:

```python
app.config["SECRET_KEY"] = "your-secret-key-here"
```

## Development

To run in development mode with debug enabled:

```bash
python main.py
```

The application will automatically reload when you make changes to the code.

## Deployment Considerations

For production deployment:

1. Set `debug=False` in the `socketio.run()` call
2. Use a production-grade WSGI server like Gunicorn with eventlet or gevent
3. Set a strong, random `SECRET_KEY`
4. Configure proper CORS settings if needed
5. Consider using Redis for scalable message queuing

## Known Limitations

- Messages are stored in memory and will be lost on server restart
- No user authentication or persistent accounts
- No message history beyond the current session
- No file sharing or media support

## Future Enhancements

- [ ] Persistent message storage (database)
- [ ] User authentication
- [ ] Private messaging
- [ ] File/image sharing
- [ ] Typing indicators
- [ ] User presence status
- [ ] Message reactions
- [ ] Dark/light theme toggle

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Flask documentation
- Socket.IO documentation
- Modern CSS design inspiration from contemporary web design trends
