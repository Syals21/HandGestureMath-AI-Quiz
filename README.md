# HandGestureMath-AI-Quiz

<div align="center">

## AI Math-Xplorer High Accuracy Edition

**A futuristic touchless math quiz game powered by hand gestures, webcam tracking, and real-time feedback**

<p>
  <img src="https://img.shields.io/badge/HTML5-Single%20File%20App-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5 Badge" />
  <img src="https://img.shields.io/badge/JavaScript-Interactive%20Logic-F7DF1E?style=for-the-badge&logo=javascript&logoColor=111111" alt="JavaScript Badge" />
  <img src="https://img.shields.io/badge/MediaPipe-Hand%20Landmarker-0097A7?style=for-the-badge&logo=google&logoColor=white" alt="MediaPipe Badge" />
  <img src="https://img.shields.io/badge/Webcam-Gesture%20Input-2563EB?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Webcam Badge" />
</p>

<p>
  <img src="https://img.shields.io/badge/Web%20Speech-Bahasa%20Melayu-10B981?style=flat-square" alt="Speech Badge" />
  <img src="https://img.shields.io/badge/Web%20Audio-Realtime%20Feedback-F59E0B?style=flat-square" alt="Audio Badge" />
  <img src="https://img.shields.io/badge/Confetti-Celebration%20Effects-EC4899?style=flat-square" alt="Confetti Badge" />
  <img src="https://img.shields.io/badge/Questions-29%20Math%20Challenges-8B5CF6?style=flat-square" alt="Questions Badge" />
  <img src="https://img.shields.io/badge/GitHub%20Pages-Live%20Deployment-171515?style=flat-square&logo=github&logoColor=white" alt="GitHub Pages Badge" />
</p>

</div>

---

## Preview

