# AI Chatbot using Flask and OpenAI

This is a simple web-based **AI Chatbot** built with **Flask (Python)** on the backend and **HTML + JavaScript** on the frontend.  
It connects to OpenAI's GPT model (`gpt-4o-mini`) to generate intelligent responses to user messages.

---

## Features

- Simple, responsive web chat interface  
- Real-time message exchange with AI  
- Powered by **OpenAI GPT-4o-mini**  
- Easy to configure and deploy locally  

---

## Project Structure
AI-chatbot-project---mini/
│
├── app.py # Flask backend (handles API requests)
├── templates/
│ └── index.html # Frontend chat interface
├── requirements.txt # Dependencies
└── README.md # Project documentation

## Installation and Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-username/AI-chatbot-project---mini.git
cd AI-chatbot-project---mini
```
### 2. Create and activate a virtual environment
```bash
python -m venv venv
source venv/bin/activate     # On Windows cmd: venv\Scripts\activate
```
### 3. Install dependencies
Create a requirements.txt file containing:
```nginx
flask
openai
```
Then install:
```bash
pip install -r requirements.txt
```
### 4. Set up your OpenAI API key
On Linux/Mac:
```bash
export OPENAI_API_KEY="your_api_key_here"
```
On Windows (PowerShell):
```powershell
setx OPENAI_API_KEY "your_api_key_here"
```
You can get your API key from https://platform.openai.com/account/api-keys

### 5. Run the Flask app
```bash
python app.py
```

## Example Interaction
```makefile
You: Hello
AI: Hi there! How can I assist you today?
```

## Troubleshooting
| Issue	                                        | Possible Fix                                                                |
|-----------------------------------------------|-----------------------------------------------------------------------------| 
| AI: undefined	                                | Check that your backend returns {"reply": ...} and your JS reads data.reply.|
| Error: No API key provided	                  | Ensure your OPENAI_API_KEY environment variable is set before running Flask.|
| ModuleNotFoundError: No module named 'openai'	| Run pip install openai flask again inside your virtual environment.         |

## How It Works
1. Frontend (index.html) — sends user messages to the backend using fetch() with JSON.
2. Backend (Flask app.py) — receives messages via /chat, queries the OpenAI API, and returns the AI-generated response.
3. AI Model (OpenAI GPT-4o-mini) — generates natural language replies based on the user’s input.

## Technologies Used
1. Python
2. Flask
3. OpenAI API
4. HTML5 / JavaScript

## License

This project is licensed under the MIT License — feel free to modify and use it for personal or educational purposes.

## Future Enhancements
1. Add chat history persistence using SQLite or PostgreSQL
2. Include a typing animation (“AI is typing...”)
3. Improve UI with CSS or a frontend framework (React, Vue, etc.)
4. Enable multi-user sessions



