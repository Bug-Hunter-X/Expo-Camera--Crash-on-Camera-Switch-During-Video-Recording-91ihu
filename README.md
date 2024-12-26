# Expo Camera Crash on Camera Switch During Video Recording

This repository demonstrates a bug in the Expo `Camera` API where switching cameras while recording video leads to inconsistent crashes. The issue is particularly noticeable when using a custom camera UI rather than the default Expo components.

## Bug Description

The app crashes or freezes unpredictably when the user attempts to switch between the front and rear cameras during video recording.  Console logs often lack detailed error messages, hindering debugging.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app using Expo Go.
4. Begin recording a video.
5. Attempt to switch cameras (front to back or back to front).
6. Observe the app crashing or freezing.

## Solution

A potential solution (implemented in `bugSolution.js`) involves adding more robust error handling and asynchronous operations during the camera switching process, making sure the camera is fully stopped before attempting a switch. This is not a guaranteed fix, but it may improve the stability.