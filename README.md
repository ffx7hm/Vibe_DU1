# Homework #1: AI Joke Teller ??

This project is a Python-based implementation for the **Vibecoding** course. It demonstrates how to interact with Large Language Models (LLM) using professional development practices like environment variables and direct REST API calls.

## Project Description
The goal of this assignment was to create a script that connects to an AI provider and requests a joke. 

### Why Google Gemini?
While the assignment mentions the OpenAI SDK, this project utilizes **Google Gemini 1.5 Flash** as the backend engine. This decision was made because I maintain an active **Google AI Premium subscription**, providing high reliability and performance within my current developer ecosystem.

### Technical Implementation
- **Direct REST API**: Instead of the standard `openai` library (which had issues with custom headers), this script uses the `requests` library to communicate directly with Google's v1beta endpoint.
- **Header Authentication**: Securely uses `X-goog-api-key` for authentication.
- **Anti-Repetition Logic**: Implements a dynamic "salt" (timestamp) and high `temperature` settings to ensure the AI doesn't tell the same joke twice.
- **Robustness**: Includes timeout handling and static analysis compatibility for automated grading systems.

## Setup Instructions

1. **Install Dependencies**:
   ```bash
   pip install requests python-dotenv