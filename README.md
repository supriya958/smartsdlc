# SmartSDLC – AI-Enhanced Software Development Lifecycle

SmartSDLC is a full-stack, AI-powered platform that redefines the traditional Software Development Lifecycle (SDLC) by automating key stages using advanced Natural Language Processing (NLP) and Generative AI technologies.

It is not just a tool — it's an intelligent ecosystem that allows teams to convert unstructured requirements into code, test cases, and documentation instantly, thereby minimizing manual intervention, enhancing accuracy, and accelerating the delivery pipeline.

---

## Features / Scenarios

### Scenario 1: Requirement Upload and Classification
- Upload PDF documents containing raw, unstructured text.
- Extract content using PyMuPDF.
- Classify sentences into SDLC phases using IBM Watsonx’s Granite-20B AI model.
- Transform classified input into structured user stories.
- Frontend displays grouped results by SDLC phase for clarity.

### Scenario 2: AI Code Generator
- Input natural language prompts or user stories.
- Generate production-ready code via Watsonx AI.
- Code displayed with syntax highlighting for easy use.

### Scenario 3: Bug Fixer
- Accept buggy Python or JavaScript code.
- AI analyzes and returns corrected, optimized code.
- Compare original and fixed code in frontend.

### Scenario 4: Test Case Generator
- Generate unit or integration test cases from code or requirements.
- Uses unittest/pytest style for seamless automation.

### Scenario 5: Code Summarizer
- Generate human-readable explanations for code snippets.
- Useful for documentation and onboarding.

### Scenario 6: Floating AI Chatbot Assistant
- Conversational AI chatbot powered by LangChain.
- Answer SDLC-related queries in real-time.
- Intuitive chat interface integrated into the platform.

---

## Milestones and Development Phases

### Milestone 1: Model Selection and Architecture
- Research and select IBM Watsonx Granite models for NLP and code generation.
- Define system architecture: Streamlit frontend + FastAPI backend.
- Integrate AI workflow via Watsonx APIs and LangChain orchestration.
- Set up development environment and project structure.

### Milestone 2: Core Functionalities Development
- Implement key AI-powered SDLC modules:
  - Requirement analysis
  - Code generation
  - Test case generation
  - Bug fixing
  - Documentation generation
  - Chatbot assistance
  - Feedback collection
  - GitHub integration
- Develop FastAPI backend with routing, authentication, and service layers.

### Milestone 3: User Interface Design and Integration
- Build modular Streamlit pages for each core feature.
- Responsive UI with custom CSS and clean layout.
- Backend API integration using requests for real-time communication.
- Floating chatbot embedded on frontend.

### Milestone 4: Deployment and Local Testing
- Setup Python virtual environments.
- Configure environment variables securely with `.env`.
- Run backend (FastAPI + Uvicorn) and frontend (Streamlit) locally.
- Test all functionalities end-to-end.

---

## Getting Started

### Prerequisites
- Python 3.9+
- IBM Watsonx API credentials (API Key, Project ID, Model ID)
- Required Python packages (listed in `requirements.txt`)

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/pravallika4218/smartsdlc.git
   cd smartsdlc
Create and activate a virtual environment

bash
Copy
Edit
python3 -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
Install dependencies

bash
Copy
Edit
pip install -r requirements.txt
Create a .env file in the root directory with:

env
Copy
Edit
WATSONX_API_KEY=your_ibm_watsonx_api_key
WATSONX_PROJECT_ID=your_project_id
WATSONX_MODEL_ID=granite-20b-code-instruct
Running the Application
Start the FastAPI backend

bash
Copy
Edit
uvicorn app.main:app --reload
API docs available at: http://127.0.0.1:8000/docs

Start the Streamlit frontend

bash
Copy
Edit
streamlit run frontend/Home.py
Open in browser: http://localhost:8501

Project Structure
bash
Copy
Edit
smartsdlc/
├── app/                  # FastAPI backend modules
│   ├── ai_story_generator.py
│   ├── code_generator.py
│   ├── bug_resolver.py
│   ├── doc_generator.py
│   ├── conversation_handler.py
│   ├── chat_routes.py
│   ├── feedback_routes.py
│   ├── feedback_model.py
│   ├── github_service.py
│   └── main.py           # FastAPI app entrypoint
├── frontend/             # Streamlit UI files
│   ├── Home.py
│   ├── Upload_and_Classify.py
│   ├── Code_Generator.py
│   ├── Test_Generator.py
│   ├── Bug_Fixer.py
│   ├── Code_Summarizer.py
│   ├── Feedback.py
│   └── api_client.py
├── requirements.txt      # Backend dependencies
├── .env.example          # Sample environment variables file
├── README.md
└── LICENSE               # MIT License
Technologies Used
Python 3.9+

FastAPI (Backend API)

Streamlit (Frontend UI)

IBM Watsonx Granite-20B AI models

PyMuPDF (PDF text extraction)

LangChain (Conversational AI)

Uvicorn (ASGI server)

License
This project is licensed under the MIT License - see the LICENSE file for details.
