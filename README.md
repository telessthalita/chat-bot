# README


## Prerequisites

- **Python 3.7+**
- **Google Colab** (optional, but facilitates execution)
- **Google Gemini API Key**: A valid API key is required to authenticate and access the Google Gemini models.

## Installation

1. Ensure you have a Google Gemini API key.
2. In Colab, save the API key as `GOOGLE_GEMINI_API_KEY` to be retrieved directly.

To install the library, run:

```python
!pip install -q -U google-generativeai

## Configuration

The API key is loaded using Colab's `userdata` functionality, enabling secure authentication. Here’s how to configure the API key:

```python
from google.colab import userdata

# Load the API key
GOOGLE_GEMINI_API_KEY = userdata.get('GOOGLE_GEMINI_API_KEY')
genai.configure(api_key=GOOGLE_GEMINI_API_KEY)

## Usage

The code performs the following steps:

1. **Listing Available Models**: Lists all models that support content generation, displaying their identifiers.
2. **Initializing the Model**: Selects the model `models/gemini-1.5-pro-latest` for response generation.
3. **Generating Content**: Generates a response to a predefined question ("Who created the Gemini AI models?").
4. **Starting an Interactive Chat**: Initiates a chat session where the user can send messages to the model until the command "exit" is typed.
