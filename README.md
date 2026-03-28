# BlinkLock - Day 04

## What it does
Watches your eyes through the webcam.
Blink 3 times rapidly → screen locks.
Press 'u' → unlocks.

## How to run
1. pip install opencv-python mediapipe
2. python day04.py

## Controls
- Blink 3x fast = LOCK
- Press U = unlock
- Press Q = quit

## What I learned
- EAR (Eye Aspect Ratio) measures how open your eye is
- When EAR drops below the threshold, that counts as a blink
- State machine = program has 3 modes: IDLE, COUNTING, LOCKED
- Debounce = filtering out fake signals (eye must close for 2+ frames)
- Timeout = if you don't blink 3x within 2 seconds, it resets

## Threshold value used
EAR_THRESHOLD = 0.21
