# Pulpit MC

Narzędzie do przygotowania i prowadzenia spotkań młodzieżówek Beloved, Source Youth i zjazdów SUM.

- `index.html` – aplikacja: planowanie, archiwum, scena. Logowanie kontem Google, dane w Firebase (Firestore).
- `scena/` – widok sceniczny bez logowania. Plan przychodzi w linku (`#p=...`), strona nie wysyła go na żaden serwer.
- `config.js` – konfiguracja projektu Firebase (wartości publiczne).
- `firestore.rules` – reguły dostępu do bazy. Po każdej zmianie wklej je w konsoli Firebase.
- `lib/firebase-12.19.0.js` – biblioteka Firebase (app, auth, firestore) spakowana do jednego pliku, bez CDN.
- `artefakt/` – źródło poprzedniej wersji (artefakt na claude.ai).

Dostęp:
- administrator: dokument `admins/<gmail>` dodany ręcznie w konsoli Firebase;
- osoby z dostępem: `allow/<gmail>`, dodaje je administrator w aplikacji (Konto → Osoby z dostępem);
- spotkania i zjazdy widzi administrator i osoby z pola `members` (przycisk „Kto widzi”).

W repozytorium nie ma żadnych danych spotkań ani danych osobowych, tylko kod.
Do testów bez bazy na localhost: `index.html?lokalnie` (zapis tylko w przeglądarce).
