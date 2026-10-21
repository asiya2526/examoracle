# examoracle
ExamOracle - The AI Exam Survival Kit 
# 🎃 ExamOracle — The AI Exam Survival Kit

> *"Don't fear the exam. Unmask it."*

[![React](https://img.shields.io/badge/React-19.0-61DAFB?logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-6.x-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.x-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini-3.8_Flash-8E75B2?logo=google&logoColor=white)](https://ai.google.dev/)
[![Theme](https://img.shields.io/badge/Theme-Halloween_Trick_or_Treat-FF7518)](https://github.com/)

**ExamOracle** is a full-stack, AI-powered exam preparation platform built for college students facing large syllabi, disorganized previous-year question papers (PYQs), and tight deadlines. Designed around the college hackathon theme **"Trick or Treat?"**, ExamOracle replaces exam panic with evidence-based intelligence, adaptive revision planning, and Halloween gamification.

Unlike generic flashcard apps or static dashboards, ExamOracle calculates historical question recurrence from **actual uploaded past examination papers**, identifies individual student weak spots, and generates targeted practice questions with university marking rubrics.

---

## 🌟 Key Features

### 1. 📊 Evidence-Based PYQ Intelligence Engine (Core Differentiator)
- **Deterministic Recurrence Frequency**: Calculates question frequency strictly from distinct uploaded papers (e.g., 3 out of 4 papers = 75% appearance rate) rather than artificial AI guesses.
- **Priority Classification**:
  - `High Priority`: Recurring in $\ge 50\%$ of past exams and aligned with core syllabus modules.
  - `Needs Attention`: Heavy exam weight combined with low individual student quiz accuracy.
  - `Medium Priority`: Moderate historical recurrence (1–2 papers).
- **Traceable Source Documents**: Every question links directly to source papers (year, examination type, marks, and exact vs. conceptual match).
- **Paper-by-Paper Comparison Matrix**: Side-by-side comparison grid visualizing question trends across multiple years.

### 2. 📚 Subject & Syllabus Management
- **Hierarchical Structure**: Organize subjects into Units/Modules, Chapters, Topics, and Subtopics with estimated study hours and syllabus weight percentages.
- **AI Syllabus Extractor**: Paste raw course syllabi or documents to automatically extract structured modules using Google Gemini (`gemini-3.8-flash`).
- **Granular Progress Tracking**: Set confidence ratings (1–5 stars) and mastery statuses (`Not Started`, `Learning`, `Mastered`) per topic.

### 3. 📁 Multi-Format Document Processing
- Drag-and-drop file upload supporting PDF, DOCX, TXT, and scanned papers with text-paste fallback.
- Classify files into **Syllabus**, **PYQ Papers**, **Lecture Notes**, or **Reference Guides**.
- Server-side question extractor parses individual question numbers, marks, and concept tags.

### 4. ⚡ AI Question Generator
- Generate exam-style questions across difficulty levels (`Easy`, `Medium`, `Hard`) and formats (`MCQ`, `Short Answer 2–5M`, `Long Essay 10M`, `Numerical`).
- Includes step-by-step marking rubrics, expected answers, examiner deduction criteria, and ground-truth syllabus citations.
- Interactive in-card self-testing with immediate deterministic feedback.

### 5. 🔮 AI Doubt Solver (Oracle Tutor)
- Interactive conversational AI tutor grounded in uploaded course notes.
- **Mode Presets**: *Exam-Ready Answer*, *Step-by-Step Breakdown*, and *Explain Simply*.
- **Mark Shortcuts**: Instant templates for *2-Mark Quick Definitions*, *5-Mark Standard Answers*, and *10-Mark Detailed Essays*.
- Highlights **Examiner Keywords** that score points in grading and generates follow-up recall challenges.

### 6. ⚔️ Practice Arena & Halloween Boss Battles
- **4 Distinct Quiz Modes**:
  - *Quick Practice Sprint*: 3–5 rapid MCQs for fast daily recall.
  - *PYQ High-Frequency Drill*: Questions extracted directly from past papers.
  - *Weak Topic Rescue Drill*: Focuses on lowest-accuracy concepts diagnosed by the Oracle.
  - *The Final Boss*: Comprehensive 10-question monster exam with live Boss HP and Player HP bars! Score $\ge 80\%$ to defeat the boss.
- Deterministic objective scoring (no AI hallucinations for multiple-choice answers).
- AI Subjective Grader evaluates essays against university marking rubrics.

### 7. 📅 Personalized Revision Planner
- Adaptive daily revision schedule based on exam proximity, topic confidence, and past quiz mistakes.
- Displays transparent **"Why this was recommended"** explanations for every scheduled task.
- Interactive task completion with XP rewards and roll-over adaptation for missed tasks.

### 8. 📈 Progress Analytics & Transparent Exam Readiness
- Transparent Readiness formula clearly displayed:
  $$\text{Exam Readiness} = (\text{Coverage} \times 40\%) + (\text{Quiz Accuracy} \times 35\%) + (\text{PYQ Exposure} \times 25\%)$$
- Visual quiz accuracy trends over time.
- Diagnostic lists contrasting weakest topics ($< 70\%$ accuracy) against mastered concepts.

### 9. 🍬 Halloween Gamification & Mystery Cauldron
- Earn **XP**, maintain **Study Streaks**, and collect **Candy Tokens** through verified learning activities.
- Unlock themed achievement badges: *First Blood*, *Ghost Hunter*, *Pumpkin Scholar*, *Consistency Curse Breaker*, *Exam Slayer*, and *PYQ Archaeologist*.
- **Mystery Study Cauldron**: Spend 10 Candy Tokens to pull revision power-ups, motivational wisdom, and study tips.
- Demo Cohort Leaderboard comparing performance with peer students.

---

## 🛠️ Tech Stack & Architecture

| Layer | Technology |
|---|---|
| **Frontend** | React 19, TypeScript, Tailwind CSS v4, Lucide Icons |
| **Backend** | Express 4 running full-stack with Vite middleware (`server.ts`) |
| **AI Engine** | Google GenAI TypeScript SDK (`@google/genai`) using `gemini-3.8-flash` |
| **State & Persistence** | React Context API with Browser LocalStorage synchronization |
| **Styling & Theme** | Dark cyber-scholastic Halloween palette (Charcoal `#09090e`, Violet `#8b5cf6`, Amber `#f97316`) |
