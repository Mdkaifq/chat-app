# FastAPI React Chat App

A real-time chat application built with FastAPI backend and React frontend, featuring WebSocket connections for instant messaging.

## Features

- Real-time messaging with WebSocket support
- User authentication and authorization
- Message history persistence
- Responsive React UI
- RESTful API endpoints
- Real-time user presence indicators

## Tech Stack

### Backend
- **FastAPI** - Modern Python web framework
- **WebSockets** - Real-time bidirectional communication
- **Motor** - Database ORM
- **MongoDB** - Database
- **JWT** - Authentication tokens
- **Pydantic** - Data validation
- **Uvicorn** - ASGI server

### Frontend
- **React** - UI library
- **Socket.io-client** - WebSocket client
- **Axios** - HTTP client
- **React Router** - Navigation
- **Tailwind CSS** - Styling
- **Redux** - State management

## Prerequisites

- Python 3.8+
- Node.js 16+

## Installation

### Backend Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/fastapi-react-chat.git
cd fastapi-react-chat
```

2. Create and activate a virtual environment:
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install Python dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your configuration
```

5. Start the FastAPI server:
```bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd ../frontend
```

2. Install Node.js dependencies:
```bash
npm install
```

3. Create environment file:
```bash
cp .env.example .env.local
# Edit .env.local with your API URL
```

4. Start the React development server:
```bash
npm start
```

## Environment Variables

### Backend (.env)
```env
port=
APP_NAME=
API_V_STR=/api/v1
DEBUG_MODE=
ALLOWED_ORIGINS=
API_ORIGIN=
FRONTEND_LOGIN_URL=
DB_HOST=localhost
DB_PORT=
DB_NAME=
USERS_COLLECTION=
PRIVATE_CHAT_COLLECTION=
GROUP_CHAT_COLLECTION=
JWT_SECRET_KEY=
ACTIVATION_SECRET_KEY=
ALGORITHM=
ACCESS_TOKEN_EXPIRE_MINUTES=
```

### Frontend (.env.local)
```env
REACT_APP_API_URL=
REACT_APP_WS_URL=
```

```

### Code Formatting

Backend (Python):
```bash
black .
isort .
flake8 .
```

Frontend (JavaScript):
```bash
npm run lint
npm run format
```

## Project Structure

```
backend
│   ├── app
│   │   ├── api
│   │   ├── core
│   │   ├── crud
│   │   ├── database
│   │   ├── exceptions
│   │   ├── main.py
│   │   ├── models
│   │   ├── schemas
│   │   ├── serializers
│   │   ├── services
│   │   └── websocket
│   ├── index.py
│   └── requirements.txt
├── frontend
│   ├── index.html
│   ├── package.json
│   ├── public
│   ├── src
│   │   ├── assets
│   │   ├── components
│   │   │   ├── AccountActivatedPage
│   │   │   ├── ActiveLink
│   │   │   ├── Auth
│   │   │   ├── Chat
│   │   │   ├── Chats
│   │   │   ├── ChatSearch
│   │   │   ├── Groups
│   │   │   ├── LandingPge
│   │   │   ├── Layout
│   │   │   ├── Login
│   │   │   ├── LoginInputFields
│   │   │   ├── Logout
│   │   │   ├── Message
│   │   │   ├── MessageBoxTop
│   │   │   ├── Messages
│   │   │   ├── MyProfile
│   │   │   ├── NoMessage
│   │   │   ├── PasswordChange
│   │   │   ├── PasswordChangeInputFields
│   │   │   ├── Profile
│   │   │   ├── SendMessage
│   │   │   ├── Settings
│   │   │   ├── Sidebar
│   │   │   ├── Signup
│   │   │   ├── SignupComplete
│   │   │   ├── SignupInputFields
│   │   │   ├── SignupLogin
│   │   │   ├── User
│   │   │   ├── Users
│   │   │   └── UserSearch
│   │   ├── index.css
│   │   ├── main.jsx
│   │   └── utilities
│   ├── tailwind.config.js
│   └── vite.config.js
└── readme.md

```

## Deployment

### Using Docker

1. Build and run with Docker Compose:
```bash
docker-compose up --build
```

### Manual Deployment

#### Backend (Heroku/Railway)
```bash
# Install gunicorn
pip install gunicorn

# Start with gunicorn
gunicorn main:app -w 4 -k uvicorn.workers.UvicornWorker
```

#### Frontend (Vercel/Netlify)
```bash
# Build for production
npm run build

# Deploy build folder to your hosting service
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support, email mdkaifq22@gmail.com or create an issue in the GitHub repository.

---

Made with ❤️ by [Md Kaif](https://github.com/mdkaifq)