```
  _      _  _     _                   _         _        ____        _       
 | |    | || |   | |                 / \  _   _| |_ ___ | __ )  ___ | |_ ___ 
 | |    | || |_  | |      ______    / _ \| | | | __/ _ \|  _ \ / _ \| __/ __|
 | |___ |__   _| | |___  |______|  / ___ \ |_| | || (_) | |_) | (_) | |_\__ \
 |_____|   |_|   |_____|          /_/   \_\__,_|\__\___/|____/ \___/ \__|___/
                                                          
```

# L4L-AutoBot 🤖

A robust, stealthy, and fully automated Python bot for **Like4Like.org**. Built with Selenium and Python, designed to handle YouTube, Instagram, and Twitter interactions with human-like behavior to avoid detection.

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Selenium](https://img.shields.io/badge/Selenium-Firefox-orange?style=for-the-badge&logo=selenium)

## ✨ Key Features

* **Multi-Platform Support:**
    * 📺 **YouTube:** Smart "Watch & Like" logic (waits for video buffer).
    * 📸 **Instagram:**
        * **Smart Filtering:** Distinguishes between Main Post Likes vs. Comment Likes (size detection).
        * **Reels Support:** Uses Native OS Double-Click to prevent pausing videos.
    * 🐦 **Twitter (X):** Auto-Favorite handling.
* **🛡️ Anti-Detection System:**
    * **Randomized Delays:** Human-like sleep intervals between actions.
    * **Native Interactions:** Uses specific browser events instead of generic clicks.
* **🍪 Smart Session Management:**
    * Auto-saves cookies locally (`session_cookies.json`) to prevent frequent logins.
    * Auto-recovers session if logged out.
* **⚙️ Resilience:**
    * **Retry Logic:** Automatically refreshes and retries if tasks are missing (up to 5 attempts).
    * **Target Limit:** Stops automatically after reaching a specific number of likes (e.g., 100 likes).
    * **Emergency Stop:** Press `Esc` key at any time to safely terminate the bot.

## 📋 Requirements

* **Python 3.x**
* **Mozilla Firefox** (Latest version recommended)
* **GeckoDriver** (Must be in your system PATH)

## 🚀 Installation

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/logoro17/L4L-AutoBot.git]
    cd L4L-AutoBot
    ```

2.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

## ⚙️ Configuration

1.  **Run the script once** to generate the configuration file:
    ```bash
    python main.py
    
    ```
    *The script will create a `profiles.json` file and exit because it needs configuration.*

2.  **Edit `profiles.json`**:
    Open the generated `profiles.json` and paste your Firefox Profile path.

    **How to find your Firefox Profile Path:**
    * Open Firefox.
    * Type `about:profiles` in the address bar and press Enter.
    * Look for the **Root Directory** of your default profile.
    * Copy that path and paste it into `profiles.json`.

    *Example `profiles.json`:*
    ```json
    {
        "active_index": 0,
        "accounts": [
            {
                "name": "My Primary Profile",
                "path": "/home/yourname/.mozilla/firefox/abcd1234.default-release"
            }
        ]
    }
    ```

## 🎮 Usage

Run the main script:

```bash
python main.py

```
Select Platform: Choose between YouTube, Twitter, or Instagram.

    Select Mode:
        [1] Normal: Dashboard view with progress bar.
        [2] Debug: Detailed logs for troubleshooting.

Set Target		: Input how many likes/points you want to earn (Default: 100).
Login			: If it's your first time, the browser will open. Log in to Like4Like manually. The bot will save your cookies for next time.
To Stop the Bot	: Press the Esc key on your keyboard.**
    
## ⚠️ Disclaimer
This tool is for educational purposes only. Automating actions on social media platforms may violate their Terms of Service. The author is not responsible for any consequences resulting from the use of this tool. Use responsibly and do not abuse the system.

## 🤝 Contributing
Feel free to fork this project and submit pull requests. Any improvements to the detection logic or new platform support are welcome!
