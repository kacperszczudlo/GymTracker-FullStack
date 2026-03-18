![Android](https://img.shields.io/badge/Frontend-Android-3DDC84?style=flat-square&logo=android)
![Kotlin](https://img.shields.io/badge/Language-Kotlin-7F52FF?style=flat-square&logo=kotlin)
![Gradle](https://img.shields.io/badge/Build-Gradle-02303A?style=flat-square&logo=gradle)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

# GymTracker — Frontend (Android)

Aplikacja mobilna **GymTracker** (frontend) na Androida.

## Tech stack
- **Kotlin**
- **Android SDK**
- **Gradle (Kotlin DSL)** (`build.gradle.kts`, `settings.gradle.kts`)
- Repozytoria: **Google Maven**, **Maven Central**, **JitPack**

## Wymagania
- Android Studio (rekomendowane)
- JDK (zgodne z Android Studio / ustawieniami projektu)
- Android SDK + emulator lub fizyczne urządzenie

## Struktura katalogu
Najważniejsze pliki/katalogi:
- `app/` — moduł aplikacji (kod źródłowy, zasoby, manifest)
- `build.gradle.kts` — top-level konfiguracja Gradle
- `settings.gradle.kts` — konfiguracja projektu (m.in. `rootProject.name`, `include(":app")`, repozytoria)
- `gradle.properties` — ustawienia Gradle
- `gradle/`, `gradlew`, `gradlew.bat` — Gradle Wrapper

## Konfiguracja

### Backend URL / API
Jeżeli aplikacja komunikuje się z backendem, upewnij się, że adres API (base URL) jest ustawiony poprawnie w kodzie/konfiguracji.

**Tip:** dla emulatora Androida backend uruchomiony lokalnie na Twoim komputerze zwykle jest dostępny pod `http://10.0.2.2:<port>` (zamiast `localhost`).

## Uruchomienie

### 1) Android Studio
1. Otwórz katalog `frontend/` w Android Studio.
2. Poczekaj aż Gradle zsynchronizuje projekt.
3. Wybierz urządzenie (emulator lub telefon).
4. Kliknij **Run**.

### 2) Z linii komend (opcjonalnie)
W katalogu `frontend/`:

```bash
# Linux/Mac
./gradlew assembleDebug
