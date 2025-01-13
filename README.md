
# Discord Bot with Voice Chat and Voice Clips

This project is a **Discord bot** that integrates both **text-based and voice-based interactions**. It supports voice chat, voice clips, and leverages advanced AI models to engage in dynamic conversations with users. The bot uses AI memory to store past conversations and provides relevant context to ongoing chats. It can generate and play back **text-to-speech (TTS)** responses and recognize **user speech**.

## Features:
- **Text and Voice Interactions**: The bot can respond to both text-based and voice-based messages.
- **AI Memory Store**: Remembers past conversations and fetches context to maintain continuity.
- **Voice Synthesis (TTS)**: Converts text responses into speech using **PiperTTS**.
- **Voice Recognition**: Recognizes speech from voice messages and converts it into text.
- **Voice Clips**: Sends voice clips in Discord channels based on bot responses.

---

## Prerequisites

Before setting up the bot, make sure you have the following installed:

- **Python 3.8+** (with the latest `pip` version)
- **Ollama** (running with `ollama run llama3.1:8b` or another supported model)
- **PiperTTS** (for generating TTS responses)

You will also need a **Discord Bot Token** to connect the bot to your server. You can get this from the [Discord Developer Portal](https://discord.com/developers/applications).

---

## Installation Steps

### 1. Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/discord-bot-voice-chat.git
cd discord-bot-voice-chat
```

### 2. Set Up a Virtual Environment

Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scriptsctivate`
```

### 3. Install Dependencies

Install the required Python packages:

```bash
pip install discord.py[voice] sentence-transformers faiss-cpu numpy aiohttp speechrecognition ollama python-dotenv
python -m pip install discord-ext-voice-recv
```

### 4. Set Up Your Discord Bot Token

Paste in Discord Token

```env
DISCORD_BOT_TOKEN=your-discord-bot-token-here
```

### 5. Configure PiperTTS (Optional)

If you are using **PiperTTS**, ensure that the necessary model files are located in the correct directories as specified in the code (`piper/piper.exe` and the model files). You can adjust these paths in the code if needed.

---

## Running the Bot

Once everything is set up, you can start the bot by running the following command:

```bash
python bot.py
```

The bot will log into Discord, join voice channels, listen for voice or text commands, and generate voice clips based on its responses.

---

## Commands

- `!test` - Joins the voice channel and starts listening.
- `!stop` - Disconnects the bot from the voice channel.
- `!die` - Shuts down the bot.

---

## Contributing

Feel free to open issues or submit pull requests if you'd like to contribute to this project!

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
