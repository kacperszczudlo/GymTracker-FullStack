# GymTracker - FullStack Fitness App

![Android](https://img.shields.io/badge/Frontend-Android_Java-3DDC84?style=flat-square&logo=android)
![Spring Boot](https://img.shields.io/badge/Backend-Spring_Boot-6DB33F?style=flat-square&logo=springboot)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791?style=flat-square&logo=postgresql)
![Security](https://img.shields.io/badge/Security-JWT-000000?style=flat-square&logo=jsonwebtokens)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

## Opis
**GymTracker** to aplikacja fullstack do śledzenia treningów siłowych i postępów. Projekt składa się z:
- **Android app (Java)** – interfejs użytkownika do treningów, ćwiczeń i historii,
- **REST API (Spring Boot)** – logika biznesowa + autoryzacja **JWT**,
- **PostgreSQL** – baza danych.

Repozytorium ma strukturę **monorepo**:
- `frontend/` – aplikacja Android
- `backend/` – Spring Boot API + konfiguracja bazy

## Uruchomienie (skrót)
1. Sklonuj repo:
   ```bash
   git clone <URL_REPO>
   cd GymTracker-FullStack
   ```
2. Uruchom backend zgodnie z instrukcją w `backend/README.md` (domyślnie port **8080**).
3. Uruchom aplikację Android z `frontend/` (Android Studio) i ustaw adres backendu w konfiguracji aplikacji.

## Dokumentacja modułów
- Frontend: `frontend/README.md`
- Backend: `backend/README.md`

## Autor
Kacper Szczudło
