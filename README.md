# Codenames - Multiplayer Browser Game

A fully-featured, real-time multiplayer implementation of the popular word game Codenames using Node.js, Express, and Socket.io.

## Features

- ✅ Real-time multiplayer gameplay
- ✅ Team-based play (Red vs Blue)
- ✅ Spymaster and Operative roles
- ✅ Live lobby system
- ✅ 5x5 word grid with 25 words
- ✅ Scoring system
- ✅ Turn-based gameplay
- ✅ Win/lose conditions
- ✅ Responsive design
- ✅ New game functionality

## How to Run

### Prerequisites
- Node.js (version 12 or higher)
- npm (comes with Node.js)

### Installation

1. Navigate to the game directory:
```bash
cd codenames-multiplayer
```

2. Install dependencies:
```bash
npm install
```

3. Start the server:
```bash
npm start
```

4. Open your browser and go to:
```
http://localhost:3000
```

5. To play with multiple people, each person should open `http://localhost:3000` in their browser

**Note:** If you want others on the same network to join, they can use your local IP address:
```
http://YOUR_LOCAL_IP:3000
```

## How to Play

### Setup
1. Enter your name when you first join
2. Choose Red or Blue team
3. One player from each team should click "Become Spymaster"
4. When ready, click "Start Game"

### Gameplay

**Spymasters:**
- Can see all word colors on the board
- Give one-word clues followed by a number
- The number indicates how many words relate to your clue
- Try to help your team guess your words while avoiding the other team's words and the assassin!

**Operatives:**
- Click on words to guess them based on your spymaster's clue
- You get (clue number + 1) guesses per turn
- Your turn ends if you:
  - Guess a word from the other team
  - Guess a neutral word
  - Use all your guesses
  - Click "End Turn"

### Winning
- **Red team** needs to find all 9 red words
- **Blue team** needs to find all 8 blue words
- **Instant loss** if you click the black assassin word!

## Game Rules

- Red team always goes first and has 9 words
- Blue team has 8 words
- There are 7 neutral words
- There is 1 assassin word (instant loss if selected)
- Spymasters cannot click on words - only operatives can guess
- Teams alternate turns
- You can end your turn early by clicking "End Turn"
- Click "New Game" to start a fresh game with the same teams

## Technical Details

- **Backend:** Node.js with Express
- **Real-time Communication:** Socket.io
- **Frontend:** Vanilla HTML/CSS/JavaScript
- **Port:** 3000 (configurable via PORT environment variable)

## File Structure

```
├── server.js       # Node.js backend server
├── index.html      # Frontend game interface
├── package.json    # Dependencies and scripts
└── README.md       # This file
```

## Customization

### Change Port
Set the PORT environment variable:
```bash
PORT=8080 npm start
```

### Word Bank
Edit the `WORD_BANK` array in `server.js` to add or change words.

## Troubleshooting

**Players can't connect:**
- Make sure the server is running (`npm start`)
- Check that you're using the correct URL
- Ensure port 3000 is not blocked by firewall

**Game not updating:**
- Refresh the browser
- Check browser console for errors (F12)

**Words not appearing:**
- Make sure "Start Game" was clicked
- Ensure both teams have at least one player

## Credits

Based on the popular board game Codenames by Vlaada Chvátil.

Enjoy playing! 🕵️
