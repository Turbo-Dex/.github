# 🚗 TurboDex

**TurboDex** is an open-source mobile app and platform for car enthusiasts, collectors, and communities.
With TurboDex you can catalog your cars, discover new vehicles, share your collection, and connect with other car lovers around the world.

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-3.x-blue?logo=flutter" alt="flutter" />
  <img src="https://img.shields.io/badge/Dart-3.x-0175C2?logo=dart" alt="dart" />
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="license" />
  <img src="https://img.shields.io/github/actions/workflow/status/TurboDexOrg/mobile-app/ci.yml?label=CI" alt="ci" />
</p>

---

## ✨ Features

* 📸 **Vehicle Pokedex** — browse and search cars like a collector’s Pokédex
* 🎨 **Collection Showcase** — create your own virtual garage and share it
* 🔥 **Feed & Social** — like, comment, and follow other enthusiasts
* 📍 **Geo-Tagged Cars** — add context with location and details
* 📲 **Built with Flutter** — cross-platform (iOS + Android)

---

## 🛠️ Tech Stack

* [Flutter](https://flutter.dev/) (Dart 3.x, Material 3, Provider for state management)
* Firebase (Auth, Firestore, Storage)
* GitHub Actions (CI/CD for build, lint, and tests)
* Modern Android Gradle setup (AGP 8+, Gradle 8+)

---

## 🚀 Getting Started

### Prerequisites

* [Flutter SDK](https://docs.flutter.dev/get-started/install) (3.22 or newer recommended)
* Dart SDK (included with Flutter)
* Android Studio / Xcode for emulators and builds

### Clone & Run

```bash
# Clone the repo
git clone https://github.com/TurboDexOrg/mobile-app.git
cd mobile-app

# Install dependencies
flutter pub get

# Run on device/emulator
flutter run
```

### Build APK

```bash
flutter build apk --release
```

---

## 📂 Project Structure

```
mobile-app/
├── lib/
│   ├── controllers/      # State management
│   ├── repositories/     # Data layer
│   ├── views/            # UI screens
│   ├── models/           # Data models
│   └── core/             # Theme & core utilities
├── test/                 # Unit/widget tests
├── android/              # Android native config
├── ios/                  # iOS native config
└── pubspec.yaml          # Dependencies & assets
```

---

## ✅ Contributing

We ❤️ contributions!

1. Fork the repo
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add some amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request 🚀

Check out our [CONTRIBUTING.md](CONTRIBUTING.md) for more details.

---

## 🧪 Testing

Run analyzer and unit/widget tests:

```bash
flutter analyze
flutter test
```

---

## 📦 CI/CD

* **Lint & Analyze**: Run `flutter analyze` on pull requests
* **Tests**: Run unit and widget tests with `flutter test`
* **Build**: GitHub Actions builds the release APK on merge

---

## 📸 Screenshots (optional)

> *Add some app screenshots or mockups here*

---

## 📜 License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.

---

## 👥 Community

* 💬 Discussions → [GitHub Discussions](https://github.com/TurboDexOrg/mobile-app/discussions)
* 🐛 Issues → [Report a bug](https://github.com/TurboDexOrg/mobile-app/issues)
* ⭐ Star the repo to support us!
