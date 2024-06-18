# PokerGPTForGG - GPT4 poker bot for GGPoker

PokerGPTForGGG is a fork of [PokerGPT](https://github.com/HarperJonesGPT/PokerGPT), supporting Only GGPoker.

## Prerequisites

-   Python 3.8 or higher
-   Access to OpenAI GPT-4 API
-   Tesseract OCR for text recognition
-   Pokerstars client

## Installation

1. Clone the repository to your local machine.
2. Install the required Python dependencies by running `pip install -r requirements.txt`.
3. Set up your OpenAI API key in the `.env` file. (register free account at https://openai.com/ and get your API key here: https://platform.openai.com/api-keys)
4. Make sure Tesseract OCR is installed and its path is correctly set in the scripts(Tesseract is included and path set).

## GGPoker client (Visual) setup:

1. Since this bot reads all of the data from the poker client window, you will need to setup the visuals excactly like in this image:
2. Disable all animations for Pokerstars client in the table settings.
   ![GGPokerView](https://github.com/Kotakageyama/PokerGPTForGG/assets/27982108/b3e803e8-63b2-4917-8334-34a5aca6002b)


## Usage

To start the PokerGPTForGG, follow these steps:

1. Open Pokerstars client and ensure it's visible on the screen.
2. Run `main.py` to initiate the bot: `python main.py`.
3. Enter your own player number (player numbers start from the bottom of the table and goes clockwise 1(bottom), 2(bottom-left), 3(top-eft), 4(top), 5(top-right), 6(bottom-right))
4. The bot will automatically locate the poker window and start playing based on the GPT-4 strategy analysis.

## Structure

-   `audio_player.py`: Handles audio feedback from the bot.
-   `game_state.py`: Manages the current state of the game.
-   `gui.py`: Provides a graphical user interface for monitoring the bot's actions.
-   `hero_action.py`: Contains logic for determining the hero's actions.
-   `hero_hand_range.py`: Assesses hand ranges for the hero.
-   `hero_info.py`: Collects information about the hero's current state.
-   `main.py`: Entry point for running the bot.
-   `poker_assistant.py`: Interfaces with OpenAI's API to analyze the game state and decide on actions.
-   `read_poker_table.py`: Uses OCR and pixel detection to read the table state.

## Limitations

-   Dependant on the Pokerstars client window size (PokerGPTForGG automatically resizes to small window)
-   Might not work on all screen resolutions
-   Works only in Pokerstars 6-Player table.
-   Image reading(OCR) speed is dependant on your CPU.

## License

This project is licensed under the MIT License - see the `LICENSE.md` file for details.
