# flutter_rust_bridge_patched

This is a local vendor copy of `flutter_rust_bridge 2.11.1` with a **single change**.

## What changed

`pubspec.yaml`:
```yaml
# Original:
sdk: ">=3.4.0 <4.0.0"

# Patched:
sdk: ">=3.3.0 <4.0.0"
```

## Why

`flutter_rust_bridge` 2.x dropped Dart 3.3 support starting from `2.0.0-dev.39`.
This project requires compatibility with Flutter 3.19.6 (Dart 3.3.4).

All Dart source files are **byte-for-byte identical** to the official 2.11.1 release.
Only the SDK version constraint in `pubspec.yaml` was relaxed.

## How to upgrade in the future

1. `cp -r ~/.pub-cache/hosted/pub.flutter-io.cn/flutter_rust_bridge-<NEW_VERSION> ./flutter_rust_bridge_patched`
2. Edit `pubspec.yaml` inside: change `sdk: ">=3.4.0 <4.0.0"` → `sdk: ">=3.3.0 <4.0.0"`
3. Update `dependency_overrides` version comments in root `pubspec.yaml` and `example/pubspec.yaml`
