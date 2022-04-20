# User Case: Półka

## Usuwanie własnej półki
Aktorzy: Użytkownik
1. Użytkownik wybiera opcję "usuń półkę"
2. System wyświetla komunikat o nieodwracalnej operacji usuwania danych i prośbę o potwierdzenie wykonania operacji
3. użytkownik potwierdza chęć wykonania operacji
4. System usuwa dane o półce 

### Scenariusze poboczne
3a. Uźytkownik nie potwierdza chęci wykonania operacji
3a1. Półka nie zostaje usunięta 

## Skopiowanie połki innego użytkownika
Aktorzy: Użytkownik
1. użytkownik wybiera widoczną dla niego pułkę innego użytkownika
2. Użytkownik wybiera opcję "kopiuj półkę"
3. Informacje o półce i zawartości zostają skopiowane i przypisane do konta Użytkownika.

## Zmienianie widoczności półki
Aktorzy: Użytkownik
1. Użytkownik wybiera opcję zmiany widoczności półki
2. System wyświetla okno dialogowe z możliwością wyboru nowych opcji widoczności
3. Użytkownik wybiera nowe opcje widoczności 
4. Użytkownik naciska przycisk "zapisz"
5. System stosuje nowe opcje widoczności

### Scenariusze poboczne
4a. Użytkownik naciska przyciks "anuluj"
4a1. Ustawienia widoczności nie zostają zmienione

## Dodawanie filmu do półki
Aktorzy: Użytkownik
1. Użytkownik wybiera film
2. Użytkownik wybiera dodaj do półki
3. System presentuje okno dialogowe z listą pułek użytkownika
4. Użytkownik wybiera półkę
5. System dodaje książkę do półki

### Scenariusze poboczne
3a. Uźytkownik wybiera utwóż nową półkę
3a1. System wyświetla okno dialogowe z prośbą o podanie nazwy nowej półki oraz ustawieniami widoczności
3a2. Użytkownik wprowadza nazwę i ustawienia widoczności
3a3. uzytkownik wybiera opcję utwórz nową półke
3a4. Pułka zostaje utworzona a system dodaje do wybrany film.
3a3a. Użytkownik wybiera opcję anuluj
3a3a1. Proces zostaje przerwany

## Usuwanie z półki
Aktorzy: Użytkownik
1. Użytkownik wybiera film
2. Użytkownik wybiera opcję "usuń z półki"
3. System usuwa informacje o przypisaniu filmu do półki

## Przeglądanie publicznych półek
Aktorzy: Gość, zalogoway użytkownik, zaufany użytkownik, admin
1. Aktor klika w "przeglądaj półkę" w profilu użytkownika.
2. Pokaż zawartość półki aktorowi.

### Scenariusze poboczne

2a. Półka danego użytkownika nie jest dostępna.
2a1. Wyświetl komunikat o niepowodzeniu.

## Usuwanie półki
Aktorzy: Admin
1. Admin klika w "usuń półkę" w przeglądzie półek.
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
3. Admin wybiera opcje kontynuacji działania.
4. Usuń wybraną półkę z systemu.
5. Wyświetl komunikat o powodzeniu.

### Scenariusze poboczne

3a. Admin wybiera "anuluj".


## Tworzenie półki
Aktorzy: Zalogowany użytkownik, zaufany użytkownik.
1. Aktor klika "dodaj półkę" w swoim przeglądzie półek.
2. Wyświetl formularz do tworzenia nowej półki z polami "widoczność", "nazwa", "filmy".
3. Aktor wypełnia wszystkie pola.
4. Aktor klika "zatwierdź".
5. Utwórz nową półkę przypisaną do tego użytkownika.
6. Wyświetl komunikat o powodzeniu.

### Scenariusze poboczne

3a. Użytkownik nie wypełnił wszystkich pól.
3a1. Użytkownik klika "zatwierdź".
3a2. Wyświetl komunikat o konieczności wypełnieniu wszystkich pól. idź do 2.


Autor 3 ostatnich: Dominik Kikla
Autor reszty: Antoni Lasoń




