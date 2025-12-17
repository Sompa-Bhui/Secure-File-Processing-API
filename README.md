# Secure File Upload API

FastAPI-based secure file upload system with JWT authentication.

## 🚀 Features
- 🔐 JWT Authentication
- 📁 Secure File Upload (Max 10MB)
- 👤 User Management
- 🗑️ File Management (List, Delete)
- 🔒 Password Hashing with Bcrypt
- 📚 Interactive API Documentation

## 🏃 Quick Start

### Local Development
```bash
# Install dependencies
pip install -r requirements.txt

# Run the API
python main.py

# API will be available at: http://localhost:8000
# Docs available at: http://localhost:8000/docs
```

### Docker
```bash
# Build and run
docker-compose up -d

# Access API at: http://localhost:8000
```

### Deploy to Render.com
1. Push files to GitHub
2. Go to Render.com and create account
3. New Web Service → Connect GitHub repo
4. Deploy automatically!

## 📡 API Endpoints

### Authentication
- `POST /register` - Register new user
- `POST /login` - Login and get token

### File Operations (Requires Authentication)
- `POST /upload` - Upload a file
- `GET /files` - List your files
- `DELETE /files/{file_id}` - Delete a file

### General
- `GET /` - API info
- `GET /health` - Health check
- `GET /docs` - Interactive API documentation

## 🧪 Testing

### 1. Register User
```bash
curl -X POST "http://localhost:8000/register" \
  -H "Content-Type: application/json" \
  -d '{"username":"testuser","password":"test123","email":"test@example.com"}'
```

### 2. Login
```bash
curl -X POST "http://localhost:8000/login" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -d "username=testuser&password=test123"
```

### 3. Upload File
```bash
curl -X POST "http://localhost:8000/upload" \
  -H "Authorization: Bearer YOUR_TOKEN_HERE" \
  -F "file=@/path/to/your/file.pdf"
```

## 🔒 Security
- Passwords hashed with bcrypt
- JWT tokens for authentication
- File size validation (10MB max)
- User-specific file access
- CORS protection

## 📦 Tech Stack
- Python 3.11
- FastAPI
- Uvicorn
- JWT (python-jose)
- Bcrypt
- Docker

## 🌐 Deployment Options
- Render.com (Free)
- Railway.app (Free)
- Heroku
- Docker
- VPS

## 📝 Environment Variables
Create a `.env` file:


## Live Projects 
https://secure-file-api-2.onrender.com/docs
