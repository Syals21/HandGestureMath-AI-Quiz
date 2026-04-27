# HandGestureMath-AI-Quiz

## Project Overview

**HandGestureMath-AI-Quiz** is an interactive browser-based mathematics game that transforms a traditional multiple-choice quiz into a touchless learning experience. Instead of clicking answers, players respond by raising the correct number of fingers in front of a webcam. The project combines math practice, computer vision, visual storytelling, and instant feedback to create a classroom-friendly game that feels futuristic and engaging.

At the center of the experience is [AI_Math_Game/AI_Math.html](/c:/GitHub/HandGestureMath-AI-Quiz/AI_Math_Game/AI_Math.html), a single-page implementation that blends a cinematic interface with real-time hand gesture recognition. The result is a quiz game where students can solve arithmetic questions, confirm their choices with a short hand hold gesture, and receive immediate visual and audio feedback without touching the screen.

## Core Idea

This project is designed to make mathematics feel active, playful, and immersive. Rather than treating quiz practice as a static worksheet, the game invites learners to:

- read and hear each question
- look at four answer choices
- raise `1`, `2`, `3`, or `4` fingers to match the selected option
- hold the gesture briefly to confirm the answer
- continue learning through retry-based feedback and score progression

The interaction style encourages focus, movement, and participation, which makes the game suitable for demos, classroom activities, digital exhibitions, or creative AI-learning showcases.

## How The Game Works

The game begins with a polished start screen that introduces the webcam-based interaction. Once the player starts, the app activates the camera, initializes MediaPipe Hands, and opens the main quiz interface.

During gameplay:

- the left side shows the current math question, progress, score, and four answer cards
- the right side shows the live webcam feed with tracked hand landmarks
- the system detects raised fingers from `1` to `4`
- a hold-to-confirm mechanic prevents accidental selections
- correct answers award points and automatically move to the next question
- wrong answers trigger a retry flow so the student can attempt the same question again

At the end of the quiz, the player sees a final results screen with their total score and a celebratory finish sequence.

## Learning Experience

The quiz is built with a student-centered interaction model:

- **Touchless answering** makes the experience feel natural and memorable.
- **Retry instead of reveal** encourages learners to think again rather than simply copy the correct answer.
- **Voice support in Bahasa Melayu (`ms-MY`)** helps reinforce question delivery for younger learners.
- **Short celebratory feedback** through sound, color shifts, and confetti keeps motivation high.
- **Sectioned question flow** introduces a progression from easier arithmetic to more combined operations.

This makes the project more than a technical demo. It is also a playful educational tool that supports repetition, attention, and confidence-building.

## Technical Implementation

The project is implemented as a single self-contained HTML application with embedded CSS and JavaScript. Its architecture is lightweight, direct, and easy to run in a browser environment.

### Main technologies used

- **HTML/CSS/JavaScript** for the complete interface and game logic
- **MediaPipe Hands** for real-time hand landmark detection
- **camera_utils** for webcam handling
- **Web Speech API** for spoken question playback
- **Web Audio API** for win/lose sound effects
- **canvas-confetti** for celebration effects

### Implementation highlights

- A question bank of **29 math questions** is embedded directly in the file.
- Each question contains a section label, prompt, answer options, and the correct answer index.
- Finger detection is based on hand landmark comparisons from the tracked webcam feed.
- Only gestures between **1 and 4 fingers** are accepted as valid answer inputs.
- A hold-confirm system using `REQUIRED_FRAMES = 24` reduces false selections.
- Correct answers increase the score by `10` points and trigger automatic progression.
- A safeguard using an `answeredCorrectly` set prevents duplicate point farming on repeated attempts.
- Incorrect answers do not reveal the solution immediately, preserving the learning challenge.

## Interface Style

The game is designed with a strong sci-fi visual identity. The interface uses:

- glowing blue and cyan gradients
- glassmorphism panels
- animated background effects
- futuristic typography
- live camera overlays and progress indicators

This styling helps the quiz feel like an "AI mission" rather than a basic school exercise, which is a big part of the project's appeal.

## Project Structure

```text
HandGestureMath-AI-Quiz/
|- README.md
`- AI_Math_Game/
   `- AI_Math.html
```

## Running The Project

Because the game depends on webcam access, it should be opened in a browser environment that allows camera permissions. For the best experience, run it from a local server instead of opening the HTML file directly.

## Why This Project Stands Out

**HandGestureMath-AI-Quiz** stands out because it merges education and AI interaction in a form that is immediate, visual, and fun. It shows how computer vision can be used not only for advanced technical systems, but also for creative learning experiences that are accessible to students. The project demonstrates a meaningful combination of gamification, gesture control, and math practice in one compact implementation.
