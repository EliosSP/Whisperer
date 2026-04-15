# Whisperer

An automated tool for local audio transcription and intelligent text formatting, designed for students, researchers, and design professionals.

## Project Vision
MagicTranscript was born from the need to transform raw audio recordings (lectures, user interviews, workshops) into clean, organized, and ready-to-use text documents without losing the fidelity of the original content. 

The tool combines the power of local transcription via **OpenAI Whisper** with the editing intelligence of **Google Gemini AI**.

## Technical Architecture
The system operates as a background "Folder Watcher":
1. **Input:** The user drops an audio file into the `To_Transcribe` folder.
2. **Transcription (Local):** The Whisper `medium` model processes the audio directly on the device (ensuring complete data privacy for the audio).
3. **Refining (Cloud):** The raw text is sent to Gemini Pro via API to remove fillers, correct grammar, and format the output into clean Markdown.
4. **Output:** The original file is archived, and a structured `.md` document is generated in the `Formatted_Notes` folder.

## Requirements
- **Python 3.9+**
- **FFmpeg** (for audio codec handling)
- **Apple Silicon (M1/M2/M3/M4)** highly recommended for optimal local performance.

## Installation and Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/MagicTranscript.git](https://github.com/your-username/MagicTranscript.git)
   cd MagicTranscript
