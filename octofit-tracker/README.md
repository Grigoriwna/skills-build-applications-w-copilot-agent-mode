# OctoFit Tracker - Modern Multi-Tier Application

A modern, full-stack fitness tracking application built with React 19, Vite, Express, TypeScript, and MongoDB.

## Project Structure

```
octofit-tracker/
├── frontend/          # React 19 + Vite application
│   ├── src/
│   ├── public/
│   ├── vite.config.js
│   ├── package.json
│   └── .env
├── backend/           # Express + TypeScript + Mongoose backend
│   ├── src/
│   │   └── server.ts
│   ├── tsconfig.json
│   ├── package.json
│   └── .env.example
└── README.md
```

## Technology Stack

### Frontend
- **React 19** - UI library
- **Vite** - Build tool and dev server
- **Port**: 5173

### Backend
- **Node.js** - Runtime
- **Express** - Web framework
- **TypeScript** - Type safety
- **Mongoose** - MongoDB ODM
- **Port**: 8000

### Database
- **MongoDB** - NoSQL database
- **Port**: 27017

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- npm (v7 or higher)
- MongoDB (running on localhost:27017)

### Installation

#### Backend Setup
```bash
cd backend
npm install
cp .env.example .env
# Update .env if needed (default values are already configured)
```

#### Frontend Setup
```bash
cd frontend
npm install
# .env is already configured with API URL
```

## Running the Application

### Start MongoDB
```bash
# If MongoDB is installed locally
mongod
# Or using Docker
docker run -d -p 27017:27017 --name mongodb mongo:latest
```

### Start the Backend
```bash
cd backend
npm run dev    # Development mode with hot reload
# or
npm run build  # Build for production
npm start      # Production mode
```

The backend server will be available at `http://localhost:8000`

### Start the Frontend
```bash
cd frontend
npm run dev    # Development mode with hot reload
# or
npm run build  # Build for production
npm run preview # Preview production build
```

The frontend will be available at `http://localhost:5173`

## API Endpoints

### Health Check
- `GET /health` - Returns API status

## Environment Variables

### Backend (.env)
```
PORT=8000
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
FRONTEND_URL=http://localhost:5173
```

### Frontend (.env)
```
VITE_API_URL=http://localhost:8000
```

## Scripts

### Backend
- `npm run dev` - Start development server with hot reload
- `npm run build` - Build TypeScript to JavaScript
- `npm start` - Run production build

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Features

- ✅ React 19 with latest features
- ✅ TypeScript for type safety
- ✅ MongoDB persistence with Mongoose
- ✅ Express REST API
- ✅ Hot module reloading in development
- ✅ CORS enabled for frontend-backend communication
- ✅ Environment configuration management

## Development Workflow

1. Ensure MongoDB is running
2. Start the backend server: `npm run dev` in the backend directory
3. Start the frontend server: `npm run dev` in the frontend directory
4. Open `http://localhost:5173` in your browser
5. The API is accessible at `http://localhost:8000`

## Building for Production

### Backend
```bash
cd backend
npm run build
npm start
```

### Frontend
```bash
cd frontend
npm run build
# Serve the dist folder
```

## Troubleshooting

### MongoDB Connection Issues
- Ensure MongoDB is running on port 27017
- Check connection string in backend `.env` file
- Verify network connectivity

### CORS Errors
- Frontend must be on `http://localhost:5173`
- Backend CORS is configured to allow all origins (update in production)

### Port Already in Use
- Frontend (5173): `lsof -i :5173` to find process
- Backend (8000): `lsof -i :8000` to find process
- MongoDB (27017): `lsof -i :27017` to find process

## License

ISC
