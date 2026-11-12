# Wspólny Koszyk

Wspólna lista zakupów dla dwóch lub więcej osób. Dzieli zakupy na działy sklepu, pozwala odhaczać kupione rzeczy i planować obiady. Instaluje się na telefonie jako ikonka.

## Jak to uruchomić (jednorazowo, ok. 15 minut)

### Krok 1. Baza danych, która łączy Wasze telefony (Firebase, darmowe)

1. Wejdź na https://console.firebase.google.com i zaloguj się kontem Google.
2. Kliknij **Utwórz projekt**, nazwij go np. `wspolny-koszyk`. Google Analytics możesz wyłączyć.
3. W menu po lewej: **Kompilacja → Firestore Database → Utwórz bazę danych**. Wybierz lokalizację `eur3 (Europe)` i tryb produkcyjny.
4. W bazie otwórz zakładkę **Reguły**, usuń to, co tam jest, wklej całą zawartość pliku `firestore.rules` i kliknij **Opublikuj**.
5. Kliknij koło zębate → **Ustawienia projektu**. Na dole w sekcji **Twoje aplikacje** kliknij ikonę `</>` (aplikacja internetowa), nadaj nazwę i zarejestruj. Hostingu nie zaznaczaj.
6. Pojawi się fragment `const firebaseConfig = { ... }`. Skopiuj zawartość nawiasów klamrowych.
7. Otwórz plik `config.js` i zamień `null` na skopiowany fragment, żeby wyglądało jak w przykładzie w tym pliku.

### Krok 2. GitHub

1. Załóż konto na https://github.com (jeśli go nie masz).
2. Kliknij **+ → New repository**, nazwa `wspolny-koszyk`, zaznacz **Public**, kliknij **Create repository**.
3. Na stronie repozytorium kliknij **uploading an existing file** i przeciągnij tam WSZYSTKIE pliki z tego folderu razem z folderem `icons` (zawartość folderu, nie sam folder). Kliknij **Commit changes**.
4. **Settings → Pages**. W polu **Branch** wybierz `main` i `/ (root)`, kliknij **Save**.
5. Po 1–2 minutach aplikacja będzie pod adresem `https://TWOJA-NAZWA.github.io/wspolny-koszyk/`.

### Krok 3. Ikonka na telefonie

Otwórz ten adres na telefonie (oboje):

- **Android (Chrome):** menu ⋮ → **Dodaj do ekranu głównego** / **Zainstaluj aplikację**.
- **iPhone (Safari):** przycisk Udostępnij → **Do ekranu początkowego**.

### Krok 4. Połączenie w grupę

1. Ty: wpisz imię i kliknij **Utwórz grupę**. Zobaczysz 8-znakowy kod.
2. Druga osoba: wpisuje imię, wybiera **Mam kod grupy** i wpisuje Twój kod.

Od tej chwili macie jedną wspólną listę.

## Warto wiedzieć

- Każdy, kto zna kod grupy, widzi i zmienia listę. Nie ma haseł ani kont.
- Bez internetu aplikacja się otwiera i pokazuje ostatnią listę; zmiany wyślą się, gdy wróci zasięg.
- Dopóki `config.js` ma `null`, aplikacja działa w trybie próbnym: lista jest tylko na jednym urządzeniu.
