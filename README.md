# Flutter iOS CI Demo

A Flutter iOS simulator app that builds via GitHub Actions and uploads to AutoDevice.

## Build

```bash
flutter pub get
flutter build ios --simulator --debug
```

The output `.app` is in `build/ios/iphonesimulator/`.

## CI/CD

The GitHub Actions workflow (`.github/workflows/build.yml`) runs on every push to `main`:

1. Sets up Flutter 3.27.4 on `macos-15`
2. Builds a simulator app with `flutter build ios --simulator --debug`
3. Uploads the `.app` to AutoDevice

## Required Secrets

- `AUTODEVICE_API_KEY` — AutoDevice API key for uploading builds
