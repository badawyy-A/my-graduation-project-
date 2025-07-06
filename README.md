# 🏛️ KEMIT: AI-Powered Smart Travel Companion for Egypt

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Flutter](https://img.shields.io/badge/Flutter-3.5+-blue.svg)](https://flutter.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-20.x-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-19.1.0-blue.svg)](https://reactjs.org/)
[![Docker](https://img.shields.io/badge/Docker-3.9+-blue.svg)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **KEMIT** is a comprehensive AI-powered travel companion designed to revolutionize the tourist experience in Egypt. The system integrates multiple advanced AI technologies including a custom-trained CNN model for ancient Egyptian artifact and monument recognition, a sophisticated RAG (Retrieval-Augmented Generation) chatbot with multilingual support, real-time text-to-speech synthesis, and advanced lip-sync technology for immersive storytelling.

## 📋 Table of Contents

- [🎯 Project Overview](#-project-overview)
- [🏗️ System Architecture](#️-system-architecture)
- [🚀 Features](#-features)
- [🛠️ Technology Stack](#️-technology-stack)
- [📁 Project Structure](#-project-structure)
- [⚙️ Installation & Setup](#️-installation--setup)
- [🔧 Configuration](#-configuration)
- [📱 API Documentation](#-api-documentation)
- [🧪 Testing](#-testing)
- [🚀 Deployment](#-deployment)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

## 🎯 Project Overview

KEMIT addresses critical tourism challenges by providing personalized cultural insights, interactive historical narratives, and seamless multilingual communication, making Egyptian heritage accessible and engaging for international visitors.

### 🌟 Key Innovations

- **First-Person Historical Narratives**: Each classified artifact/monument provides immersive first-person storytelling
- **Advanced Lip-Sync Technology**: Realistic video generation for human figures with synchronized speech
- **Comprehensive Topic Classification**: 40+ specialized categories for precise tourist guidance
- **Multilingual Cultural Context**: Deep cultural insights available in 7+ languages
- **Real-time Image Processing**: Instant artifact recognition with contextual information

## 🏗️ System Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Flutter App   │    │  React Web App  │    │   Mobile Web    │
│   (Frontend)    │    │   (Landing)     │    │   (PWA)         │
└─────────┬───────┘    └─────────┬───────┘    └─────────┬───────┘
          │                      │                      │
          └──────────────────────┼──────────────────────┘
                                 │
                    ┌─────────────┴─────────────┐
                    │     Node.js Backend       │
                    │   (Authentication,        │
                    │    User Management,       │
                    │    Chat History)          │
                    └─────────────┬─────────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    │    FastAPI AI Services    │
                    │   (CNN, RAG, TTS,         │
                    │    Lip-Sync)              │
                    └─────────────┬─────────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    │   Infrastructure Layer    │
                    │  (MinIO, MongoDB,         │
                    │   Ollama, Chroma)         │
                    └───────────────────────────┘
```

## 🚀 Features

### 🤖 AI-Powered Services

#### 1. **Ancient Egyptian CNN Classification**
- **Model**: Custom-trained Keras CNN from scratch (96% accuracy)
- **Classes**: 21 distinct categories including:
  - **Pharaohs**: King Akhenaten, King Amenhotep III, King Thutmose III, King Tutankhamun, King Ramesses II, King Zoser
  - **Queens**: Queen Hatshepsut, Queen Nefertiti, Ankhesenamun
  - **Deities**: Goddess Isis
  - **Monuments**: Pyramids (Khafre, Menkaure, Bent, Djoser), Sphinx, Colossi of Memnon
  - **Temples**: Temple of Hatshepsut, Temple of Isis in Philae, Temple of Kom Ombo, Ramessum
- **Features**: Real-time image processing, confidence scoring, multilingual descriptions

#### 2. **RAG (Retrieval-Augmented Generation) Chatbot**
- **LLM**: Ollama with Llama3.1:8b model
- **Embeddings**: Google Generative AI (models/embedding-001)
- **Vector Database**: Chroma with MMR (Maximal Marginal Relevance) retrieval
- **Topics**: 40+ specialized categories including:
  - Nile Cruises, Alexandria, Hotel Advice, Safety & Emergency
  - Red Sea Resorts, Theme Tours, Siwa Oasis, Valley of Kings & Queens
  - Local Legends, Cultural Experiences, Arabic Phrases, Abu Simbel
  - Transport Guide, Sinai Attractions, Grand Egyptian Museum
  - And many more...
- **Multilingual Support**: Arabic, English, Spanish, French, German, Chinese, Japanese

#### 3. **Advanced Text-to-Speech (TTS)**
- **Model**: XTTS v1.1 multilingual speech synthesis
- **Features**: 
  - Natural-sounding voice generation
  - Multiple speaker voices (male/female)
  - Language-specific pronunciation
  - Real-time audio generation

#### 4. **Lip-Sync Technology**
- **Model**: Wav2Lip for realistic lip synchronization
- **Features**:
  - Synchronized speech with visual content
  - Support for human figures and artifacts
  - High-quality video output generation

### 📱 Mobile Application (Flutter)

#### Core Features
- **Cross-Platform**: Android, iOS, Web, Desktop support
- **State Management**: Flutter Bloc + Riverpod
- **UI Components**: Material Design 3 with custom theming
- **Navigation**: Curved navigation bar with smooth transitions

#### Chat Interface
- **Library**: Dash Chat 2 for rich chat experience
- **Features**:
  - Real-time messaging with AI assistant
  - Message persistence with local storage
  - User-specific chat history
  - Clear chat functionality
  - Typing indicators and message status

#### Image Classification
- **Image Picker**: Camera and gallery support
- **Language Selection**: 7 language options
- **Real-time Processing**: Instant artifact recognition
- **Video Playback**: Integrated video player for results

#### Additional Features
- **Authentication**: Secure login/signup with JWT
- **User Profile**: Personal information management
- **Settings**: App preferences and configuration
- **Location Services**: GPS-based nearby places
- **Offline Support**: Local data caching

### 🌐 Web Landing Page (React)

#### Technologies
- **Framework**: React 19.1.0 with TypeScript
- **Styling**: CSS with dark/light theme support
- **State Management**: Zustand for global state
- **Routing**: React Router DOM v7
- **Animations**: Framer Motion

#### Features
- **Responsive Design**: Mobile-first approach
- **Theme Toggle**: Dark/light mode switching
- **Interactive Demo**: Live chatbot and image classification
- **Modern UI**: Clean, professional design
- **SEO Optimized**: Meta tags and structured data

### 🔧 Backend API (Node.js)

#### Authentication & User Management
- **Framework**: Express.js with middleware
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT with bcrypt password hashing
- **Email**: Nodemailer for verification emails
- **File Upload**: Multer with Sharp image processing

#### Models
- **User Model**: Profile management, role-based access
- **Chat Models**: Text and image chat history
- **Place Model**: Tourism locations with categories
- **Report Model**: User feedback and issues

#### Services
- **Auth Service**: Login, registration, password reset
- **Chat Services**: Message handling and history
- **Place Service**: Location-based recommendations
- **Upload Service**: Image processing and storage

### 🤖 AI Component (FastAPI)

#### Core Services
- **Image Service**: CNN classification and video generation
- **RAG Engine**: Intelligent chatbot with context retrieval
- **TTS Service**: Speech synthesis with voice cloning
- **WaveLIB Service**: Lip-sync video generation

#### Infrastructure
- **Storage**: MinIO object storage for media files
- **Vector DB**: Chroma for document embeddings
- **LLM**: Ollama for local model inference
- **Logging**: Comprehensive request tracking

## 🛠️ Technology Stack

### Frontend Technologies

#### Flutter Mobile App
```yaml
dependencies:
  flutter: ^3.5.1
  flutter_bloc: ^9.1.1
  flutter_riverpod: ^2.4.9
  dash_chat_2: ^0.0.21
  flutter_gemini: ^3.0.0
  google_maps_flutter: ^2.12.3
  image_picker: ^1.1.2
  video_player: ^2.10.0
  dio: ^5.7.0
  shared_preferences: ^2.3.2
  geolocator: ^13.0.2
  flutter_secure_storage: ^9.2.4
```

#### React Web App
```json
{
  "dependencies": {
    "react": "^19.1.0",
    "react-dom": "^19.1.0",
    "react-router-dom": "^7.6.1",
    "typescript": "^4.9.5",
    "framer-motion": "^12.15.0",
    "zustand": "^5.0.5"
  }
}
```

### Backend Technologies

#### Node.js Backend
```json
{
  "dependencies": {
    "express": "^4.18.3",
    "mongoose": "^8.2.1",
    "bcryptjs": "^2.4.3",
    "jsonwebtoken": "^9.0.2",
    "multer": "^1.4.5-lts.1",
    "sharp": "^0.33.2",
    "cloudinary": "^2.4.0",
    "nodemailer": "^6.9.14",
    "cors": "^2.8.5",
    "compression": "^1.7.4"
  }
}
```

#### Python AI Services
```txt
fastapi==0.104.1
uvicorn==0.24.0
torch==2.1.0
keras==2.15.0
langchain==0.1.0
langchain_ollama==0.1.0
langchain_google_genai==0.1.0
TTS==0.22.0
opencv_python==4.8.1.78
Pillow==10.1.0
minio==7.2.0
deep_translator==1.11.4
langid==1.1.6
```

### Infrastructure & DevOps

#### Containerization
```yaml
# Docker Compose
version: "3.9"
services:
  kemit-api:
    build: .
    ports: ["4000:4000"]
    depends_on: [ollama, minio]
  
  ollama:
    image: ollama/ollama
    ports: ["11434:11434"]
  
  minio:
    image: minio/minio
    ports: ["9000:9000", "9001:9001"]
```

#### AI Models & Services
- **CNN Model**: Custom Keras model (96% accuracy)
- **LLM**: Ollama with Llama3.1:8b
- **TTS**: XTTS v1.1 multilingual
- **Lip-Sync**: Wav2Lip implementation
- **Embeddings**: Google Generative AI

## 📁 Project Structure

```
FULL_KEMIT/
├── kemit_ai_component/           # AI Services (FastAPI)
│   ├── main.py                   # FastAPI application entry
│   ├── routers/                  # API route definitions
│   │   ├── chat_route.py         # RAG chatbot endpoints
│   │   └── image_route.py        # CNN classification endpoints
│   ├── services/                 # AI service implementations
│   │   ├── cnn_classifier/       # Custom CNN model
│   │   ├── rag_chatbot/          # RAG engine implementation
│   │   ├── TTS_service/          # Text-to-speech service
│   │   └── waveLIB_service/      # Lip-sync technology
│   ├── utils/                    # Utilities and configuration
│   ├── reference_data/           # Kings descriptions and prompts
│   ├── reference_audio/          # Voice samples
│   ├── models/                   # Trained AI models
│   ├── vectors_data_bases/       # Vector database storage
│   ├── Dockerfile                # Container configuration
│   └── docker-compose.yml        # Multi-service orchestration
│
├── kemit_backend/                # Node.js Backend API
│   ├── index.js                  # Express application entry
│   ├── routes/                   # API route handlers
│   │   ├── authRoute.js          # Authentication endpoints
│   │   ├── chatbotTextRoute.js   # Text chat management
│   │   ├── chatbotImageRoute.js  # Image chat management
│   │   ├── placesRoute.js        # Location services
│   │   └── userRoute.js          # User management
│   ├── models/                   # MongoDB schemas
│   ├── services/                 # Business logic
│   ├── middleware/               # Express middleware
│   ├── utils/                    # Utilities and helpers
│   └── config/                   # Database configuration
│
├── kemit_flutter_app/            # Flutter Mobile Application
│   ├── lib/
│   │   ├── main.dart             # App entry point
│   │   ├── core/                 # Core utilities
│   │   │   ├── caching/          # Local storage
│   │   │   ├── networking/       # API clients
│   │   │   └── widgets/          # Reusable components
│   │   └── features/             # Feature modules
│   │       ├── home/             # Main app features
│   │       │   ├── chat_gemini/  # AI chat interface
│   │       │   ├── image_classification/ # CNN integration
│   │       │   └── tourism_details/ # Location features
│   │       ├── auth/             # Authentication
│   │       ├── profile/          # User profile
│   │       └── settings/         # App settings
│   ├── assets/                   # Images and resources
│   └── pubspec.yaml              # Dependencies
│
├── kemit_landing_page/           # React Web Application
│   ├── src/
│   │   ├── components/           # Reusable UI components
│   │   ├── pages/                # Page components
│   │   ├── tabs/                 # Demo interface tabs
│   │   ├── context/              # Theme management
│   │   └── App.tsx               # Main application
│   ├── public/                   # Static assets
│   └── package.json              # Dependencies
│
├── RAG_system_preparation/       # RAG system development
│   ├── main_prepare.py           # RAG preparation script
│   ├── Loaders.py                # Document loading utilities
│   ├── Splitter.py               # Text splitting logic
│   ├── VectorDB.py               # Vector database setup
│   ├── data/                     # Training data
│   └── vectors_data_bases/       # Vector embeddings
│
└── ancient-egypt-cnn/            # CNN model development
    ├── notebooks/                # Jupyter notebooks
    ├── data/                     # Training datasets
    ├── sample_images/            # Test images
    ├── Deployment/               # Model deployment
    └── README.md                 # Detailed CNN documentation
```

## ⚙️ Installation & Setup

### Prerequisites

- **Python 3.10+**
- **Node.js 20.x**
- **Flutter 3.5+**
- **Docker & Docker Compose**
- **CUDA 12.2** (for GPU acceleration)
- **Git**

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/FULL_KEMIT.git
cd FULL_KEMIT
```

### 2. AI Component Setup

```bash
cd kemit_ai_component

# Install Python dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys and configuration

# Run with Docker Compose
docker-compose up -d
```

### 3. Backend Setup

```bash
cd kemit_backend

# Install Node.js dependencies
npm install

# Set up environment variables
cp config.env.example config.env
# Edit config.env with your database and API keys

# Start development server
npm run dev
```

### 4. Flutter App Setup

```bash
cd kemit_flutter_app

# Install Flutter dependencies
flutter pub get

# Run on device/emulator
flutter run
```

### 5. Web App Setup

```bash
cd kemit_landing_page

# Install dependencies
npm install

# Start development server
npm start
```

## 🔧 Configuration

### Environment Variables

#### AI Component (.env)
```bash
# API Keys
EMBEDDER_API_KEY=your_google_ai_key

# MinIO Configuration
MINIO_ROOT_USER=kemit
MINIO_ROOT_PASSWORD=asdASD44;
MINIO_BUCKET=kemitservices
MINIO_ENDPOINT=192.168.1.5:9000

# Ollama Configuration
OLLAMA_MODEL_NAME=llama3.1:8b
BASE_OLLAMA_URL=http://ollama:11434

# Model Paths
CNN_MODEL_PATH=/app/models/brave_pharos_detection_model256.h5
WAVE_LIB_MODEL_PATH=/app/models/wav2lip.pth
MALE_VOICE_PATH=/app/reference_audio/male.mp3
FEMALE_VOICE_PATH=/app/reference_audio/female.mp3

# Data Paths
VECTORS_DIR_NAME=/app/vectors_data_bases
PROMPTS_FILE_PATH=/app/reference_data/prompts.json
KINGS_DESCRIPTIONS_JSON_PATH=/app/reference_data/kings_descriptions.json
```

#### Backend (config.env)
```bash
# Database
MONGODB_URL=mongodb://localhost:27017/kemit

# JWT
JWT_SECRET=your_jwt_secret
JWT_EXPIRES_IN=90d

# Email
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_app_password

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Server
PORT=8000
NODE_ENV=development
```

## 📱 API Documentation

### AI Component Endpoints

#### Chat Endpoint
```http
POST /chat/
Content-Type: application/json

{
  "text": "Tell me about the Pyramids of Giza"
}
```

#### Image Classification Endpoint
```http
POST /cnn_model/
Content-Type: multipart/form-data

file: [image_file]
lang: "en"
```

### Backend API Endpoints

#### Authentication
```http
POST /api/v1/auth/signup
POST /api/v1/auth/signin
POST /api/v1/auth/forgotPassword
```

#### Chat Management
```http
POST /api/v1/chatbot/text
GET /api/v1/chatbot/text?page=1&limit=10
POST /api/v1/chatbot/image
GET /api/v1/chatbot/image?page=1&limit=10
```

#### Places & Location
```http
GET /api/v1/places/near?lat=30.0444&lng=31.2357&radius=5000
GET /api/v1/places
POST /api/v1/places
```

## 🧪 Testing

### AI Component Testing
```bash
cd kemit_ai_component

# Test CNN model
python -m pytest tests/test_cnn.py

# Test RAG system
python -m pytest tests/test_rag.py

# Test TTS service
python -m pytest tests/test_tts.py
```

### Backend Testing
```bash
cd kemit_backend

# Run unit tests
npm test

# Run integration tests
npm run test:integration
```

### Flutter Testing
```bash
cd kemit_flutter_app

# Run unit tests
flutter test

# Run widget tests
flutter test test/widget_test.dart
```

## 🚀 Deployment

### Production Deployment

#### 1. AI Component (Docker)
```bash
cd kemit_ai_component

# Build and deploy
docker-compose -f docker-compose.prod.yml up -d

# Scale services
docker-compose up -d --scale kemit-api=3
```

#### 2. Backend (Node.js)
```bash
cd kemit_backend

# Build for production
npm run build

# Start production server
NODE_ENV=production npm start
```

#### 3. Flutter App
```bash
cd kemit_flutter_app

# Build Android APK
flutter build apk --release

# Build iOS
flutter build ios --release

# Build Web
flutter build web --release
```

#### 4. Web App
```bash
cd kemit_landing_page

# Build for production
npm run build

# Deploy to GitHub Pages
npm run deploy
```

### Monitoring & Logging

- **Application Logs**: Structured logging with request IDs
- **Performance Monitoring**: Response time tracking
- **Error Tracking**: Comprehensive error handling
- **Health Checks**: Service health monitoring

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Development Guidelines

- Follow the existing code style and conventions
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Ancient Egypt Dataset**: [Egypt Monuments Dataset](https://github.com/marvy-ayman/egypt-monuments-dataset)
- **AI Models**: Hugging Face, Ollama, Google Generative AI
- **Open Source Libraries**: Flutter, React, FastAPI, Node.js community

## 📞 Contact

- **Project Link**: [https://github.com/your-username/FULL_KEMIT](https://github.com/your-username/FULL_KEMIT)
- **Issues**: [GitHub Issues](https://github.com/your-username/FULL_KEMIT/issues)

---

<div align="center">
  <p>Made with ❤️ for preserving and sharing Egypt's rich cultural heritage</p>
  <p>🏛️ KEMIT - Where Ancient History Meets Modern AI 🏛️</p>
</div> 