Try the live demo: [https://syals21.github.io/HandGestureMath-AI-Quiz/](https://syals21.github.io/HandGestureMath-AI-Quiz/)

---

## Overview

**HandGestureMath-AI-Quiz** is an interactive browser-based quiz game that turns math practice into an immersive AI-powered experience. Instead of clicking an answer, players raise `1` to `4` fingers in front of the webcam to choose an option. The game then confirms the answer through a short hold gesture, giving instant visual, audio, and progress feedback.

Built inside a single-page file, [index.html](/c:/GitHub/HandGestureMath-AI-Quiz/index.html), the project combines mathematics learning, computer vision, and cinematic UI design into a classroom-friendly game that feels playful, modern, and memorable.

## Why It Feels Different

> This is not just a quiz on a screen.  
> It is a touchless learning experience where students move, answer, listen, retry, and celebrate.

- `Touchless gameplay` replaces mouse clicks with hand gestures.
- `Real-time detection` makes the camera part of the learning loop.
- `Retry-first design` encourages thinking instead of revealing answers too early.
- `Sci-fi presentation` makes a school activity feel like an AI mission.
- `Student-friendly feedback` keeps the experience motivating and easy to follow.

---

## Key Highlights

### ✨ Interactive Experience

- Raise `1`, `2`, `3`, or `4` fingers to choose an answer.
- Hold the gesture briefly to confirm and avoid accidental selection.
- Hear the question spoken aloud using Bahasa Melayu voice support.
- Receive immediate response through glowing UI states, sound, and celebration effects.

### 🧠 Educational Flow

- Starts with easier arithmetic questions and progresses into combined operations.
- Encourages repeated attempts through the `Cuba Semula` retry flow.
- Does not instantly reveal the correct answer after a mistake.
- Rewards correct answers with score progression and visual encouragement.

### 🚀 Technical Strength

- Uses **MediaPipe Hand Landmarker** from `@mediapipe/tasks-vision` for live hand landmark tracking.
- Loads the vision bundle and hosted model asset dynamically for browser deployment.
- Falls back from `GPU` to `CPU` delegate for better device compatibility.
- Uses **Web Speech API** for spoken question delivery.
- Uses **Web Audio API** for win and lose tones.
- Uses **canvas-confetti** for success animations.
- Runs as a lightweight browser project with no large framework required.

---

## Gameplay Flow

### 🎮 How Players Interact

1. Open the game and allow webcam access.
2. Start the mission from the intro screen.
3. Read or listen to the current math question.
4. Match your answer by showing `1` to `4` fingers.
5. Hold the gesture until the answer is confirmed.
6. Move to the next question after a correct response.
7. Retry the same question if the answer is wrong.

### 🪄 What Happens Behind The Scenes

- The webcam feed is processed in real time.
- The browser starts the camera using native `getUserMedia`.
- Hand landmarks are analyzed to estimate how many fingers are raised.
- Detection runs frame-by-frame through `detectForVideo()` for live recognition.
- Only gestures from `1` to `4` are accepted as answer inputs.
- A confirmation threshold of `REQUIRED_FRAMES = 24` helps reduce false triggers.
- The score increases by `10` for each newly completed correct answer.

---

## Feature Breakdown

### ⚡ Smart Answer System

- Multiple-choice answer cards are mapped directly to finger counts.
- A progress bar fills while the gesture is being held.
- Correct answers auto-advance after feedback is shown.
- A protection set prevents duplicate scoring on repeated correct attempts.
- Startup errors are surfaced on screen so tracking failures are easier to diagnose.

### 🔊 Feedback System

- Spoken question playback supports younger learners and classroom use.
- Winning and losing tones create immediate emotional feedback.
- Confetti and theme changes reinforce success moments.

### 🛰️ Visual Style

- Futuristic blue and cyan color palette
- Glassmorphism panels
- Animated background atmosphere
- Neon-style score and progress indicators
- Mission-themed language and presentation

---

## Tech Stack

### 🧪 Core Technologies

- **HTML5** for structure
- **CSS3** for styling and animation
- **JavaScript** for game logic and interaction

### 🤖 AI and Browser APIs

- **MediaPipe Hand Landmarker** from `@mediapipe/tasks-vision`
- **FilesetResolver** for loading MediaPipe vision assets
- **getUserMedia** for webcam access
- **Web Speech API** for voice playback
- **Web Audio API** for sound effects
- **canvas-confetti** for celebration visuals

---

## Project Snapshot

| Category | Details |
|---|---|
| Main file | [index.html](/c:/GitHub/HandGestureMath-AI-Quiz/index.html) |
| Live site | `https://syals21.github.io/HandGestureMath-AI-Quiz/` |
| Quiz type | Touchless webcam-based math quiz |
| Input method | Hand gestures using `1-4` fingers |
| Total questions | `29` |
| Scoring | `10 points` per correct answer |
| Confirmation system | Hold gesture for `24` frames |
| Voice language | `ms-MY` |
| Tracking engine | `HandLandmarker` with `GPU -> CPU` fallback |

---

## Project Structure

```text
HandGestureMath-AI-Quiz/
|- index.html
`- README.md
```

---

## Run Locally

### 🛠️ Recommended

Run the project from a local server so webcam permissions work more reliably.

### Quick options

1. Open the project folder in your editor.
2. Start a local server.
3. Launch `index.html` in the browser.
4. Allow camera access when prompted.

If the browser blocks webcam access, avoid opening the file directly with `file:///` and use a local server instead.

---

## Deployment

### 🌐 GitHub Pages

Live version: `https://syals21.github.io/HandGestureMath-AI-Quiz/`

- The project is compatible with GitHub Pages hosting.
- The hand-tracking system now uses the newer MediaPipe Tasks Vision setup.
- The model is loaded from a hosted MediaPipe asset, which makes browser deployment more reliable than the older legacy loader.

---

## What Makes This Project Special

**HandGestureMath-AI-Quiz** blends education and AI interaction in a way that feels immediate and exciting. It shows how computer vision can be used beyond technical demos to create meaningful learning experiences for students. The project is simple in structure, but rich in interaction, making it a strong showcase of creativity, usability, and applied AI in education.

---

## Future Ideas

- Add difficulty levels or timed challenge mode
- Show performance analytics at the end of the quiz
- Expand the question bank into more math topics
- Add multilingual voice support
- Store scores for classroom competitions

---

<div align="center">

### 🌌 Learn Math. Move Naturally. Play Like The Future.

</div>
