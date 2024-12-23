# Voice-to-Voice Translator

## Overview
The **Voice-to-Voice Translator** is a Python application that records audio in English, transcribes it, translates the text into multiple languages, and generates audio outputs in those languages. The project utilizes the following libraries and APIs:

- **Gradio** for the user interface.
- **AssemblyAI** for audio transcription.
- **ElevenLabs** for text-to-speech synthesis.
- **translate** library for text translation.
- Standard Python libraries: `os`, `uuid`, `pathlib`, and `numpy`.

## Features
1. **Audio Recording**: Record your voice in English directly through the application.
2. **Speech-to-Text**: Convert the recorded audio to text using AssemblyAI.
3. **Text Translation**: Translate the English text into six languages:
   - Russian
   - Turkish
   - Swedish
   - German
   - Spanish
   - Japanese
4. **Text-to-Speech**: Generate translated audio outputs using ElevenLabs.
5. **Interactive UI**: Built with Gradio for an intuitive and interactive experience.

## Installation

### Prerequisites
- Python 3.8 or higher
- Install the required libraries:

```bash
pip install numpy gradio assemblyai translate elevenlabs
```

### API Keys
Obtain API keys for the following services:
- **AssemblyAI**: [Get your API key here](https://www.assemblyai.com/).
- **ElevenLabs**: [Sign up for an API key here](https://elevenlabs.io/).

Add your API keys in the script:
```python
aai.settings.api_key = "YOUR_ASSEMBLYAI_API_KEY"
client = ElevenLabs(api_key="YOUR_ELEVENLABS_API_KEY")
```

## Usage

1. Run the script:
   ```bash
   python <script_name>.py
   ```

2. Open the Gradio interface in your browser.
3. Record your voice in English using the provided microphone input.
4. Click **Submit** to:
   - Transcribe the audio.
   - Translate the text into six languages.
   - Generate audio outputs in the respective languages.
5. Download the translated audio files if needed.

## Project Structure
- **Main Script**: Contains the primary logic for the application.
- **Functions**:
  - `transcribe_audio(audio_file)`: Transcribes audio using AssemblyAI.
  - `translate_text(text)`: Translates text into multiple languages.
  - `text_to_speech(text)`: Converts translated text into audio using ElevenLabs.

## Notes
- Ensure your ElevenLabs account has sufficient credits for text-to-speech generation.
- The application is designed for multilingual audio processing; it supports additional languages if configured.

## Future Enhancements
- Add support for more languages.
- Implement error handling for API limits and network issues.
- Optimize audio processing for real-time translation.

## License
This project is licensed under the MIT License.

## Acknowledgements
- AssemblyAI for transcription services.
- ElevenLabs for advanced text-to-speech capabilities.
- Gradio for creating an intuitive user interface.

