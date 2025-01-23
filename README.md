# Expo DocumentPicker - Empty URI on Android

This repository demonstrates a bug in the Expo DocumentPicker API on Android.  The `DocumentPicker.getDocumentAsync()` function occasionally returns an empty URI when selecting a file, preventing access to the selected file.  The solution provides a workaround to handle this unexpected behavior.

## Bug Description

When using the Expo DocumentPicker API to select a file on an Android device, the `uri` property of the returned object is sometimes empty, leading to errors downstream when attempting to use the file.

## Reproduction

1. Run the `bug.js` example on an Android device.
2. Select a file using the DocumentPicker.
3. Observe that the `uri` is sometimes empty, leading to an error.

## Solution

The `bugSolution.js` file demonstrates a workaround. This involves checking if the `uri` is empty. If empty, display an appropriate message to the user.