# Bug Reports — Przykładowe zgłoszenia (Demoblaze)  
Data: 2025-08-19

> Konwencja ID: BUG-XXX

---

## BUG-001 — Brak komunikatu walidacji dla pustego hasła w logowaniu
**Środowisko:** Windows 10, Chrome 126  
**Kroki:**
1. Przejdź do https://demoblaze.com
2. Kliknij *Log in*
3. Wpisz poprawny username, pole hasła pozostaw puste
4. Kliknij *Log in*
**Oczekiwany rezultat:** Widoczny komunikat walidacyjny „Password is required” i brak próby logowania.  
**Rzeczywisty rezultat:** Alert przeglądarkowy nie wyświetla się, formularz zdaje się wysyłać.  
**Częstotliwość:** Zawsze  
**Priorytet:** Wysoki  
**Załączniki:** (zrzut ekranu/krótki film)

---

## BUG-002 — Suma w koszyku nie aktualizuje się po usunięciu produktu
**Środowisko:** macOS 14, Safari 17  
**Kroki:**
1. Dodaj 2 produkty do koszyka
2. Przejdź do *Cart*
3. Kliknij *Delete* przy jednym z produktów
**Oczekiwany rezultat:** Produkt znika; suma ulega zmniejszeniu o cenę usuniętego produktu.  
**Rzeczywisty rezultat:** Produkt znika z listy, ale suma pozostaje bez zmian do odświeżenia strony.  
**Częstotliwość:** Czasami (ok. 50%)  
**Priorytet:** Wysoki  
**Dodatkowe info:** Podejrzenie odświeżania sumy po stronie klienta — brak eventu po usunięciu.

---

## BUG-003 — Brak widocznego fokusa na przyciskach (dostępność)
**Środowisko:** Windows 11, Chrome/Edge (klawiatura)  
**Kroki:**
1. Otwórz stronę główną
2. Poruszaj się klawiszem Tab po elementach interaktywnych
**Oczekiwany rezultat:** Wyraźny wskaźnik fokus (outline) na przyciskach i linkach.  
**Rzeczywisty rezultat:** Fokus jest słabo widoczny lub niewidoczny w niektórych elementach.  
**Częstotliwość:** Zawsze  
**Priorytet:** Średni  
**Wpływ:** Utrudnienie dla użytkowników korzystających z klawiatury.

---

## BUG-004 — „Place Order” pozwala wysłać formularz bez numeru karty
**Środowisko:** Windows 10, Firefox 127  
**Kroki:**
1. Dodaj produkt do koszyka
2. Przejdź do *Cart* → *Place Order*
3. Wypełnij *Name* i *Month/Year*, pozostaw *Credit card* puste
4. Kliknij *Purchase*
**Oczekiwany rezultat:** Walidacja wymaganych pól, brak finalizacji.  
**Rzeczywisty rezultat:** Zamówienie przechodzi, a w potwierdzeniu pojawia się kwota bez danych karty.  
**Częstotliwość:** Rzadko (reprodukowalne po kilku próbach)  
**Priorytet:** Wysoki  
**Uwagi:** Potencjalny problem z walidacją po stronie klienta.
