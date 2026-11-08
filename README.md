🏛️ HeritageWalk Sri Lanka 🇱🇰 

Explore Sri Lanka's heritage. Plan meaningful journeys. Navigate with confidence.

HeritageWalk Sri Lanka is a Flutter mobile application developed as a group project for IT3060 – Human Computer Interaction. It brings heritage-place discovery, personalized tour planning, saved content, map-based navigation, and group-tour features into one mobile experience.

> **Project status:** Academic project / portfolio showcase. Features and third-party integrations may require configuration or permissions before use. This README describes the team's implementation; it is not a claim that every feature has been independently verified on every device.


💭 Overview

Visitors exploring Sri Lanka's historical and cultural sites may need to switch between separate resources to discover destinations, organize visits, navigate routes, and coordinate with others. HeritageWalk Sri Lanka aims to streamline these tasks through a mobile-first, user-centred interface.


❤️‍🔥 Features

Account & profile	 - Email/password authentication, password reset, Google sign-in, Facebook sign-in integration, profile management

Heritage discovery -	Home dashboard, featured places, searchable Explore catalog, categories, filters, place details and imagery

Tour planning	- Plan tours, generate itineraries, and save itineraries for later

Saved content	- Add and remove favorite places with persistent storage

Community feedback	- Place ratings and reviews, with administrative moderation

Maps & navigation	- GPS location, OpenStreetMap-based maps, and route guidance through OSRM

Group tours	- Group participation and opt-in, time-limited location sharing

Safety & support	- Facility and emergency-contact information, support features

Localization	- English, Sinhala, and Tamil interfaces

Content administration	- Heritage-place management and predefined place data for form auto-fill


➡️ Technology Stack

Mobile UI: Flutter, Dart

Authentication: Firebase Authentication; Google Sign-In; Facebook Login integration

Cloud data: Cloud Firestore

Maps: `flutter_map`, OpenStreetMap, `latlong2`

Location: `geolocator`

Routing: OSRM (Open Source Routing Machine), HTTP

Localization: Flutter localization tools, `intl`

Testing: Flutter tests and Firebase security-rule validation


📌 Architecture (high level)
```text
Flutter Mobile App
  ├── Presentation / Screens / Localization
  ├── Application Services & State
  │     ├── Heritage Discovery & Tour Planning
  │     ├── Favorites & Reviews
  │     ├── Navigation & Group Sharing
  │     └── Authentication & Profiles
  ├── Firebase Authentication
  ├── Cloud Firestore + Security Rules
  └── External Map / Location Services
        ├── OpenStreetMap
        ├── OSRM Routing
        └── Device GPS
```
This is a conceptual overview, not an exact source-code directory diagram. Replace it with the team's final architecture diagram if available.


👏 Getting Started

Prerequisites

💠 Flutter SDK compatible with the project's `pubspec.yaml`

💠 Dart SDK (bundled with Flutter)

💠 Android Studio or VS Code with Flutter tooling

💠 Android emulator or physical Android device

💠 Firebase project configured for your development environment

Run locally
```bash
git clone <YOUR-REPOSITORY-URL>
cd <YOUR-REPOSITORY-FOLDER>
flutter pub get
flutter run
```

Firebase setup: Configure the project using the supported FlutterFire/Firebase workflow. Authentication providers such as Google and Facebook require their own provider-specific setup, app identifiers, and signing fingerprints. Do not commit private keys, service-account credentials, or access tokens. Some platform configuration files may be needed for a functioning build; review them carefully before publication.

Quality checks
```bash
flutter analyze
flutter test
flutter build apk --release
```
The generated APK is normally located at `build/app/outputs/flutter-apk/app-release.apk`. A release APK requires the appropriate signing configuration for distribution.

🎖️ Human-Centred Design Process

The application was developed within the IT3060 Human Computer Interaction module, following a progression from identifying user needs and requirements to sketches, wireframes, prototypes, implementation, and evaluation.

The supporting requirements PDF should summarize the research approach, stakeholder needs, key findings, and functional/non-functional requirements. The testing PDF should document test cases, expected and actual results, evidence, and usability findings where available.


😎 Team & Contributions

Group: WD_22

📌 IT23839410 - W A N M Dilshan	- Account Authentication & Profile Management

📌 IT23839038 -	A B K S Sithuruwan	- Tour Discovery, Planning & Saved Content

📌IT23825550 - N M S H Premarathna -	Navigation, Digital Guide, Facilities & Safety

📌IT23841772	- R D I H Rajapaksha	- Group Tour, Language & Support Features

Portfolio note: If showcasing this repository on an individual portfolio, clearly state your personal contribution and credit all teammates. For example: My primary responsibility was tour discovery, itinerary planning, and saved-content workflows, including UI integration and Firestore persistence.


🔏 Privacy & Security

Location sharing is designed to be opt-in, with explicit stopping and expiry behaviour.

Firebase security rules should be deployed and validated for the environment in use.

Do not publish real user data, raw research participant identifiers, private API keys, signing keys, or credentials.

Review third-party map tile/routing service usage policies and attribution requirements before public deployment.


😒 Known Limitations
Social sign-in providers require external console configuration and may not function in an unconfigured fork.

GPS, connectivity, map/routing availability, and device permissions affect location-based features.

Multi-device group-sharing behaviour should be verified on physical devices for each release.

The app is an academic project and should not be presented as a production-certified navigation or emergency-response service.


👊 License
License not yet specified. Confirm ownership and permission from all group members before adding an open-source license or making the repository public. If the team chooses an open-source license, add a `LICENSE` file and update this section.

Developed for IT3060 – Human Computer Interaction as the HeritageWalk Sri Lanka group project. Mapping and location functionality uses third-party open mapping and routing technologies; retain applicable provider attribution in the application and documentation.
