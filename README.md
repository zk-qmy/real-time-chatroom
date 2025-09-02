# real-time-chatroom

## Tentative Project Structure
```
chatroom-app/
│
├── client/
│   ├── core/
│   │   ├── ChatClient.py           # Main client logic (connect, send, receive)
│   │   ├── MessageSender.py        # Sends encrypted messages
│   │   ├── MessageReceiver.py      # Runs in QThread, receives messages
│   │   ├── FileTransfer.py         # Handles file sending/receiving
│   │   └── __init__.py
│   │
│   ├── gui/
│   │   ├── ChatWindow.py           # Main PyQt GUI class (QMainWindow)
│   │   ├── EmojiPicker.py          # Emoji selection widget (QDialog)
│   │   ├── FileDialog.py           # QFileDialog wrapper
│   │   └── __init__.py
│   │
│   ├── services/
│   │   ├── EncryptionService.py    # AES/RSA encryption logic
│   │   ├── EmojiService.py         # Maps emoji codes to visuals
│   │   └── __init__.py
│   │
│   ├── utils/
│   │   ├── MessageFormatter.py     # Adds timestamps, formats messages
│   │   ├── ClientLogger.py         # Logging utility
│   │   └── __init__.py
│   │
│   ├── client_main.py              # Entry point for client
│   └── __init__.py
│
├── server/
│   ├── core/
│   │   ├── ChatServer.py           # Accepts connections, manages threads
│   │   ├── ClientHandler.py        # Handles each client connection
│   │   ├── MessageRouter.py        # Routes messages to recipients
│   │   ├── FileTransfer.py         # Server-side file handling
│   │   └── __init__.py
│   │
│   ├── services/
│   │   ├── EncryptionService.py    # Server-side encryption
│   │   ├── UserManager.py          # Tracks connected users
│   │   └── __init__.py
│   │
│   ├── utils/
│   │   ├── ServerLogger.py         # Logging utility
│   │   └── __init__.py
│   │
│   ├── server_main.py              # Entry point for server
│   └── __init__.py
│
├── shared/
│   ├── Protocol.py                 # Message formats, headers, codes
│   ├── Constants.py                # Shared constants (e.g., buffer size)
│   ├── Logger.py                   # Unified logging utility
│   └── __init__.py
│
├── config/
│   ├── settings.py                 # HOST, PORT, TIMEOUT, etc.
│   └── __init__.py
│
├── assets/
│   ├── emojis/                     # Image-based emojis
│   ├── screenshots/                # GUI screenshots for docs
│   └── __init__.py
│
├── tests/
│   ├── test_client.py              # Unit tests for client logic
│   ├── test_server.py              # Unit tests for server logic
│   ├── test_encryption.py          # Tests for encryption
│   ├── test_protocol.py            # Tests for message parsing
│   └── __init__.py
│
├── docs/
│   ├── README.md                   # Setup and usage guide
│   ├── DESIGN.md                   # Architecture decisions
│   ├── CHANGELOG.md                # Version history
│   └── architecture_diagram.png    # System design visual
│
├── requirements.txt                # Python dependencies
└── LICENSE                         # Open source license
```
