# Strony dla salonów: z ankiety do gotowej strony

Projekt portfolio [Szymona Leśniaka](https://szymonlesniak244.github.io).
Podgląd: https://szymonlesniak244.github.io/strony-salonow/

**Oba salony są fikcyjne.** Dane, ceny i zdjęcia są przykładowe (zdjęcia z Unsplash).

## Jak to działa
1. Klient wypełnia ankietę w przeglądarce (`system/ankieta.html`). Ankieta zapisuje plik z danymi.
2. Plik sprawdza schemat danych (`system/brief.schema.json`).
3. Claude Code buduje stronę według spisanych przeze mnie zasad: telefon, dostępność, prywatność, bez wymyślonych treści.
4. Ja sprawdzam wynik na telefonie i komputerze.
5. Na stronie działa kalendarz rezerwacji SimplyBook. W tej wersji demo zastąpiłem go zrzutami (`rezerwacja-demo/`).

## Zawartość
- `lawenda/`: Pracownia Włosa Lawenda (fryzjer)
- `luna/`: Pracownia Luna (kosmetyka)
- `system/`: ankieta i schemat danych
- `rezerwacja-demo/`: zrzuty procesu rezerwacji (konto testowe, rezerwacja niewysłana)

Czysty HTML i CSS, bez frameworków.
