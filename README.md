# PowerPoint Presentation Generator  

[![Built with Flask](https://img.shields.io/badge/Built%20with-Flask-000000?logo=flask&logoColor=white)](https://flask.palletsprojects.com/)  
[![LangChain](https://img.shields.io/badge/AI-LangChain-blue?logo=chainlink&logoColor=white)](https://www.langchain.com/)  
[![Powered by Gemini Pro](https://img.shields.io/badge/Powered%20by-Google%20Gemini-4285F4?logo=google&logoColor=white)](https://ai.google/)  
[![Deploy on Render](https://img.shields.io/badge/Deploy%20on-Render-46E3B7?logo=render&logoColor=white)](https://render.com/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)  

---

A smart web application that transforms raw text into a polished, ready-to-download **PowerPoint presentation**. Using Google’s **Gemini Pro** model with **LangChain**, the app structures unorganized content into slides, then generates a `.pptx` file with proper formatting.  

---

✨ **Key Features**  

- **AI-Powered Slide Planning**: Automatically organizes input text into slide titles and bullet points.  
- **Customizable Slide Count**: Choose exactly how many slides you want.  
- **Instant File Creation**: Presentations are generated fully in memory and delivered directly to your browser.  
- **Interactive UI**: A clean, simple interface guides you step-by-step.  
- **One-Click Deployment**: Docker and `render.yaml` make it deployment-ready on Render.  

---

🛠️ **Tech Stack**  

- **Backend**: Flask + Gunicorn  
- **AI**: Google Gemini Pro (via LangChain)  
- **File Handling**: python-pptx  
- **Frontend**: HTML + Tailwind CSS  
- **Deployment**: Docker, Render  

---

📂 **Project Layout**  

```
├── main.py             # Flask backend  
├── requirements.txt    # Dependencies  
├── Dockerfile          # Container setup  
├── render.yaml         # Render deployment config  
├── templates/          # HTML templates  
└── README.md           # This file  
```

---

## 📝 How It Works (200 Words)  

This application acts as an intelligent assistant for creating presentations. The user begins by entering unstructured text along with the desired number of slides. The backend then calls Google’s **Gemini Pro** model through LangChain, which converts the raw input into a well-structured markdown outline. Each section of this outline corresponds to a slide, complete with a title and bullet points.  

Once the plan is generated, the app gives users the option to refine or improvise the content based on feedback. When finalized, the markdown outline is passed to a **PowerPoint generator** powered by the `python-pptx` library. This library dynamically creates slides, applies titles, and inserts bullet points into the presentation file. Importantly, the file is never stored on the server. Instead, it is created in memory and streamed directly back to the user’s browser for download, ensuring both efficiency and security.  

The interface, built using **Flask templates with Tailwind CSS**, makes the workflow straightforward: input text → AI-generated slide plan → preview and refine → download `.pptx`. Deployed with Docker on Render, the system is lightweight, scalable, and accessible anywhere. In short, this app saves time and effort by automating the most repetitive parts of presentation creation.  

---

## 🚀 Deployment on Render  

Follow these steps to host your app on **Render**:  

1. **Push Code to GitHub**  
   - Make sure your project (with `render.yaml`, `Dockerfile`, and all files) is in a GitHub repository.  

2. **Create a New Service on Render**  
   - Go to [https://dashboard.render.com](https://dashboard.render.com).  
   - Click **New + → Blueprint**.  
   - Connect your GitHub repo.  

3. **Render Auto-Detection**  
   - Render will detect the `render.yaml` file and configure everything automatically.  

4. **Set Environment Variable**  
   - Go to your service’s **Environment** tab.  
   - Add a new variable:  
     - `GOOGLE_API_KEY` → (Your Google Gemini API key).  

5. **Deploy**  
   - Click **Deploy** and wait for the build.  
   - Once deployed, your app will be live at:  
     ```
     https://powerpoint-presentation-generator.onrender.com
     ```  

6. **Use the App**  
   - Enter text → Choose slide count → Generate → Download your `.pptx` presentation.  
