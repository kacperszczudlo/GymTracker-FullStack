# GymTracker (Full‑Stack)

Aplikacja do śledzenia treningów siłowych: **Android (Java)** + **Spring Boot (REST API)** + **PostgreSQL**. Autoryzacja: **JWT**.

![Android](https://img.shields.io/badge/Frontend-Android_Java-3DDC84?style=flat-square&logo=android)
![Spring Boot](https://img.shields.io/badge/Backend-Spring_Boot-6DB33F?style=flat-square&logo=springboot)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791?style=flat-square&logo=postgresql)
![Security](https://img.shields.io/badge/Security-JWT-000000?style=flat-square&logo=jsonwebtokens)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

## Spis treści
- [Opis](#opis)
- [Struktura repozytorium](#struktura-repozytorium)
- [Wymagania](#wymagania)
- [Szybki start](#szybki-start)
- [Konfiguracja](#konfiguracja)
- [Dokumentacja modułów](#dokumentacja-modułów)
- [Autor](#autor)

## Opis
**GymTracker** pozwala planować i zapisywać treningi, zarządzać ćwiczeniami oraz przeglądać historię i postępy.

## Struktura repozytorium
To repozytorium jest **monorepo** i składa się z dwóch modułów:
- `frontend/` – aplikacja Android (Java)
- `backend/` – REST API (Spring Boot) + konfiguracja bazy

## Wymagania
- **Backend:** Java 17+, Maven/Gradle (zależnie od konfiguracji w module), PostgreSQL
- **Frontend:** Android Studio + Android SDK

> Szczegółowe wymagania i kroki uruchomienia są opisane w README w podkatalogach.

## Szybki start
1. Sklonuj repozytorium:
   ```bash
   git clone https://github.com/kacperszczudlo/GymTracker-FullStack.git
   cd GymTracker-FullStack
   ```
2. Uruchom backend zgodnie z instrukcją w `backend/README.md` (domyślnie port **8080**).
3. Uruchom aplikację Android z `frontend/` w Android Studio i ustaw adres backendu w konfiguracji aplikacji.

## Konfiguracja
- **Adres API**: ustawiany po stronie aplikacji Android (szczegóły w `frontend/README.md`).
- **Baza danych**: konfiguracja po stronie Spring Boot (szczegóły w `backend/README.md`).

## Dokumentacja modułów
- Frontend: `frontend/README.md`
- Backend: `backend/README.md`

## Autor
Kacper Szczudło
