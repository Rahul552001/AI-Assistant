# AI Assistant for Dental Clinic

This repository contains a Python project for creating a virtual AI assistant designed to assist in a dental clinic setting. The assistant is built using AssemblyAI for real-time transcription, Eleven Labs for text-to-speech functionality, and OpenAI's GPT-3.5-turbo model for generating responses.

## Features

- **Real-time Transcription**: Uses AssemblyAI to transcribe spoken language into text.
- **AI Response Generation**: Generates responses using OpenAI's GPT-3.5-turbo model.
- **Text-to-Speech**: Converts AI responses into audio using Eleven Labs.

## Installation

To run this project, you need to have Python installed. Create a virtual environment and install the necessary dependencies with the following commands:

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
pip install assemblyai elevenlabs openai
```

# Configuration
1. API Keys: You need to replace the API keys in the 'AI_Assistant' class with your own. You can get API keys by signing up for the respective services.
```python
aai.settings.api_key = "YOUR_ASSEMBLYAI_API_KEY"
self.openai_client = OpenAI(api_key="YOUR_OPENAI_API_KEY")
self.elevenlabs_api_key = "YOUR_ELEVENLABS_API_KEY"
```

3. Voice Name: Ensure the valid_voice_name in the generate_audio method matches a valid voice name available in Eleven Labs.
```python
   valid_voice_name = "Lily"  # Replace with a valid voice name
```

# Usage
To start the AI assistant, run the bot.py script. This will initialize the AI assistant and begin transcription. You can also generate a greeting message as follows:
```python
greeting = "Thank you for calling Alok Dental Clinic. My name is Garima, how may I assist you?"
ai_assistant = AI_Assistant()
ai_assistant.generate_audio(greeting)
ai_assistant.start_transcription()
```

# Running the Script
Execute the script with:
```python
python bot.py
```

# Troubleshooting
+ Invalid API Key Error: Ensure that your API keys are correctly set and not expired.
+ Audio Generation Issues: Check that the voice name is valid and that you have a proper internet connection.






