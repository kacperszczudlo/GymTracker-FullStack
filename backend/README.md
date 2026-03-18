# GymTracker — Backend (Spring Boot)

REST API dla aplikacji **GymTracker**.

## Tech stack
- **Java 21**
- **Spring Boot 3.4.4**
- **Spring Web**
- **Spring Data JPA + Hibernate**
- **PostgreSQL**
- **Spring Security**
- **JWT** (biblioteka `io.jsonwebtoken:jjwt`)
- Maven (Maven Wrapper: `mvnw` / `mvnw.cmd`)

## Wymagania
- Java **21**
- Dostęp do **PostgreSQL**
- (Opcjonalnie) IntelliJ IDEA / inny IDE

## Struktura katalogu
Najważniejsze pliki:
- `pom.xml` — zależności i konfiguracja builda
- `mvnw`, `mvnw.cmd`, `.mvn/` — Maven Wrapper
- `src/main/resources/application.properties` — konfiguracja aplikacji (DB, JPA, itp.)
- `src/main/java/...` — kod aplikacji (kontrolery/serwisy/encje itd.)
- `src/test/java/...` — testy (jeśli/jeżeli dodasz)

## Konfiguracja (application.properties)

Plik: `src/main/resources/application.properties`

Wartości, które zwykle musisz ustawić lokalnie:
- `spring.datasource.url`
- `spring.datasource.username`
- `spring.datasource.password`

### Ważne (bezpieczeństwo)
W repo wida��, że w `application.properties` jest wpisany adres hosta DB.
Rekomendacja:
- nie trzymać produkcyjnych/semiotwartych danych w repo,
- przenieść konfigurację do zmiennych środowiskowych lub osobnego profilu (`application-local.properties` dodanego do `.gitignore`).

Przykład podejścia z env (do rozważenia):
```properties
spring.datasource.url=${DB_URL}
spring.datasource.username=${DB_USER}
spring.datasource.password=${DB_PASSWORD}
```

## Uruchomienie

### 1) Baza danych (PostgreSQL)
Upewnij się, że PostgreSQL działa i masz utworzoną bazę (oraz ewentualnie schemat), a dane w `application.properties` pasują do Twojego środowiska.

W konfiguracji widać m.in.:
- `spring.jpa.hibernate.ddl-auto=validate` (czyli aplikacja **sprawdza** schemat, ale go nie tworzy)

To oznacza, że **tabele muszą już istnieć** (np. utworzone wcześniej/migracjami).

### 2) Start aplikacji
W katalogu `backend/`:

```bash
# Linux/Mac
./mvnw spring-boot:run
```

```bat
:: Windows
mvnw.cmd spring-boot:run
```

Domyślnie backend powinien wystartować na porcie **8080** (o ile nie zmienisz `server.port`).

### 3) Build JAR (opcjonalnie)
```bash
./mvnw clean package
```

## Notatki
- Jeśli pojawia się błąd połączenia z DB: sprawdź URL/port, dane logowania oraz czy DB jest dostępna z Twojej sieci.
- Jeśli `ddl-auto=validate` wywala błędy: schemat w bazie nie zgadza się z encjami JPA (trzeba wyrównać tabele albo zmienić strategię/migracje).