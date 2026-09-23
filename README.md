# Ashka Email App

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Google%20Gemini-AI-8A2BE2?style=for-the-badge" alt="Gemini AI" />
  <img src="https://img.shields.io/badge/Notebook-Colab-FF6F61?style=for-the-badge" alt="Colab" />
</p>

A modern email generation and enhancement project powered by Google Gemini AI. This app helps users convert raw email ideas into polished, professional, and purpose-driven email drafts for multiple business and personal scenarios.

## Overview

Ashka Email App is a lightweight AI-powered notebook-based project that uses the Google GenAI SDK to generate clean and professional emails from basic user input. Instead of writing messages manually, users can provide a rough draft or a set of details, and the system transforms it into a high-quality email tailored to the use case.

The project demonstrates how AI can be used for:

- improving existing email text
- generating formal business messages
- creating customer-facing communication
- producing context-aware responses for hospitality and sales scenarios

## Project Features

- AI-powered email improvement
- Professional grammar and tone correction
- Context-aware email generation
- Support for marketing, leave, and booking communication
- Easy-to-run notebook workflow in Google Colaboratory
- Secure API key handling using `getpass()`

## Email Generation Types

This project showcases multiple email generation styles, each designed for a different communication need.

### 1. General Email Improvement

Best for:
- rough drafts
- informal messages
- non-native writing
- business communication clean-up

Example use case:
- improving a promotional message for a product launch
- refining grammar and structure without changing the core intent

Typical output:
- corrected grammar
- professional tone
- polished formatting
- clearer message flow

### 2. Leave Request Email

Best for:
- employee leave applications
- manager communication
- time-off requests

Example use case:
- a staff member requests 2 days of leave
- the app generates a formal leave message with a respectful tone

Typical output:
- subject line
- greeting
- request explanation
- work handover note
- closing and signature

### 3. Hotel Booking Response

Best for:
- customer support
- hospitality communication
- reservation inquiries

Example use case:
- a guest sends booking details
- the system returns a professional booking request response

Typical output:
- polite greeting
- acknowledgment of request
- booking details summary
- note about room availability
- professional closing

### 4. Promotional / Marketing Email

Best for:
- product announcements
- campaign promotions
- sales outreach
- brand awareness messaging

Example use case:
- marketing a smartphone launch or product update
- generating an attractive sales email with subject line, features, CTA, and value proposition

Typical output:
- catchy subject
- engaging product positioning
- feature highlights
- promotional call-to-action
- brand-friendly closing

---

## Visual Summary of Email Types

| Email Type | Purpose | Example Output |
|---|---|---|
| General Improvement | Polishes rough text | Refined and professional email |
| Leave Request | Formal employee communication | Permission request with structured format |
| Hotel Booking | Reservation-related follow-up | Customer confirmation request message |
| Promotional Email | Sales and marketing promotion | Product announcement and CTA email |

## How It Works

1. The user enters a Gemini API key.
2. The user provides raw email content or business details.
3. A prompt is created based on the scenario.
4. Google Gemini generates a refined, suitable email response.
5. The result is displayed in the notebook output.

## Tech Stack

- Python
- Google GenAI SDK
- Google Gemini model
- Jupyter Notebook / Google Colab

## Installation

Run the following in a Python environment or Google Colab:

```bash
pip install google-auth==2.49.0
pip install google-genai==2.12.0
```

## Usage

Open the notebook file:

```text
Email_Appipynb.ipynb
```

Then:

1. Run the notebook cells
2. Enter your Gemini API key
3. Input the email text or booking details
4. View the generated email response

## Example Workflow

```python
from google import genai
from getpass import getpass

api_key = getpass("Enter your Gemini API key: ")
client = genai.Client(api_key=api_key)

email_text = input("Enter your email: ")

prompt = f"""
Improve the following email.

Instructions:
- Correct grammar and spelling
- Make it professional and clear
- Keep the original meaning
- Return only the improved email

Email:
{email_text}
"""

response = client.models.generate_content(
    model="gemini-3.6-flash",
    contents=prompt
)

print(response.text)
```

## Project Structure

```text
Ashka-Email-APP/
├── Email_Appipynb.ipynb
├── README.md
└── readme
```

## Use Cases

- student and professional email polishing
- business communication drafting
- leave approval requests
- hotel reservation response templates
- brand promotional messaging

## Future Enhancements

- add a user-friendly web interface
- support multiple languages
- create email templates for HR, sales, support, and marketing
- save generated emails to text or PDF format
- support tone selection (formal, friendly, persuasive, executive)

## License

This project is currently shared as a learning and demonstration project. Please check the repository for licensing details or update it based on your intended usage.

## Contributing

Contributions are welcome. If you want to improve the notebook, add more email templates, or enhance the prompt logic, feel free to submit a pull request.

---

<p align="center">
  <b>Ashka Email App</b><br>
  AI-powered email generation for better communication.
</p>
