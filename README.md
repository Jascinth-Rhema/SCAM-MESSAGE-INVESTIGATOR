# Scam Message Investigator

An AI-powered application that analyzes suspicious SMS messages, emails, WhatsApp messages, and online offers to identify potential scam indicators using a locally running Large Language Model (LLM).

## Overview

https://scam-message-investigator-e8sq3umjfefxgwhht3f4um.streamlit.app/

Scam Message Investigator helps users understand whether a message may contain suspicious or potentially fraudulent content.

The application uses **Gemma 3:1B through Ollama** to examine message content, identify warning signs, assess potential risk, and suggest appropriate safety actions.

Unlike cloud-based AI applications, this project uses a locally running language model for message analysis.

## Features

- **AI-Powered Message Analysis:** Examines messages using Gemma 3:1B.
- **Risk Assessment:** Classifies messages into Low Concern, Medium Concern, or High Concern.
- **Warning Sign Detection:** Identifies suspicious phrases and explains why they may be risky.
- **Message Classification:** Determines the likely category of a message.
- **Safety Recommendations:** Provides practical actions to help users avoid potential scams.
- **Investigation Limitations:** Explains what cannot be verified from message content alone.
- **Investigation History:** Maintains previously analyzed messages during the current session.
- **Local AI Processing:** Uses Ollama to run the language model locally.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Application development |
| Streamlit | User interface |
| Ollama | Local LLM execution |
| Gemma 3:1B | AI-powered message analysis |
| Requests | Communication with Ollama API |
| JSON | Structured AI responses |

## Project Architecture

1. User enters a suspicious message.
2. Streamlit sends the message to the local Ollama API.
3. Gemma 3:1B analyzes the message using a predefined system prompt.
4. The model generates a structured JSON response.
5. Python processes the response.
6. Streamlit displays the investigation report, including risk level, warning signs, and recommended actions.

## Project Structure

```text
Scam-Message-Investigator/
│
├── app.py
├── requirements.txt
└── README.md
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Scam-Message-Investigator.git
```

### 2. Navigate to the Project Directory

```bash
cd Scam-Message-Investigator
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Install Ollama

Download Ollama from:

https://ollama.com/

Install and start Ollama on your computer.

### 5. Download the Gemma Model

```bash
ollama pull gemma3:1b
```

### 6. Run the Application

```bash
streamlit run app.py
```

The application will open in your browser at:

```text
http://localhost:8501
```

## Requirements

Create a `requirements.txt` file containing:

```text
streamlit
requests
```

Additional requirements:

- Python 3.9 or later
- Ollama installed and running
- Gemma 3:1B model downloaded
- Internet connection for initial model download

## Risk Classification

| Risk Level | Description |
|---|---|
| Low Concern | No clear suspicious indicators identified |
| Medium Concern | Some potentially suspicious patterns detected |
| High Concern | Multiple significant scam indicators identified |

Risk classifications are AI-generated assessments and should not be treated as definitive proof of fraud.

## Limitations

- The application analyzes message text and does not independently verify the sender.
- It does not authenticate URLs, bank accounts, or phone numbers.
- AI-generated results may contain inaccuracies.
- A legitimate-looking message may still be fraudulent.
- A suspicious-looking message is not necessarily a scam.
- Analysis depends on the capabilities of the locally running language model.

## Future Enhancements

- URL reputation and phishing link detection.
- Email header analysis.
- Multilingual scam message detection.
- Image and screenshot-based scam detection.
- Improved investigation history and report export.
- Integration with trusted threat intelligence databases.


## Author

**Jascinth Rhema R**

GitHub: https://github.com/Jascinth-Rhema

---

Developed as an AI-powered digital safety project using Python, Streamlit, Ollama, and Gemma 3:1B.
