# Audio2Text

# Audio Transcription App

This repository contains a Python-based web application for transcribing audio files into text using OpenAI's Whisper model and Gradio. The app provides a user-friendly interface for uploading audio files and receiving the transcribed text.

## Features

- **Speech Recognition**: Utilizes OpenAI's Whisper-tiny.en model for automatic speech recognition.
- **Batch Processing**: Processes audio files in chunks for efficient transcription.
- **Gradio Interface**: Provides an interactive web-based UI for uploading audio and viewing transcription results.

## Requirements

To run this application, you need the following dependencies:

- `torch`
- `transformers`
- `gradio`

Install them using pip:

```bash
pip install torch transformers gradio
```

## Usage

1. Clone the repository:

```bash
git clone https://github.com/mohammad5994/Audio2Text.git
cd audio-transcription-app
```

2. Run the script:

```bash
python audio_summarizer.py
```

3. Open the web application:

   - The application will launch on `http://127.0.0.1:7860` by default.

4. Upload an audio file:

   - Drag and drop or upload an audio file through the interface.
   - View the transcription result in the text box.

## How It Works

1. **Model Initialization**:

   - The application initializes a Hugging Face pipeline for automatic speech recognition using the `openai/whisper-tiny.en` model.

2. **Audio Processing**:

   - The uploaded audio file is segmented into 30-second chunks for efficient transcription.
   - The model processes these chunks and returns the transcribed text.

3. **Gradio Interface**:

   - The Gradio library creates an interactive interface for uploading audio files and displaying transcriptions.

## Example

1. Upload an audio file containing a spoken sentence.
2. The application will display the transcribed text, e.g.:

```
Transcribed Text: "Hello, how can I help you today?"
```

## Customization

- **Model Choice**:

  - Replace `"openai/whisper-tiny.en"` with a different Whisper model for varying accuracy and performance.

- **Chunk Size**:

  - Adjust `chunk_length_s=30` to process longer or shorter audio segments at a time.

- **Interface Design**:

  - Modify `title` and `description` in the Gradio interface to suit your application's theme.

## Limitations

- The transcription quality depends on the audio clarity and the selected model.
- Processing time may increase for longer audio files or on less powerful hardware.

## Acknowledgments

- [Hugging Face Transformers](https://huggingface.co/docs/transformers/index) for the Whisper model.
- [Gradio](https://gradio.app/) for the interactive interface.
- OpenAI for the Whisper model.

## License

This project is licensed under the Apache2.0 License. See the `LICENSE` file for details.

