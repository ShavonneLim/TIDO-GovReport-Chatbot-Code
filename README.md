# GovReport Chat Application

GovReport is a chat application designed to help citizens easily report issues to the relevant government agencies. It features a web-based chat interface and a seamless integration with a Telegram bot.

## Features

  * **Web Chat Interface**: A clean and intuitive chat interface for users to report issues.
  * **Multimedia Support**: Users can send text, images, and audio recordings through the chat.
  * **AI-Powered Responses**: The bot uses an AI (Large Language Model) to understand user reports and provide relevant information or next steps.
  * **Telegram Integration**: The service is also available as a Telegram chatbot, allowing for easier access and use on the go.
  * **Issue Reporting Lifecycle**: The system is designed to help citizens *Recognise* issues, *Report* them easily, and ensure they are *Resolved* by the correct department.

-----

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

  * Python 3.8+
  * `pip` for package management

### Installation

1.  **Clone the repository**:

    ```bash
    git clone [repository_url]
    cd [repository_name]
    ```

2.  **Create and activate a virtual environment**:

    ```bash
    python -m venv venv

    # On Windows
    .\venv\Scripts\activate

    # On macOS/Linux
    source venv/bin/activate
    ```

3.  **Install the required packages**:

    ```bash
    pip install -r requirements.txt
    ```

4.  **Set up environment variables**:

    Create a `.env` file in the root directory with the following variables:

    ```env
    TELE_API_TOKEN=your_telegram_bot_token
    SYSTEM_PROMPT=your_llm_system_prompt
    IMAGES_DIR=your_images_directory
    ```

    *(You can adjust `IMAGES_DIR` as needed for storing uploads.)*

-----

### Installing Models

The application uses several AI models for different functionalities. You can download and install them using the following commands:

#### Llama 3.2 (Text Generation)

Used for generating text-based responses.

```bash
ollama pull llama3.2
```

#### LLaVA (Multimodal Understanding)

Required for processing images and understanding their content.

```bash
ollama pull llava
```

#### Whisper (Speech-to-Text)

Used to transcribe audio recordings from users.

```bash
ollama pull whisper
```

-----

### Running the Application

Run the application with:

```bash
python app.py
```