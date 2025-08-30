 # AI-Powered Physiotherapy & Medical Report Assistant

An intelligent healthcare assistant that combines computer vision, natural language processing, and conversational AI to provide: Real-time posture analysis & physiotherapy guidance
Medical report summarization using OCR + NLP
Interactive chatbot powered by GPT4All for health queries and daily reminders
This project aims to make physiotherapy, medical interpretation, and health tracking accessible to patients anywhere, without requiring constant doctor supervision.

# Features
🔹 Posture Analysis
-Detects posture using MediaPipe/OpenPose keypoint extraction
-Supports sitting posture, squats, push-ups, and extensible to yoga & mobility routines
-Provides real-time correction feedback (visual/audio cues)
-Tracks reps, errors, and progress over time

🔹 Medical Report Understanding
-Upload reports in PDF, JPG, PNG, or DICOM
-OCR extracts text from scans and documents
-NLP pipeline (SBERT + FAISS) converts medical jargon into patient-friendly summaries
-Dashboard with report storage and downloadable summaries

🔹 Conversational Chatbot (GPT4All)
-Hybrid RAG pipeline:
-High similarity queries → Report-specific answers
-Low similarity queries → GPT4All fallback for physiotherapy/health guidance
-Explains medical reports, suggests exercises, and answers health queries
-Includes daily reminders (hydration, sleep, exercise schedule)

🔹 Lifestyle & Reminders
-Calendar-based schedule for exercises & follow-ups
-Custom reminders for water intake, sleep routine, fitness goals
-Progress dashboard for tracking improvements

# System Architecture
Frontend: Flutter / React.js
Minimalist, accessible UI with 5-tab navigation (Exercise, Camera, Consultation, Upload, Schedule)
Sidebar profile dashboard with patient details

Posture Model:
MediaPipe/OpenPose for skeleton extraction
Angle calculation + ML classifier for error detection
TensorFlow Lite optimization for mobile
OCR + NLP:
Tesseract OCR for text extraction
SBERT embeddings + FAISS vector DB for semantic search
Summarization using transformer-based models
Chatbot Engine:
Retrieval-Augmented Generation (RAG)
GPT4All as fallback LLM for general health queries
Context-aware conversation with report + posture data
