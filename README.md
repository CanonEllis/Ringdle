# Ringdle

A Wordle-style game for guessing Apple ringtones. Listen to the ringtone and guess its name in 6 attempts!

## Features

- 🎧 Audio playback with animated waveform visualization
- 🔤 Autocomplete suggestions as you type
- 📊 Statistics tracking (games played, win rate, streak)
- 📋 Share your results with friends
- 💾 Progress saved locally
- 📱 Fully responsive design

## Setup for GitHub Pages

### 1. Create the audio folder

Create an `audio/` folder in your repository with the ringtone files.

### 2. Add your ringtone files

The game expects `.m4a` files with these exact names (lowercase, underscores for spaces):

```
audio/
├── apex.m4a
├── beacon.m4a
├── bulletin.m4a
├── by_the_seaside.m4a
├── chimes.m4a
├── circuit.m4a
├── constellation.m4a
├── cosmic.m4a
├── crystals.m4a
├── duck.m4a
├── hillside.m4a
├── illuminate.m4a
├── marimba.m4a
├── night_owl.m4a
├── opening.m4a
├── playtime.m4a
├── presto.m4a
├── radar.m4a
├── radiate.m4a
├── reflection.m4a
├── ripples.m4a
├── sencha.m4a
├── signal.m4a
├── silk.m4a
├── slow_rise.m4a
├── stargaze.m4a
├── summit.m4a
├── twinkle.m4a
├── uplift.m4a
├── waves.m4a
└── xylophone.m4a
```

### 3. Where to find ringtones

On a Mac, Apple ringtones are located at:
```
/System/Library/PrivateFrameworks/ToneLibrary.framework/Versions/A/Resources/Ringtones/
```

On an iPhone, you can use various apps to extract them, or find them in an iTunes/Finder backup.

**Note:** Apple ringtones are copyrighted. This game is intended for personal use only.

### 4. Deploy to GitHub Pages

1. Create a new repository on GitHub
2. Push this project to the repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/ringdle.git
   git push -u origin main
   ```
3. Go to Settings → Pages
4. Set Source to "Deploy from a branch"
5. Select "main" branch and "/ (root)" folder
6. Click Save

Your game will be live at `https://YOUR_USERNAME.github.io/ringdle/`

## Customization

### Adding/Removing Ringtones

Edit the `RINGTONES` array in `index.html`:

```javascript
const RINGTONES = [
    "Apex",
    "Beacon",
    // ... add or remove as needed
];
```

### Using Different Audio Formats

The game defaults to `.m4a` files. To use `.mp3` or other formats, change this line:

```javascript
audioPlayer.src = `audio/${audioFile}.m4a`;
```

to:

```javascript
audioPlayer.src = `audio/${audioFile}.mp3`;
```

## How to Play

1. 🔊 Click the play button to hear the ringtone
2. ⌨️ Type your guess in the input field
3. 📝 Select from the autocomplete suggestions
4. ✅ Click "Guess" to submit
5. ⏭️ Use "Skip" if you're stuck (uses an attempt)
6. 🎯 Get it right in 6 attempts to win!

## Tech Stack

- Vanilla HTML/CSS/JavaScript
- No external dependencies
- LocalStorage for stats persistence
- Works offline once loaded

## License

This project is for personal/educational use. Apple ringtones are property of Apple Inc.
