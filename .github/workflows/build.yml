name: Build Android APK
on:
  workflow_dispatch:
  push:
    branches: [ main, master ]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-java@v4
        with:
          java-version: '17'
          distribution: 'temurin'
      - run: bash setup.sh && gradle assembleDebug
      - uses: actions/upload-artifact@v4
        with:
          name: JawakerBot-APK
          path: app/build/outputs/apk/debug/app-debug.apk
