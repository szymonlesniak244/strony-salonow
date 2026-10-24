# Zasady dla AI: strony dla salonów beauty i barberskich

Publiczna wersja pliku instrukcji (`CLAUDE.md`), który Claude Code czyta na początku każdej sesji.
Usunąłem z niej dane kont, szczegóły publikacji i ustawienia narzędzi.
Zasady powstają z moich decyzji i poprawek: każda nowa preferencja („nie podoba mi się X”, „zawsze rób Y”) trafia do tego pliku, żeby AI stosowało ją przy każdej kolejnej stronie.

## Jak to działa (bez osobnego generatora)
- Dane klienta są w `brief.json`, a jego zdjęcia i logo w folderze `assets/`.
- Klient wypełnia ankietę `system/ankieta.html` w przeglądarce i na końcu pobiera `brief.json`. Ankieta i schemat zmieniają się razem: nowe pole w schemacie = nowe pytanie w ankiecie.
- Format briefu opisuje `system/brief.schema.json`. To źródło prawdy o polach.
- Na prośbę „zrób stronę dla <slug>” AI czyta brief, sprawdza zgodność ze schematem i pisze gotową stronę w zwykłym HTML i CSS. Bez generatorów i bez instalowania pakietów.
- Każda nowa strona dostaje własny pomysł: motyw, układ, kształty, typografię, animację i wygląd kalendarza. Nie może wyglądać jak szablon z kart.
- Pomysły już użyte (nie powtarzać): Luna – księżyc, nocne niebo, fazy księżyca w krokach, zdjęcia w kole i łukach; Lawenda – złote pasmo włosów rysujące się linią, pąki lawendy w krokach, zdjęcia w kształcie kapsuły, wybór osoby „Z czym przychodzisz?”.
- **Brakujące dane: nic nie wymyślaj** (opinii, cen, zdjęć, godzin). Zostaw sekcję pustą albo zapytaj. Na stronach testowych dozwolone są zdjęcia ze stocku z listą źródeł i dopiskiem w stopce.

## Zasady techniczne strony
1. Zwykły HTML i CSS, bez frameworków. JavaScript tylko minimalny, a strona działa także bez niego.
2. Zero żądań do zewnętrznych serwerów (bez Google Fonts, Analytics, osadzonych map). Jedyny wyjątek to kalendarz rezerwacji SimplyBook.
3. Strona nie ustawia plików cookie. Jeśli jest kalendarz rezerwacji, polityka prywatności informuje o cookies dostawcy.
4. Najpierw telefon: kompozycja wyśrodkowana, brak poziomego przewijania od 320 px, przycisk „Umów wizytę” na górze i jako pasek na dole.
5. Dostępność: jeden `h1`, poprawna hierarchia nagłówków, widoczny focus, kontrast co najmniej 4,5:1, każdy obrazek z `alt`, etykiety w formularzach, link „przejdź do treści”.
6. Wydajność: `width` i `height` na obrazkach, `loading="lazy"` poniżej pierwszego ekranu, zdjęcia przeskalowane i bez metadanych (GPS).
7. Kolory marki muszą mieć dobry kontrast z tekstem na przyciskach.

## Sekcje strony (każda znika, gdy brak danych)
- Hero, usługi i cennik, zespół, o nas, galeria, opinie, rezerwacja, kontakt.
- Opinie tylko ze zgodą na publikację. Żadnych wymyślonych opinii ani gwiazdek.
- Rezerwacja: kalendarz SimplyBook dopasowany kolorami do strony, pod spodem zasady odwołania.

## Kalendarz rezerwacji (SimplyBook)
- Najpierw plik z konfiguracją z briefu: dane firmy, godziny, usługi z czasem i ceną, pracownicy, zasady odwołania, przypomnienia, kolory.
- Przypomnienia tylko e-mailem. Cały kalendarz po polsku (bez angielskich napisów).
- Wygląd kalendarza dopasowany do strony. Przed wdrożeniem sprawdzić każdy krok (kategoria, usługa, termin, formularz) na komputerze i telefonie.
- Bez płatności i danych kart w konfiguracji.

## SEO
- `<title>` do 60 znaków, `meta description` do 155 znaków, dane strukturalne `LocalBusiness` bez ocen i recenzji.
- Strony testowe mają `noindex` i są ukryte przed wyszukiwarkami.

## Dokumenty prawne
- Polityka prywatności i regulamin powstają z danych briefu, zrozumiale i ostrożnie. Nie twierdzić niczego, czego nie wiadomo.
- W nagłówku dokumentów zdanie, że to szablon do sprawdzenia przez prawnika. Strona prawdziwego klienta nie trafia na jego domenę bez zatwierdzenia dokumentów przez prawnika.

## Prywatność
- Do repozytoriów nie trafiają hasła, klucze ani prawdziwe dane osobowe klientów.
- Repozytoria prawdziwych klientów są prywatne.

## Po zakończeniu każdej strony
Sprawdzić: zgodność briefu ze schematem, brak błędów, jeden `h1`, wszystkie obrazki z `alt`, brak zewnętrznych adresów poza dozwolonymi, brak poziomego przewijania na 360 px, `noindex` w trybie testowym.
