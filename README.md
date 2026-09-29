AI API Assignment

📌 Project Overview

This project demonstrates how to use AI APIs with Python.
The assignment includes examples using Groq API and Google Gemini API to generate AI-based responses.

🛠️ Technologies Used

- Python
- Google Colab
- Groq API
- Google Gemini API
- GitHub

📂 Files

AI_API_Assignment/
│
├── OpenAI.ipynb
├── Gemini.ipynb
└── README.md

🔑 API Keys

The API keys are stored securely using Google Colab Secrets.

Required secrets:

GROQ_API_KEY
GEMINI_API_KEY

Do not upload or share API keys publicly.

🚀 Groq API

Install the required library:

!pip install groq

Import the required modules:

import os
from groq import Groq
from google.colab import userdata

os.environ["GROQ_API_KEY"] = userdata.get("GROQ_API_KEY")

client = Groq()

Generate a response:

completion = client.chat.completions.create(
    model="qwen/qwen3.8-27b",
    messages=[
        {
            "role": "user",
            "content": "What is the largest continent and what is its approximate population in numbers?"
        }
    ]
)

print(completion.choices[0].message.content)

🤖 Google Gemini API

Install the required library:

!pip install google-genai

Initialize Gemini:

import os
from google import genai
from google.colab import userdata

os.environ["GEMINI_API_KEY"] = userdata.get("GEMINI_API_KEY")

client = genai.Client()

Generate a response:

response = client.models.generate_content(
    model="gemini-3.8-flash",
    contents="What is the closest habitable planet in our galaxy according to scientists? Answer in one line."
)

print(response.text)

📊 Expected Result

The APIs generate answers based on the prompts provided by the user.

Example:

Groq API → Generates an AI response
Gemini API → Generates an AI response

🎯 Learning Objectives

Through this assignment, we learn:

1. How to install AI API libraries.
2. How to securely store API keys.
3. How to connect Python programs with AI APIs.
4. How to send prompts to AI models.
5. How to display AI-generated responses.
6. How to use GitHub for project documentation.

👨‍💻 Author

Bishaldeb Mandal

B.Tech CSE (Data Science)

The Neotia University
