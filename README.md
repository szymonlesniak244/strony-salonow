# Strony dla salonów: z ankiety do gotowej strony

Projekt portfolio [Szymona Leśniaka](https://szymonlesniak244.github.io).
Podgląd: https://szymonlesniak244.github.io/strony-salonow/

**Oba salony są fikcyjne.** Dane, ceny i zdjęcia są przykładowe (zdjęcia z Unsplash).

## Jak to działa
1. Klient wypełnia ankietę w przeglądarce (`system/ankieta.html`). Ankieta zapisuje plik z danymi.
2. Schemat danych (`system/brief.schema.json`) sprawdza, czy plik jest kompletny.
3. Claude Code buduje stronę według spisanych zasad ([ZASADY-DLA-AI.md](ZASADY-DLA-AI.md)): wygląd na telefonie, dostępność, prywatność, bez wymyślonych treści.
4. Ja sprawdzam wynik na telefonie i komputerze.
5. Kalendarz rezerwacji działa na moim własnym systemie, który zastąpił SimplyBook. Rezerwację można przejść na obu stronach, a dane testowe znikają 7 dni po terminie.

## Zawartość
- `lawenda/`: Pracownia Włosa Lawenda (fryzjer)
- `luna/`: Pracownia Luna (kosmetyka)
- `system/`: ankieta i schemat danych

Czysty HTML i CSS, bez frameworków. Rezerwacja jest wstawiona w ramkę z osobnego systemu.
