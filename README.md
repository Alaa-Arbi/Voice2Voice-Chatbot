# Voice2Voice-Chatbot

In this repository, I experiment with the Nova Sonic model from AWS to create a Voice-to-Voice chatbot.

## Overview
The `voice_chatbot.py` script is a sophisticated implementation of a voice-to-voice chatbot that integrates with AWS Bedrock's Nova Sonic model. It captures audio from the microphone, processes it, and interacts with the Nova Sonic model to generate responses. The chatbot also supports real-time audio playback and session management.

## Features
- **AWS Bedrock Integration**: Utilizes the Nova Sonic model for voice-to-voice interactions.
- **Audio Capture**: Captures audio from the microphone in real-time.
- **Audio Processing**: Sends audio data to the Nova Sonic model for processing and response generation.
- **Real-Time Playback**: Plays audio responses from the Nova Sonic model in real-time.
- **Session Management**: Handles session initialization, audio input/output, and session termination.
- **Customizable Prompts**: Allows customization of system and user prompts for tailored interactions.

## How It Works
1. **Initialization**: The `VoiceChatbot` class initializes the AWS Bedrock client and sets up the audio processing pipeline.
2. **Session Start**: The `start_session` method sends session and prompt initialization events to the Nova Sonic model.
3. **Audio Capture**: The `capture_audio` method reads audio data from the microphone and sends it to the Nova Sonic model.
4. **Response Processing**: The `_process_responses` method processes text and audio responses from the Nova Sonic model.
5. **Audio Playback**: The `play_audio` method plays audio responses in real-time.
6. **Session End**: The `end_session` method terminates the session and closes the audio stream.

## Requirements
- Python 3.8+
- Libraries:
  - `pyaudio`
  - `aws-sdk-bedrock-runtime`
  - `smithy-aws-core`

## Usage
1. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
2. Set up AWS credentials in your environment.
3. Run the script:
   ```bash
   python voice_chatbot.py
   ```
4. Speak into the microphone to interact with the chatbot. The chatbot will process your input and play the response in real-time.

## Notes
- Ensure that your AWS credentials are correctly configured in your environment.
- Modify the `VoiceChatbot` class to customize prompts and audio configurations.

## Future Improvements
- Enhance error handling and logging.
- Add support for multi-channel audio processing.
- Integrate additional AWS Bedrock models for expanded functionality.
