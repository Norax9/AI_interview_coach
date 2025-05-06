# AI Interview Coach

## 📌 Project Goal

The AI Interview Coach is an AI-powered web application designed to assist users in enhancing their interview skills. It provides personalized feedback by analyzing both verbal and non-verbal communication aspects, including:

- **Verbal Analysis**: Evaluating spoken responses through speech-to-text transcription.
- **Facial Expression Analysis**: Assessing emotions and expressions during responses.
- **Posture Analysis**: Monitoring body language and posture.
- **CV-Based Question Generation**: Creating tailored interview questions based on the user's resume.

By offering real-time, comprehensive feedback, the application aims to help users build confidence and improve their performance in actual interviews.

---

## 🧠 Project Architecture

The system is structured into modular components to ensure scalability and maintainability:

1. **User Interface (Gradio)**
   - Facilitates user interactions, including CV uploads and video recordings.
   - Displays generated questions and feedback in an intuitive layout.

2. **CV Processing Module**
   - Parses uploaded resumes to extract relevant information.
   - Utilizes a Retrieval-Augmented Generation (RAG) system to generate personalized interview questions based on CV content.

3. **Interview Response Analysis**
   - **Speech-to-Text Transcription**: Converts spoken responses into text using OpenAI's Whisper model.
   - **Facial Expression Analysis**: Detects and interprets facial emotions using DeepFace.
   - **Posture Analysis**: Evaluates body posture and gestures through MediaPipe and OpenCV.

4. **RAG + GPT Question Answering**
   - Retrieves pertinent information from the CV using a vector store.
   - Generates context-aware interview questions and evaluates responses using GPT models.

5. **Feedback Generation Engine**
   - Integrates data from all analysis modules.
   - Produces detailed feedback on verbal communication, facial expressions, body language, and the relevance and clarity of answers.

6. **Output Delivery**
   - Presents comprehensive feedback and performance metrics through the Gradio interface, guiding users on areas for improvement.

---

## ✅ Testing Methodology

To ensure the reliability and effectiveness of the application, the following testing strategies were employed:

- **Unit Testing**
  - Validated individual modules such as CV parsing, speech transcription, emotion detection, and posture analysis with diverse input scenarios.

- **Integration Testing**
  - Assessed the seamless interaction between modules from CV upload to feedback generation.

- **Performance Testing**
  - Measured system responsiveness and latency to guarantee real-time feedback delivery.

- **RAG System Evaluation with LangSmith**
  - Employed LangSmith to trace, debug, and evaluate the Retrieval-Augmented Generation pipeline.
  - Analyzed the relevance and consistency of generated questions and answers.
  - Enhanced retrieval accuracy and response coherence based on LangSmith insights.
