# Silent Failure of Expo Linking.openURL

This repository demonstrates a silent failure issue with Expo's `Linking.openURL` API. When attempting to open a URL with a custom scheme (e.g., `myapp://`), the function fails silently if the scheme is unregistered or the associated application is not installed on the device.

This lack of feedback makes it difficult to handle such situations gracefully within the app.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app on an emulator or physical device.
4. Try to open the URL; it will fail without any clear indication.

## Solution

The solution involves adding error handling to detect and gracefully manage these failures. The `bugSolution.js` file demonstrates this improved implementation.