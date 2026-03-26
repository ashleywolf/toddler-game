# Jump & Play! 🦘

A camera-based action game for toddlers. No install, no app store -- just open in a browser.

**[Play now](https://ashleywolf.github.io/toddler-game/)**

## How it works

The game uses your device's camera and asks your toddler to do things:

- **Smile** -- detected via face mesh landmarks
- **Jump** -- detected via pose tracking (shoulder/nose position)
- **Hold up fingers** (1-5) -- detected via hand landmark tracking
- **Name shapes** -- detected via speech recognition (say "circle", "star", etc.)

Every response gets confetti and a celebration. There are no wrong answers and no failure states. If the toddler doesn't respond within 15 seconds, the game gently moves on.

## Difficulty levels

Rounds 1-3 ask for smiles and jumps only. Fingers get introduced at round 4, shapes at round 7, and the full mix at round 10.

## Tech

Single HTML file. No build step, no dependencies to install.

- [MediaPipe Vision](https://developers.google.com/mediapipe) (loaded from CDN) for face, hand, and pose detection
- [Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API) for voice prompts and speech recognition
- Web Audio API for sound effects

## Tips

- Works best on Chrome or Edge (speech recognition requires these)
- Prop a phone or tablet where the kid can see themselves on screen -- they love that
- Make sure the full body is visible for jump detection
- The mute button (bottom right) silences voice prompts and sounds
- The restart button resets to round 1

## Running locally

```
open index.html
```

That's it. Or use any local server (`python3 -m http.server`, etc.) if your browser blocks camera on `file://` URLs.
