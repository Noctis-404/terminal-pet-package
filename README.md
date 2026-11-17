# Terminal Pet A

**A friendly cat companion for your terminal.**

## What it does
Terminal Pet A is a command-line companion that lives right in your terminal. It allows developers to interact with a virtual pet (checking stats, feeding, and playing) while also providing built-in productivity utilities like a Pomodoro-style reminder system, a browser launcher, and motivational quotes.

## Why it is useful
It improves developer productivity by acting as a quick launcher for web tools and providing motivational mental breaks during long coding sessions without forcing you to leave your command-line environment. 

## Installation
To install this package globally on your machine, run the following command in your terminal:
`npm install -g terminal-pet-a`

## Basic usage
Once installed globally, you can interact with your pet from anywhere in your terminal by typing the command `mypet` followed by an action.

### Example
`mypet status`
`mypet remind 5m "Check the server logs"`

## API / Method Documentation

### Core Commands (No parameters)
- `mypet help`: Shows all available commands.
- `mypet status`: Displays your pet's current mood, hunger, and energy levels.
- `mypet feed`: Gives your pet a snack (increases hunger stats).
- `mypet play`: Plays a quick catch game (increases mood, uses energy).
- `mypet sleep`: Lets your pet rest and restore energy.
- `mypet speak`: Prints a motivational developer quote.
- `mypet work`: Uses the system's `child_process` to open Google Chrome.

### Commands with Parameters
- `mypet remind <duration> <text>`
  - **Parameters:** `duration` (String: "10s", "5m", "2h"), `text` (String: your reminder message).
  - **Return value:** Triggers a delayed console output after the specified time.
- `mypet message <text>`
  - **Parameters:** `text` (String: the message to echo).
  - **Return value:** Prints the text back to the terminal.
- `mypet open <site>`
  - **Parameters:** `site` (String: URL or known site name).
  - **Return value:** Launches the default browser to the specified site.

## Limitations
The `work` and `open` commands rely on the host operating system's default browser routing and may behave differently depending on whether you are running macOS, Windows, or a headless Linux server.

## License
MIT