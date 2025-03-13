# Issue Tracker

Issue Tracker to aplikacja do zarządzania problemami w projektach. Umożliwia przeglądanie, tworzenie i zarządzanie problemami w projekcie.

## Wymagania

- Node.js w wersji 14 lub nowszej
- Baza danych MySQL

## Instalacja

1. Sklonuj repozytorium:

   ```sh
   git clone https://github.com/vat332/issue-tracker.git
   cd issue-tracker
   ```

2. Zainstaluj zależności:

   ```sh
   npm install
   ```

3. Skonfiguruj plik `.env` na podstawie `.env.example`:

   ```sh
   cp .env.example .env
   ```

4. Uruchom migracje bazy danych:
   ```sh
   npx prisma migrate dev
   ```

## Uruchomienie

Aby uruchomić aplikację w trybie deweloperskim, użyj:

```sh
npm run dev
```

Aplikacja będzie dostępna pod adresem `http://localhost:3000`.

## Budowanie

Aby zbudować aplikację do produkcji, użyj:

```sh
npm run build
```

Aby uruchomić zbudowaną aplikację, użyj:

```sh
npm start
```

## Struktura projektu

- 🛠️ `.env.example` - przykładowy plik konfiguracyjny środowiska
- 🔄 `middleware.ts` - plik middleware
- 🔗 `QueryClientProvider.tsx` - komponent dostarczający klienta zapytań
- 📂 `.next/` - katalog generowany przez Next.js zawierający pliki builda
- 📁 `app/` - główny katalog aplikacji zawierający komponenty i strony
  - 📁 `api/` - katalog aplikacji zawierający
    implementacje endpointow
    - 📁 `auth/` - katalog zawierający uwierzytelnianie
    - 📁 `issues/` - endpoint issues
    - 📁 `users/` - endpoint users
  - 📁 `auth/` - katalog zawierający uwierzytelnianie
  - 📁 `components/` - katalog aplikacji zawierający komponenty
  - 📁 `issues/` - katalog aplikacji zawierający komponenty
  - 📊 `IssueChart.tsx` - komponent wykresu zgłoszeń
  - 📋 `IssueSummary.tsx` - komponent podsumowania zgłoszeń
  - 🆕 `LatestIssues.tsx` - komponent najnowszych zgłoszeń
  - 🏗️ `layout.tsx` - główny layout aplikacji
  - 🧭 `NavBar.tsx` - komponent nawigacji
  - 📄 `page.tsx` - główna strona aplikacji
  - 🎨 `theme-config.css` - konfiguracja motywu
  - ✅ `validationSchemas.ts` - schematy walidacji
- 🗄️ `prisma/` - katalog zawierający schemat bazy danych Prisma
- 🌍 `public/` - katalog zawierający zasoby publiczne, takie jak obrazy i pliki statyczne

## Technologie

- Next.js
- React
- Prisma
- Tailwind CSS

## Autorzy

- [vat332](https://github.com/vat332)

## Licencja

Ten projekt jest licencjonowany na warunkach licencji MIT.

.
