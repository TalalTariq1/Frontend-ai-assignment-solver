# AI Assignment Solver 🚀

A full-stack AI application that transforms assignment documents into formatted programming solutions. Upload a `.docx` lab manual, and get a professional Word document with AI-generated code in seconds.

**Live Site:** [https://assignment-solver-seven.vercel.app/](https://assignment-solver-seven.vercel.app/)

---

## 🏗️ System Architecture & Stack

This project follows a **Decoupled Full-Stack Architecture**, separating the user interface from the heavy-lifting AI processing logic.

### 1. Frontend (The UI)
- **Hosted on:** Vercel
- **Tech Stack:** React.js, Tailwind CSS, Vite.
- **Key Function:** Manages the user form and file upload. It uses a **Secure Blob Download** system to handle cross-origin file delivery reliably across different browsers.

### 2. Backend (The Engine)
- **Hosted on:** Railway
- **Tech Stack:** FastAPI (Python), Gunicorn, Uvicorn, Python-Docx.
- **Key Function:** A microservice that parses `.docx` binary data, communicates with the Groq Llama-3 API, and dynamically rebuilds a new Word document containing the solutions.

### 3. AI Intelligence
- **Model:** Llama-3.3-70B-Versatile (via Groq Cloud)
- **Specialization:** High-speed technical code generation with zero conversational filler, specifically tuned for academic and laboratory tasks.

---

## 🚀 How It Works (Technical Flow)

1.  **Client-Side:** The user inputs metadata (Name, Roll No, etc.) and attaches a `.docx` assignment.
2.  **API Request:** React sends a `multipart/form-data` POST request to the FastAPI server on Railway.
3.  **Extraction:** The backend extracts raw text from the uploaded document using `python-docx`.
4.  **AI Inference:** The extracted text is sent to the Groq API with a system prompt to generate clean, accurate code for each task.
5.  **Document Rebuild:** The backend creates a new `.docx` file, injecting the student's header information and the AI-generated solutions.
6.  **Secure Download:** The frontend receives the file path, fetches the file as a `Blob`, and triggers a native browser download.

---

## 🛠️ Key Features

- **Automated Formatting:** Injects Name, Roll Number, Section, and Subject into the output header.
- **Multi-Language Support:** Solve assignments in Python, Java, C++, and more.
- **Intelligent Parsing:** Identifies individual tasks within the manual and organizes them with clear headings.
- **Modern UI:** Responsive, dark-mode design styled with Tailwind CSS.

---

## 💻 Local Development

1. **Clone the Project:**
   ```bash
   git clone [your-frontend-repo-link]
   npm install
   npm run dev

   Backend Configuration:

   
The frontend is currently pointing to the production API at: https://web-production-187bb.up.railway.app.

🔒 Security Note
The Backend repository is kept private to protect API credentials and the proprietary document-parsing logic. All sensitive keys are managed via secure Environment Variables on the Railway platform.

📝 License
Distributed under the MIT License.

Author: [Your Name]

Project Link: https://github.com/your-username/assignment-solver-frontend
