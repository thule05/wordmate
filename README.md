# WordMate — English Vocabulary Learning App
WordMate is an Android application designed to make English vocabulary learning more engaging and organized. It combines topic-based vocabulary lessons, interactive flashcards, practice games, dictionary search, and progress tracking in one mobile app.

Built with Java and XML for Android, WordMate also integrates Firebase for account authentication and user-data synchronization.
## Features
- Topic-based vocabulary: Explore curated English vocabulary organized by topic, with pronunciation, meanings, and example sentences.
- Interactive flashcards: Review words, reveal their meanings, listen to pronunciation, shuffle cards, and mark words as learned.
- Vocabulary games: Practice with multiple-choice quizzes, missing-letter exercises, and word–meaning matching.
- Dictionary search: Look up English words through an online dictionary and receive search suggestions.
- Favorite word lists: Create and manage personalized collections for future review.
- Learning dashboard: Track learned words, review needs, study time, daily goals, weekly progress, and learning streaks.
- Study reminders: Set daily notifications to develop consistent learning habits.
- Account authentication: Sign up and sign in using email/password, Google, or Facebook.
- Cloud synchronization: Restore and sync supported user learning data with Firebase.
- Personalization: Configure app language, sound, reminders, and light/dark appearance.

## Tech Stack

| Category | Technologies |
|----------|--------------|
| Platform | Android (Min SDK 24, Target SDK 36) |
| Languages | Java, XML, Kotlin DSL |
| UI | AndroidX, Material Components, RecyclerView, ConstraintLayout |
| Authentication | Firebase Authentication, Google Sign-In, Facebook Login |
| Database | Firebase Realtime Database |
| Networking | Retrofit, Gson |
| APIs | Free Dictionary API, Datamuse API |
| Image Loading | Glide |
| Build Tools | Gradle, Android Gradle Plugin |




## Project Structure

```text
wordmate/
├── app/
│   ├── src/main/
│   │   ├── java/com/example/engapp/
│   │   │   ├── activities/       # App screens and user flows
│   │   │   ├── fragments/        # Main navigation screens
│   │   │   ├── adapters/         # RecyclerView adapters
│   │   │   ├── models/           # Data models
│   │   │   ├── network/          # API clients and services
│   │   │   ├── repositories/     # Data access and persistence
│   │   │   ├── receivers/        # Notification and boot receivers
│   │   │   └── utils/            # Shared utilities
│   │   ├── assets/
│   │   │   └── vocabulary.json
│   │   ├── res/
│   │   └── AndroidManifest.xml
│   ├── google-services.json
│   └── build.gradle.kts
├── gradle/
├── build.gradle.kts
├── settings.gradle.kts
├── gradlew
└── gradlew.bat
```


## Getting Started
Prerequisites
- Android Studio with an Android SDK compatible with this project
- JDK 17 or the compatible JDK configured by Android Studio
- Android device or emulator running Android 7.0 (API 24) or newer
- Internet connection for online dictionary search and cloud-based features
1. Clone the repository
git clone https://github.com/thule05/wordmate.git
cd wordmate
2. Open the project
1. Launch Android Studio.
2. Choose Open and select the cloned wordmate folder.
3. Let Gradle sync and download the required dependencies.
4. Install any Android SDK components requested by Android Studio.
3. Configure Firebase authentication (when using your own backend)
The repository contains an Android Firebase configuration associated with the original project. To connect a separate Firebase project:
1. Create a project in the Firebase Console.
2. Register an Android app with the package name com.example.engapp (or update the application ID accordingly).
3. Replace app/google-services.json with your project's configuration file.
4. Enable the required Firebase Authentication providers and set up Firebase Realtime Database with appropriate security rules.
5. For Google and Facebook login, configure the relevant OAuth/app settings and Android signing-key fingerprints for your environment.
Firebase sign-in and data synchronization depend on the corresponding backend configuration and access permissions. Do not add private credentials or service-account keys to the repository.

4. Build and run
Select an Android emulator or connected device, then click Run ▶ in Android Studio.

Alternatively, from the project root, build a debug APK:

Windows
.\gradlew.bat assembleDebug
macOS / Linux
./gradlew assembleDebug
The output APK is typically located at app/build/outputs/apk/debug/app-debug.apk.
##How to Use
1. Open WordMate and complete the initial onboarding steps.
2. Explore vocabulary topics on the Home screen.
3. Open a topic and study individual words with Flashcards.
4. Practice your knowledge using one of the three Games modes.
5. Use Search to look up other words and save them to a favorite list.
6. Review your learning statistics in Dashboard.
7. Customize notifications and preferences in Settings; sign in to use account-based synchronization.
##Application Design
WordMate separates screen logic, data access, and shared functionality:
- Activities / Fragments: User interface and navigation.
- Adapters / Models: Presentation of vocabulary and structured data.
- Repositories: Vocabulary loading, preferences, favorites, progress, and cloud synchronization.
- Network: Retrofit services for dictionary and word-suggestion APIs.
- Utilities / Receivers: Text-to-speech, reminders, localization, and supporting functions.
The built-in vocabulary dataset is stored in app/src/main/assets/vocabulary.json; online search uses the Free Dictionary and Datamuse APIs.
##Screenshots
Screenshots have not been added yet. You can create a screenshots/ folder and include images of Home, Flashcards, Games, Search, and Dashboard here.
##Author
@thule05
##License
No license file has been specified in this repository. Please contact the repository owner before reusing or redistributing the source code beyond what applicable law permits.
