# Speech to Text Conversion using OpenAI Whisper and Hugging Face

## Project Overview  
This project converts audio files in MP3 format into text using OpenAI's Whisper model with Hugging Face's Transformers library. It utilizes Python, FFmpeg, and torchaudio to process audio and extract transcriptions efficiently.  

## Technologies Used  
- Python – Main programming language  
- OpenAI Whisper – AI model for speech to text  
- Hugging Face Transformers – Model hub and pre trained Whisper model  
- TorchAudio – Audio processing with PyTorch  
- FFmpeg – Audio conversion and processing  

## Installation and Setup  
To run this project locally follow these steps  

### 1. Clone the Repository  

git clone https://github.com/your-username/stt-whisper.git
cd stt-whisper

## 2. Install Dependencies

pip install transformers torchaudio ffmpeg
3. Download and Install FFmpeg if not installed

For Ubuntu or Linux
sudo apt update && sudo apt install ffmpeg

For Windows
Download FFmpeg from https://ffmpeg.org/download.html
Add it to the system PATH

## 4. Run the Speech to Text Script
Place your MP3 file in the project directory and run
python stt.py

## Project Workflow
Load the Whisper model from Hugging Face
Process the MP3 audio file
Convert speech to text transcription
Save the transcribed text into a file
Allow downloading the output


## Code Explanation
The core script stt.py follows these steps

from transformers import pipeline

# Load Whisper model
pipe = pipeline("automatic-speech-recognition", model="openai/whisper-base")

# Define audio file path
audio_path = "harvard.mp3"

# Convert Speech to Text
transcription = pipe(audio_path)["text"]

# Save transcription to file
with open("transcription.txt", "w") as f:
    f.write(transcription)

print("Transcription saved in 'transcription.txt'")


## Future Improvements
Support for real time speech recognition
Handle different languages and accents
Enhance accuracy in noisy environments
Contributing
Feel free to fork this repository and submit pull requests for improvements














