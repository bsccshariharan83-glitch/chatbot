# Basic Chatbot

A simple rule-based chatbot written in Python. It reads what you type, matches it against predefined phrases, and replies with a fixed response.

## Features

- Responds to greetings, questions, and goodbyes
- Case-insensitive input ("Hello", "HELLO", and "hello" all work)
- Ignores extra spaces around the message
- Fallback reply for anything it doesn't understand
- Exits cleanly when you say "bye"

## Requirements

- Python 3.6 or higher
- No external libraries needed

## Installation

1. Clone or download this repository:

   ```bash
   git clone https://github.com/your-username/basic-chatbot.git
   cd basic-chatbot
   ```

2. There is nothing else to install.

## Usage

Run the chatbot:

```bash
python chatbot.py
```

Type a message and press Enter. Type `bye` to exit.

### Supported Inputs

| You type        | Chatbot replies                          |
|-----------------|------------------------------------------|
| `hello` / `hi`  | Hi!                                      |
| `how are you`   | I'm fine, thanks!                        |
| `your name`     | I'm a simple chatbot.                    |
| `help`          | Try saying: hello, how are you, or bye.  |
| `bye`           | Goodbye!                                 |
| anything else   | Sorry, I didn't understand that.         |

### Example

```
Chatbot: Hello! Type 'bye' to exit.
You: hello
Chatbot: Hi!
You: how are you
Chatbot: I'm fine, thanks!
You: what's the weather
Chatbot: Sorry, I didn't understand that.
You: bye
Chatbot: Goodbye!
```

## Project Structure

```
basic-chatbot/
├── chatbot.py    # Main program
└── README.md     # This file
```

## Key Concepts Used

- **if-elif:** `get_reply()` checks the message against known phrases.
- **Functions:** `get_reply()` holds the reply logic and `main()` runs the chat.
- **Loops:** a `while True` loop keeps the conversation going until the user says "bye".
- **Input/output:** `input()` reads the message and `print()` shows the reply.

## Customization

To teach the chatbot a new phrase, add another `elif` branch in `get_reply()`:

```python
elif "thank" in message:
    return "You're welcome!"
```

## Future Improvements

- Store replies in a dictionary instead of long if-elif chains
- Add more topics (weather, jokes, time)
- Remember the user's name during the chat
- Add a simple GUI

## License

This project is licensed under the MIT License.
