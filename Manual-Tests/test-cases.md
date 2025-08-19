# Test Cases — Moduł logowania i koszyka (Demoblaze)  
Data: 2025-08-19  
Aplikacja demo: https://demoblaze.com

> Konwencja ID: TC-XXX (np. TC-001)

## Zakres
Scenariusze pozytywne i negatywne dla: rejestracji, logowania, dodawania do koszyka i zamówienia.

---

## Tabela przypadków testowych

| ID | Funkcjonalność | Priorytet | Kroki | Dane testowe | Oczekiwany rezultat |
|---:|----------------|:---------:|-------|--------------|----------------------|
| TC-001 | Rejestracja | Wysoki | 1. Wejdź na stronę główną → *Sign up* 2. Wpisz unikalny username i hasło 3. Kliknij *Sign up* | username: `user_20250819`; hasło: `Test123!` | Komunikat potwierdzający rejestrację; możliwość zalogowania nowym kontem |
| TC-002 | Rejestracja (duplikat) | Średni | 1. *Sign up* 2. Użyj istniejącego username 3. *Sign up* | username: istniejący | Komunikat o zajętej nazwie użytkownika; brak utworzenia konta |
| TC-003 | Logowanie — poprawne | Wysoki | 1. *Log in* 2. Wpisz prawidłowe dane 3. *Log in* | poprawny username/hasło | Zmiana nagłówka na *Welcome, <username>*; widoczny przycisk *Log out* |
| TC-004 | Logowanie — błędne hasło | Wysoki | 1. *Log in* 2. Wpisz prawidłowy username i błędne hasło 3. *Log in* | hasło: `wrongPass` | Komunikat o nieprawidłowych danych, brak logowania |
| TC-005 | Logowanie — puste pola | Średni | 1. *Log in* 2. Zostaw puste pola 3. *Log in* | — | Walidacja pól (alert); brak wysyłki formularza |
| TC-006 | Dodanie do koszyka | Wysoki | 1. Wybierz kategorię *Phones* 2. Otwórz produkt 3. *Add to cart* 4. Przejdź do *Cart* | np. „Samsung galaxy s6” | Produkt widoczny w koszyku z poprawną ceną |
| TC-007 | Usunięcie z koszyka | Średni | 1. Dodaj produkt (TC-006) 2. W *Cart* kliknij *Delete* | — | Produkt znika z koszyka; cena sumaryczna aktualizuje się |
| TC-008 | Finalizacja zamówienia | Wysoki | 1. W *Cart* kliknij *Place Order* 2. Uzupełnij formularz 3. *Purchase* | Imię, karta, miesiąc/rok | Komunikat z potwierdzeniem i kwotą; *OK* czyści koszyk |
| TC-009 | Finalizacja — puste wymagane pola | Wysoki | 1. *Place Order* 2. Zostaw puste *Name/Credit card* 3. *Purchase* | — | Walidacja wymaganych pól; brak finalizacji |
| TC-010 | Nawigacja paginacją | Niski | 1. Na stronie głównej klikaj *Next/Previous* | — | Lista produktów zmienia się zgodnie z paginacją |
| TC-011 | Sesja użytkownika | Średni | 1. Zaloguj się 2. Odśwież stronę 3. Przejdź do innej podstrony | — | Utrzymanie zalogowania w obrębie sesji/przeglądarki |
| TC-012 | Responsywność (sanity) | Niski | 1. Zmień szerokość okna (mobile/desktop) | — | Menu i karty produktów czytelne; brak nachodzenia elementów |
| TC-013 | Dostępność — focus | Niski | 1. Nawiguj klawiaturą (Tab/Shift+Tab) | — | Widoczny fokus na elementach interaktywnych |
| TC-014 | Odświeżenie koszyka | Średni | 1. Dodaj 2 różne produkty 2. Wejdź do koszyka 3. Odśwież stronę | — | Zawartość koszyka i suma zachowane |
| TC-015 | Wylogowanie | Średni | 1. *Log out* będąc zalogowanym | — | Znika *Welcome, <username>*; pojawia się *Log in/Sign up* |

---

## Uwagi
- Przed TC-003 załóż konto (TC-001) lub użyj istniejącego testowego.
- Dane kartowe: używaj danych testowych (mock), nie prawdziwych.
