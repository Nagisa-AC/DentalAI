# DentalAI

## Project Overview
DentalAI is an AI-powered voice assistant for dental offices. It answers phone calls, books appointments, and triages emergencies using GPT-driven dialogue and realistic text-to-speech.

## System Architecture
- **FastAPI backend** handles webhooks and business logic.
- **Twilio** manages phone numbers and call routing.
- **OpenAI GPT-4** classifies intent and extracts data.
- **ElevenLabs** provides natural-sounding voice replies.
- **Tenant configuration** allows multiple offices to customize flows.
- **Call logging** stores transcripts and captured information.

## Setup Instructions
1. Create a Python virtual environment.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the development server:
   ```bash
   uvicorn src.main:app --reload
   ```
   During development, you can expose the local server to Twilio using ngrok.

## Usage Example
With the server running, visit `http://localhost:8000/health` to check the service status. Twilio webhooks will be added to handle incoming calls and drive the conversation flow.

## Future Work
This project will grow to include Twilio webhooks, GPT-powered dialogue management, ElevenLabs TTS, and multi-tenant support.

