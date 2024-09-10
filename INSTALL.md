# How to setup React Native

## System Reuirements (My Laptop - ApertureSTRIX)
CPU: Ryzen 9 7945HX
RAM: 32GB DDR5
GPU: Nvidia 4060 Laptop + Radeon 610M
SSD: Samsung 980 PRO 2TB + Micron 2400 1TB
Windows Version: Windows 11 Pro, 23H2

## Installation Instructions
1. Download Android Command Line Tools, move to SDK root folder, and use `sdkamanager` to download the Android 14 SDK, Emulator, Android 14 System Image, Android Platform Tools and Android 14 Build Tools.
2. Download NodeJS, latest version.
3. Download VSCode, latest version.
4. Create a new project with `npx @react-native-community/cli@latest init <ProjectNameHere>`
5. Attempt to run the project with `npm run android` 
6. Pray everything works, if not, refer to Troubleshooting.

## Configuration Steps
1. Make sure to set ANDROID_HOME enviroment variable to the SDK folder root.

## Project Creation
1. Run `npx @react-native-community/cli@latest init <ProjectNameHere>`, replacing ProjectNameHere with the name of the project

## Running the project
1. Spin up an android emulator, with either `emulator -avd <avd-name-here>` or through Android Studio
2. Run `npm run android`

## Troubleshooting
- You will likely get errors saying something in the SDK is malformed, meaning you need to make sure it is structured properly. The SDK should have the root android folder, with cmdline-tools that contains latest, then bin, then the tools. Once the SDK is in this format, you can use `sdkmanager` to download more android sdk things.
- Sometimes the first few builds fail, you can resolve this by alternating between `npm run dev` and `npm run android`. Eventually everything should work. If not, try googling the error and following stack overflow threads. (React Native is very picky to get started 😅)

## Resources
[React Native Docs](https://reactnative.dev/docs)
Most react native threads on StackOverflow (Use google to find relevant ones.)