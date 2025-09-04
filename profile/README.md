# 🚗 TurboDex

**TurboDex** is an open-source mobile app and platform for car enthusiasts, collectors, and communities.
With TurboDex you can catalog your cars, discover new vehicles, share your collection, and connect with other car lovers around the world.

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-3.x-blue?logo=flutter" alt="flutter" />
  <img src="https://img.shields.io/badge/Dart-3.x-0175C2?logo=dart" alt="dart" />
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="license" />
  <img src="https://img.shields.io/github/actions/workflow/status/Turbo-Dex/mobile_app/app.yml?branch=dev&label=Mobile%20App%20CI" alt="ci" />
  <img src="https://img.shields.io/github/actions/workflow/status/Turbo-Dex/TurboAi/ai.yml?branch=dev&label=Turbo%20Ai%20CI" alt="ci" />
  <img src="https://img.shields.io/github/actions/workflow/status/Turbo-Dex/TurboAi/blur.yml?branch=dev&label=Turbo%20Blur%20CI" alt="ci" />
  <img src="https://img.shields.io/github/actions/workflow/status/Turbo-Dex/backend/infra.yml?label=Backend%20CI" alt="ci" />
</p>

### Why TurboDex?

Car culture is more than just machines — it’s stories, memories, and connections. But until now, enthusiasts lacked a single place to catalog, share, and discover cars the way collectors do with trading cards or Pokédexes. TurboDex helps by solving these challenges:

#### For Car Spotters
Keep track of rare sightings with geo-tags, details, and photos — your own digital logbook of cars in the wild.

#### For Collectors 
Showcase your garage like a virtual museum, share it with others, and get inspired by collections around the globe.

#### For Garagists & Builders
Identify the vehicle in front of you.

#### For Communities
Connect with fellow enthusiasts, share stories, follow trends, and join conversations around the cars you love.

#### For Dreamers 
Not everyone can own their dream car — but with TurboDex, you can build your fantasy garage and explore without limits.

In short: TurboDex is the social hub and catalog for cars — whether you’re spotting, collecting, restoring, or just dreaming.

---

## Features

* **Vehicle Compendium** — browse and search cars like a collector’s Pokédex
* **Collection Showcase** — create your own virtual garage and share it
* **Feed & Social** — like, comment, and follow other enthusiasts
* **Geo-Tagged Cars** — add context with location and details
* **Built with Flutter** — cross-platform (iOS + Android)

---

##  Team Zone

| Name        | Role               | Responsibilities |
|-------------|--------------------|------------------|
| [Alexandre](https://github.com/Nekoth93)       |  AI Training     | Build and fine-tune car recognition models, blur AI, and analytics |
| [Dani](https://github.com/Dansnts)         |   DevOps          | Manage CI/CD pipelines, Scrum Master,Kubernetes, Terraform, cloud infrastructure and multi-task |
| [Evan](https://github.com/EVAN-ROTHEN)       |  Frontend Dev    | Design and develop the mobile app UI/UX with Flutter and Dart |
| [Jonathan](https://github.com/JONATHAN-THIEBAUD)        | Backend Dev     | Develop APIs, databases, business logic powering the platform and mobile app developement |

---

## Tech Stack

* [Flutter](https://flutter.dev/) (Dart 3.x, Material 3, Provider for state management)
* Azure (Auth, AI, Storage)
* GitHub Actions (CI/CD for build, lint, and tests)
* Modern Android Gradle setup (AGP 8+, Gradle 8+)
* Kubernetes (Load balancing and pods)

---

## Getting Started

### Prerequisites

* [Flutter SDK](https://docs.flutter.dev/get-started/install) (3.51 or newer recommended)
* Dart SDK (included with Flutter)
* Android Studio / Xcode for emulators and builds
* Latest version of Docker and MiniKube
* Azure CLI
* GPU with CUDA support (Nvidia)

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


### Clone & Run AI

```bash
# Clone the repo
git clone https://github.com/TurboDexOrg/TurboAi.git
cd TuboAI

# Train AI
docker compose up --build

# Run blur AI
cd TurboBlur
docker build -t car-blur .
docker run -p 5000:5000 car-blur

# Run analyse AI
cd TurboApi
docker build -t car-api .
docker run -p 5000:5000 car-api
```


### Deploy on Azure

```bash
# Clone the repo
git clone https://github.com/TurboDexOrg/backend.git
cd backend/AzureInfra/terraform

# Change your values from the var files

# Init terraform
terraform init
terraform validate

# Deploy terraform
terraform plan -out=turbodex
terraform apply turbodex

# Deploy DB and files (or do it manually)
ansible-playbook -i inventory_file cd../ansible/playbook.yml
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

---

## Testing

Run analyzer and unit/widget tests:

```bash
flutter analyze
flutter test
```

---

## CI/CD
### Mobile App
* **Lint & Analyze**: Run `flutter analyze` on pull requests
* **Tests**: Run unit and widget tests with `flutter test`
* **Build**: GitHub Actions builds the release APK on merge

### TurboAI
* Build and push images to the ACR

### Backend
* Build and push infra to Azure (Manual trigger)

---

## Collaborate

We welcome contributions from car enthusiasts, developers, and AI tinkerers alike!  
Here’s how you can get involved:

1. **Fork the repo** and create your feature branch  
   ```bash
   git checkout -b feature/amazing-feature
2. Commit your changes with clear messages

```bash
git commit -m "feat: add amazing feature"
Push to the branch
```
3. Push to the branch
```bash
git push origin feature/amazing-feature
```
4. Open a Pull Request and describe your changes



- Check the issues for things to work on.
- Join the discussions to suggest new ideas or features.
- Follow our coding style and run tests before submitting PRs.

Together, we can make TurboDex the ultimate hub for car lovers worldwide.

---

## Screenshots

> Comming soon

---

## 📜 License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Community

* Discussions → [GitHub Discussions](https://github.com/Turbo-Dex/mobile_app/discussions)
* Issues → [Report a bug](https://github.com/Turbo-Dex/mobile_app/issues)
* ⭐ Star the repo to support us!
