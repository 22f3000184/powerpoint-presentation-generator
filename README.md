# AI Presentation Generator

An intelligent web application that transforms raw, unstructured text into a fully formatted and downloadable PowerPoint (.pptx) presentation. The application uses Google's **Gemini Pro** model via **LangChain** to first generate a structured plan, which is then converted into a presentation file, providing an interactive and intelligent user experience.

<!-- TODO: Add a screenshot of your application here -->

---

✨ **Features**

* **Dynamic Content Planning**: The AI first generates a logical plan for the presentation, which is displayed to the user in real-time with a typewriter effect, making the process feel interactive and intelligent.
* **Custom Slide Count**: Users can specify the exact number of slides they want in the final presentation, giving them full control over the output.
* **In-Memory File Generation**: PowerPoint files are created entirely in memory and streamed directly to the user. This is highly efficient and secure as no files are ever stored on the server.
* **Interactive UI**: A clean, multi-step user interface guides the user through the process, from input to final download.
* **Ready for Deployment**: Comes with a Dockerfile and `render.yaml` for easy, one-click deployment on a platform like Render.

---

🛠️ **Tech Stack**

* **Backend**: Flask, Gunicorn
* **AI/LLM**: Google Gemini Pro, LangChain
* **File Generation**: python-pptx
* **Frontend**: HTML, Tailwind CSS
* **Deployment**: Docker, Render

---

📂 **Project Structure**

```
├── .env                # For storing secret API keys locally
├── Dockerfile          # Blueprint for building the production container
├── main.py             # The core Flask application logic and API endpoints
├── README.md           # This file
├── render.yaml         # Infrastructure-as-Code for deployment on Render
├── requirements.txt    # Python dependencies
└── templates/
    └── index.html      # The main HTML file for the user interface
```

---
