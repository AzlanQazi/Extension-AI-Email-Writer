# 🚀 AI Email Response Assistant

A full-stack AI-integrated solution to automate email drafting using Google's Gemini Pro.

---

## 📂 Project Structure
This repository is a **Monorepo** containing three distinct components:

* **`email-writer-sb/`** – Spring Boot Backend (Java 17, WebFlux).
* **`email-writer-react/`** – Web Dashboard (React.js, Tailwind CSS).
* **`email-writer-ext/`** – Chrome Extension (JavaScript, Gmail DOM Injection).

---

## ✨ Key Features
- **One-Click AI Replies:** Injects a custom "AI Reply" button directly into the Gmail UI.
- **Smart Context Awareness:** Scrapes the original email thread to generate relevant responses.
- **Tone Customization:** Choose between *Professional*, *Casual*, or *Friendly* tones.
- **Modern Tech Stack:** Uses non-blocking `WebClient` for high-performance AI integration.

---

## 🏗️ System Architecture
The system operates on a request-response cycle across three layers:

1.  **Client Layer:** Chrome Extension captures email content and sends a `POST` request.
2.  **API Layer:** Spring Boot processes the request, builds a prompt, and calls Gemini API.
3.  **AI Layer:** Google Gemini generates the text and returns it to be injected into Gmail.



---

## 🚀 Getting Started

### 1. Backend Setup (Spring Boot)
Navigate to `/email-writer-sb` and configure your API keys:
- Set `GEMINI_KEY` in your environment variables.
- Run `./mvnw spring-boot:run`.

### 2. Frontend Setup (React)
Navigate to `/email-writer-react`:
- Run `npm install` and `npm start`.

### 3. Extension Setup
- Open `chrome://extensions/` in Chrome.
- Enable **Developer Mode**.
- Click **Load unpacked** and select the `/email-writer-ext` folder.

---

## 🛠️ Technical Highlights
- **Reactive Programming:** Implemented `WebClient` for efficient API calls.
- **Cross-Origin Security:** Configured CORS to allow the extension to communicate with the Render-hosted API.
- **Prompt Engineering:** Custom logic to transform raw email text into high-quality AI prompts.
