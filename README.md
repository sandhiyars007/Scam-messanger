# Scam Identifier

## Project Overview

Scam Identifier is an AI-powered message analysis application that helps users identify potential scam messages and understand their warning signs.

The application uses a locally running Large Language Model (LLM) through Ollama to examine suspicious messages and generate a structured investigation report.

It focuses on detecting common scam indicators such as urgent threats, suspicious links, requests for sensitive information, fake rewards, and misleading offers.

 Features

- AI-powered scam message analysis
- Local LLM integration using Ollama
- Risk level classification:
  - Low Concern
  - Medium Concern
  - High Concern
- Message category identification
- Detailed explanation of warning signs
- Recommended safety actions
- Investigation limitations
- JSON-based structured responses
- Interactive user interface using Streamlit
- Local message processing without sending message content to a cloud AI API

 Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | User interface development |
| Ollama | Local LLM execution |
| Gemma 3:1B | Language model |
| Requests | API communication |
| JSON | Structured investigation results |

 System Architecture

1. User enters a suspicious message.
2. Streamlit collects the message.
3. Python sends the message to the local Ollama API.
4. Gemma 3:1B analyzes the message using predefined system instructions.
5. The model generates a structured JSON response.
6. Python processes the response.
7. Streamlit displays the investigation report.

 Project Structure

```text
Scam_Identifier/
│
└── app.py
```

 Installation and Setup

 1. Install Python

Download and install Python from:

https://www.python.org/downloads/

2. Install Ollama

Download Ollama from:

https://ollama.com/download

3. Download the Gemma Model

Open the terminal and execute:

```bash
ollama pull gemma3:1b
```
 4. Install Required Libraries

```bash
py -m pip install streamlit requests
```

5. Run the Application

Navigate to the project directory and execute:
py -m streamlit run app.py
The application will open in your default web browser.

Sample Input

```text
URGENT! Your bank account will be blocked today.
Verify your account immediately to avoid suspension.
You have won a reward of Rs. 50,000.
Claim your prize immediately!
```

Expected Output

The application generates an investigation report containing:

- Risk Level
- Message Type
- Summary
- Warning Signs
- Recommended Safety Actions
- Investigation Limitations

 Privacy and Security

- The application uses a locally running Ollama service.
- Message content is processed locally by the configured model.
- No cloud-based AI API is required.
- Users should avoid entering real passwords, OTPs, PINs, or other confidential information.

Limitations

- AI-generated results may not always be accurate.
- The application cannot independently verify the sender's identity.
- It cannot guarantee whether a message is legitimate or fraudulent.
- Suspicious messages should always be verified through official communication channels.

Future Enhancements

- URL safety analysis
- Email scam detection
- SMS scam detection
- Phishing website identification
- Detection history and report management
- Improved risk classification
- Multilingual scam message analysis

Conclusion

Scam Identifier provides an AI-powered approach to analyzing suspicious messages using a locally running language model. It helps users understand potential scam indicators and make more informed digital safety decisions.

The project demonstrates the practical application of Large Language Models, Python, API integration, and Streamlit in cybersecurity awareness.


author
sandhiya.R
