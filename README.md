# Speech-to-Text and Summarization for Recorded Phone Calls

This project demonstrates how to transcribe and summarize recorded phone calls using AI. It uses AssemblyAI's speech-to-text API for transcription and Hugging Face's Transformers library for text summarization.

## Project Overview

The project processes a phone call recording and:
1. Transcribes the audio to text using AssemblyAI
2. Summarizes the conversation using a pre-trained transformer model
3. Extracts key information from the call (customer name, phone number, purpose)

## Repository Structure

```
.
├── README.md                        # Project documentation
├── teach_back_mis_769.ipynb        # Main Jupyter notebook
├── Custom-Home-Builder.mp3         # Sample audio file
├── requirements.txt                 # Python dependencies
├── .gitignore                      # Git ignore rules
└── config.example.py               # Example configuration file
```

## Installation

1. Clone this repository
2. Install the required packages:

```bash
pip install -r requirements.txt
```

## Configuration

1. Copy `config.example.py` to `config.py`:
```bash
cp config.example.py config.py
```

2. Add your AssemblyAI API key to `config.py`:
```python
ASSEMBLYAI_API_KEY = "your_api_key_here"
```

**Important:** Never commit your actual API keys to version control.

## Usage

### Using the Jupyter Notebook

1. Open `teach_back_mis_769.ipynb` in Jupyter Notebook or JupyterLab
2. Ensure your AssemblyAI API key is set in `config.py`
3. Update the audio file path if using a different audio file
4. Run all cells to:
   - Transcribe the audio
   - Generate a summary
   - View the results

### Audio File Requirements

- Supported formats: MP3, WAV, M4A, etc.
- Place your audio file in the project root directory
- Update the file path in the notebook accordingly

## Features

- **Audio Transcription**: Converts speech to text using AssemblyAI's advanced speech recognition
- **Text Summarization**: Creates concise summaries using the DistilBART model
- **Call Analysis**: Extracts customer information and call purpose

## Example Output

The notebook provides:
- Full transcript of the phone call
- Summarized version highlighting key points
- Customer contact information and requirements

## Dependencies

- `assemblyai`: Speech-to-text transcription
- `transformers`: Text summarization using pre-trained models
- `torch`: PyTorch backend for transformers

See `requirements.txt` for specific versions.

## Notes

- The summarization model (sshleifer/distilbart-cnn-12-6) is downloaded automatically on first use
- Processing time depends on audio file length
- Transcription requires an active internet connection
- Keep your AssemblyAI API key secure and never commit it to version control

## Security

⚠️ **Important Security Notes:**
- Never commit API keys to git
- Use environment variables or a config file (excluded from git) for sensitive data
- The `.gitignore` file is configured to exclude `config.py`

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contributing

This is an educational project for MIS769. Feel free to fork and experiment with different audio files or summarization models.
