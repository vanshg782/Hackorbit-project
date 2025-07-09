# Hackorbit-project
AI Video Summarizer - Overview
This project automatically transcribes and summarizes the content of video files.
It uses OpenAI Whisper for transcription and Hugging Face transformers (BART Large CNN) for text summarization.
The Streamlit app makes it easy to upload and summarize videos.
Use cases include:
- Content creators needing notes from recordings.
- Researchers summarizing lectures.
- Students reviewing classes.
- Anyone wanting quick insights from videos.
Key Features
1. Extracts audio from video files.
2. Transcribes speech to text with Whisper.
3. Summarizes text using BART Large CNN.
4. Supports chunked summarization for large transcripts.
5. Streamlit web interface for easy use.
Project Structure (Detailed)
Files in the project:
- app.py: Streamlit interface.
- main.py: Main pipeline from video to summary.
- transcriber.py: Extracts and transcribes audio.
- summarizer.py: Summarizes text.
- utils.py: Helper functions for chunking large texts.
Models and Libraries Used:-
Transcription - OpenAI Whisper - base (can change size)
Summarization - Transformers - facebook/bart-large-cnn
Web App - Streamlit
Audio Extract - ffmpeg 
Other - torch, ffmpeg-python
Installation Steps
Clone and enter project folder:
git clone https://github.com/yourusername/video-summarizer.git
cd video-summarizer
Create and activate environment:
python -m venv venv
source venv/bin/activate (Windows: venv\Scripts\activate)
Install dependencies:
pip install -r requirements.txt
Example requirements.txt
streamlit
transformers
whisper
torch
ffmpeg-python
Important Notes
- ffmpeg must be installed and in PATH.
- Large files may take longer to transcribe.
- You can adjust summarizer settings for summary style.
Usage (CLI and Web App)
Run from command line:
python main.py
Make sure to place example_video.mp4 in the folder.
Run the web app:
streamlit run app.py
Then upload a video file and get the summary.
Process Flow
1. Upload video.
2. Extract audio using ffmpeg.
3. Transcribe audio to text using Whisper.
4. Summarize text with BART Large CNN.
5. Display summary
Extra Tips
- Change Whisper model size for better accuracy.
- Try other summarization models from Hugging Face.
- Preprocess text for cleaner summaries.
Example Output
python main.py
Expected output:
=== FINAL SUMMARY ===
<The summary of the video>
License
MIT License
Credits
- OpenAI Whisper
- Hugging Face Transformers
- Streamlit
- ffmpeg

ALL THE CODES ARE VERIFIED BY THE ARTIFICIAL INTELLIGENCE.
