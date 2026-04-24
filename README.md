# AI Assignment Solver (Frontend)

A sleek, modern React application that allows students to upload assignment documents and receive AI-generated solutions in specific programming languages.

**Live Demo:** [https://assignment-solver-seven.vercel.app/](https://assignment-solver-seven.vercel.app/)

## 🚀 Overview

This frontend serves as the user interface for the AI Assignment Solver ecosystem. It handles student data collection, file uploads, and provides an interactive interface for viewing and downloading AI-generated results.

### Key Features
- **Student Profiling:** Input fields for Name, Roll Number, Section, and Subject.
- **Language Selection:** Choose the target programming language for the solution.
- **Secure File Upload:** Drag-and-drop support for `.docx` assignment files.
- **Async Processing:** Real-time loading states while the backend processes the AI logic.
- **Smart Download:** Dynamic file generation with a secure Blob-based download system.

## 🛠️ Tech Stack

- **Framework:** React.js (Vite)
- **Styling:** Tailwind CSS (Modern Dark Mode UI)
- **API Interaction:** Fetch API with Multipart/Form-Data
- **Deployment:** Vercel

## 🔌 API Integration

The frontend communicates with a FastAPI backend hosted on Railway. It sends student metadata and document files to the `/upload` endpoint and retrieves processed documents from the `/download` endpoint.

```javascript
// Example Endpoint Configuration
const API_BASE_URL = "[https://web-production-187bb.up.railway.app](https://web-production-187bb.up.railway.app)";
