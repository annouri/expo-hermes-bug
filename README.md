README.md

Expo Hermes Error Reproduction (expo-hermes-bug)

This repository contains a minimal reproducible example (MRE) project that demonstrates a potential issue with Hermes in a new Expo project (bare workflow).

Observed Behavior:

    The app successfully builds and launches on an Android emulator or device.

    However, Logcat shows the error message:

    couldn't find DSO to load: libjscexecutor.so

This error might not prevent the app from running, but it indicates a potential problem with Hermes initialization.

Expected Behavior:

The app launches and runs without any errors in Logcat, suggesting successful utilization of Hermes for JavaScript execution.

Steps to Reproduce:

    Clone this repository:
    Bash

    git clone https://github.com/<your-username>/expo-hermes-bug.git

    

Replace <your-username> with your actual GitHub username.

Navigate to the project directory:
Bash

cd expo-hermes-bug

Build the project for Android (assuming you have the necessary tools installed):

a. Install dependencies (if necessary):

npm i

b. Prebuild for Android:
Bash

expo prebuild --platform android

Build the project for Android:
Bash

eas build --platform android --local

    Install the APK and run the app on an Android emulator

    Verify the Error:

    Use Logcat to observe the error message:

    couldn't find DSO to load: libjscexecutor.so

Additional Information:

    This project uses a bare workflow for Expo development.
    The presence of the error message doesn't necessarily prevent the app from functioning.

Purpose:

This MRE project helps investigate potential issues with Hermes initialization in new Expo projects and facilitate a resolution from the Expo development team.

Feel free to:

    Fork this repository and experiment further.
    Share this repository as a reference for others encountering the same error.
