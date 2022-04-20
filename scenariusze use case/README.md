# SCENARIUSZE USE CASE-ÓW

---

## STRONA GŁÓWNA
Autor Poniższych: Kamila Baizakova

### Use case - wyszukiwanie filmów

aktorzy: gość, zalogowany użytkownik, super użytkownik
główny scenariusz:

1. Dowolny z aktorów klika przycisk "wyszukiwanie filmów" na stronie głównej
2. System prosi użytkownika o wprowadzenie informacji o filmie (nazwa,rezyser, tytuł, opis, gatunki)
3. Użytkownik wprowadza dane filmu
4. System sprawdza bazę danych.
5. Jeśli dane są poprawne, system proponuje wszystkie możliwe opcji filmow.
6. Uzytkownik wybiera jedna opcje i system pokazuje ten film na nowej stronie.
   ### scenariusze poboczne:
  
3a. Użytkownik rezygnuje z wyszukiwania

5a. W systemie nie ma filmu o takiej nazwie

5b. Jeśli dane są nieprawidłowe to wystapi blad "Nie istnije taki film"

### Use case - przeglądanie popularnych półek miesiąca

aktorzy: gość, zalogowany użytkownik, super użytkownik
główny scenariusz:  
1. System wyświetla listę kilku najlepszych wedlug rankingu polek miesiąca. 
2. Użytkownik wybiera jedna z tych polek.
3. System otwiera nowa strone z wybrana polka
4. System prezentuje informacje o filmach w wybranej półce.

### scenariusze poboczne:

1a. System nie wyświetla nowego rankingu półek, bo nie zostal zaktualizowany.

2a. Użytkownik rezygnuje z wybora polek.

3a. System nie może odnaleźć strony, bo właściciel usunął połkę i wyświetla komunikat o błędzie


### Use case - przeglądanie cytatu dnia

aktorzy: gość, zalogowany użytkownik, super użytkownik
główny scenariusz:

   1. System wyświetla codziennie nowy cytat dnia.
   2. Użytkownik czyta cytat dnia.
   3. Użytkownik może przejść na stronę filmu z którego był wzięty cytat.
   ### scenariusze poboczne:
   
   1a. System nie może odnaleźć cytatu, bo on nie został dodany.
   
   3a. W systemie nie ma filmu z takim cytatem i występuje błąd.
   

### Use case - przeglądanie top 10 ranking filmów

aktorzy: gość, zalogowany użytkownik, super użytkownik
główny scenariusz:  
1. System wyświetla listę 10 najlepszych wedlug rankingu filmow.
2. Użytkownik wybiera jeden z tych filmow.
3. System przekieruje Użytkownika na nowa strone
4. System prezentuje informacje o filmach w wybranej półce.
 ### scenariusze poboczne:
 
1a. System nie wyświetla nowego rankingu filmów, bo nie zostal zaaktulizowany.

2a. Użytkownik rezygnuje z wyboru filmu.

3a. System nie może odnaleźć strony, bo właściciel usunął film i wyświetla komunikat o błędzie.


### Use case - przeglądanie własnych rekomendacji

aktorzy: zalogowany użytkownik, super użytkownik
główny scenariusz:  
1. System prosi użytkownika o zaznaczenie kilka gatunków filmu, które go interesują
2. Użytkownik spełnia polecenie i zatwierdza swój wybór 
3. System przeszukuje bazę danych w poszukiwaniu filmow o danych gatunkach  
4. System wyświetla listę kilku filmow i polek najlepiej spełniających kryteria wyszukiwania użytkownika
5. Użytkownik ma możliwość ponownego wyszukania lub zobaczenia strony danego filmu z listy rekomendacji
6. Użytkownik dostaje listę rekomendowanych filmow na podstawie wprowadzonych informacji

 ### scenariusze poboczne:
 
2a. Użytkownik rezygnuje z wyboru.

2b. Użytkownik wybiera tylko jeden gatunek, ktorego nie wystarczy do rekomendacji.

4a. System nie może odnaleźć strony, bo właściciel usunął film i wyświetla komunikat o błędzie.

6a. Nie istnieją filmu spełniającego kryteria


### Use case - śledzenie aktywności znajomego

aktorzy: zalogowany użytkownik, super użytkownik
główny scenariusz:
1. Użytkownik widzi aktualna informacje o aktywnosci go znajomych.
2. Użytkownik moze ukryc aktywnosc wybranego znajomego
 
 ### scenariusze poboczne:
 
1a. Użytkownik nie widzi aktywnosci znajomego, bo jeszcze nie ma znajomych w systemie.


### Use case - dodanie cytatu dnia

aktorzy: super użytkownik
główny scenariusz:

1. System prosi użytkownika o wprowadzenie nowego cytatu dnia z dowolnego filmu.
2. System prosi o dodanie linku do tego filmu z opisem.
3. Użytkownik wpisuje wymagane dane.
4. System sprawdza poprawność wprowadzonych danych
5. System tworzy nowy cytat i umieszcza go w bazie danych.
   ### scenariusze poboczne:
   
   2a. System wyświetla błąd, bo film nie istnieje na stronie.
   
   3a. Użytkownik rezygnuje z dodania cytatu.
   
   3b.Użytkownik dodał nieprawidłowe dane.
   
   4a.System informuje użytkownika, które z wprowadzonych przez niego danych są nieprawidłowe
   
   5a.System nie wyświetla nowego cytatu, bo on nie został zaaktulizowany.
   

---

## REJESTRACJA / LOGOWANIE

Autor Poniższych: Davit Hunanyan

### Use case - rejestracja + logowanie (w dynamicznym panelu)

aktorzy: admin, super użytkownik, użytkownik, gość

główny scenariusz:

- Wylogowany użytkownik wchodzi poprzez przycyiski / hiperłącze, znajdujące się na różnych miejscach aplikacji webowej na stronę rejestraci i logowania.
- Wyświetla się panel logowania wraz z przyciskiem, pozwalającym zmienić go na panel rejestrowania.
- Użytkownik wybiera czy chce się zarejestrować czy zalogować.
- Jeżeli wybrał rejestrację to:

  - Wyświetla się panel rejestracji z wymaganymi pustymi polami do wprowadzenia:
    - Imięnia
    - Nazwiska
    - Emaila
    - Hasła
    - Potwierdzenia hasła
  - Jeżeli użytkownik przy wpisaniu danych zostawi którąś/eś pole/a puste, to wyświetli się mały popup **Warningu** przy pierwszym pustym polu, z komunikatem **'Jest to pole wymagane'**. Czynność będzie się powtarzać dopóki wszystkie pola nię będą wypełnione.
    - Jeżeli tekst wpisany w polu mailowym nie ma formatu mailwego, to wyświetli się mały popup **Warningu** przy danym polu, z komunikatem **'Dany format nie jest mailowy'**. Czynność będzie się powtarzać dopóki dane mailowe nie będą miały formatu mailowego.
    - Jeżeli istnieje inne konto z podanym przez użytkownika mailem, to wyświetli się mały popup **Erroru** przy polu z mailem z komunikatem **'Użytkownik z podanym mailem już istnieje'**. Scenariusz będzie się powtarzać, dopóki użytkownik nie wpisze taki email, którego nie ma zarejestrowanego w systemie.
    - Jeżeli potwierdzające hasło wpisane przez użytkownika nie zgadza się z pierwszym, to usuwają się obie pola i wyświetla się mały popup **Erroru** przy polu z hasłem, z komunikatem **'Hasła się nie zgadzają'**. Scenariusz się powtarza, dopóki hasła wpisane przez użytkownika nie będą takie same.
  - Jeżeli po drodze nie napotkano na żadne inne błedy, to następuje **hashowanie** (szyfrowanie) hasła oraz generowanie **tokena** z podanym czasem wygaśnięcia, po czym użytkownik automatycznie loguje się do systemu i przekierowuje go na główną stronę bez możliwości cofania się do panelu rejestracji/logowania.
  - Jeżeli natomiast napotkano na jakiekolwiek inne błędy, to wyświetla się duży popup **Erroru**, z komunikatem  
    **'Oops, coś poszło nie tak :('**.

- Jeżeli natomiast wybrał logowanie to:
  - Wyświetla się panel logowania z wymaganymi pustymi polami do wprowadzenia:
    - Emaila
    - Hasła
  - Jeżeli użytkownik przy wpisaniu danych zostawi którąś/eś pole/a puste, to wyświetli się mały popup **Warningu** przy pierwszym pustym polu, z komunikatem **'Jest to pole wymagane'**. Czynność będzie się powtarzać dopóki wszystkie pola nię będą wypełnione.
    - Jeżeli tekst wpisany w polu mailowym nie ma formatu mailwego, to wyświetli się mały popup **Warningu** przy danym polu, z komunikatem **'Dany format nie jest mailowy'**. Czynność będzie się powtarzać dopóki dane mailowe nie będą miały formatu mailowego.
    - Jeżeli nie ma w systemie konta z podanym przez użytkownika mailem, to wyświetli się mały popup **Erroru** przy polu z mailem z komunikatem **'Użytkownik z podanym mailem nie istnieje'**. Scenariusz będzie się powtarzać, dopóki użytkownik nie wpisze taki email, który jest zarejestrowy w systemie.
    - Jeżeli hasło wpisane przez użytkownika nie zgadza się z tym co jest w systemie, to usuwają się obie pola i wyświetla się mały popup **Erroru** przy polu z hasłem, z komunikatem **'Nie prawidłowe hasło lub email'**. Scenariusz się powtarza dopóki użytkownik nie wpisze takiego maila, który jest w systemie oraz dla hasło, które bedzię w bazie odpowiadać temu mailowi.
  - Jeżeli po drodze nie napotkano na żadne inne błedy, to następuje generowanie **tokena** z podanym czasem wygaśnięcia, po czym użytkownik loguje się do systemu i przekierowuje go na główną stronę bez możliwości cofania się do panelu rejestracji/logowania.
  - Jeżeli natomiast napotkano na jakiekolwiek inne błędy, to wyświetla się duży popup **Erroru**, z komunikatem  
    **'Oops, coś poszło nie tak :('**.

---

## PROFIL

Autor Poniższych: Antoni Lasoń

### Use case - Złożenie podania o status zaufanego użytkownika

Aktorzy Użytkownik

1. Wybranie opcji "złóż podanie o status zaufanego użytkownika"
2. System wysyła prośbę do rozpatrzenia administratora

### Use case - Anulowanie podania o status zaufanego użytkownika

Aktorzy: Użytkownik

1. Wybranie opcji "Anuluj podanie o status zaufanego użytkownika"

## Usuwanie własnego konta
Aktorzy: Użytkownik

1. Użytkownik wybiera opcję usuń konto
2. System wyświetla powiadomienie o konsekwencjach tej akcji
3. System wyświetla zapytanie o chęć kontynuacji usuwania konta
4. Użytkownik potwierdza chęć usunięcia konta
5. Użytkonik podaje hasło
6. Konto jest usuwane z bazy

### scenariusze poboczne:

3a. Użytkownik anuluje operacje

5a. Użytkownik podaje błędne hasło

5a1. System informuje o podaniu błędnego hasła

5a2. Spwrót do punktu 5.


### Use case - Wylogowanie

Aktorzy: urzytkownik

1. Użytkownik wybiera opcję wyloguj
2. System zmienia stan urzytkownika z zalogowanego na niezalogowanego

### Use case - Edytowanie profilu

Aktorzy: użytkownik lub super użytkownik lub Administrator

1. Użytkownik wubiera opcję edycji profilu.
2. System prezentuje użytkownikowi okna dialogowe z możliwością zmiany swoich danych
3. Użytkownik edytuje swoje dane
4. Użytkownik wybiera opcję zapisz
5. Zmiany zostają zapisane

### scenariusze poboczne:

4a. Użytkonik wybiera opcję " anuluj"

4a1. Zmiany nie zostają zapisane


### Use case - Zmiana hasła

Aktorzy: użytkownik lub super użytkownik lub Administrator

1. Użytkonik wybiera opcje zmiany hasła
2. System prosi o podanie dotychczasowego hasła
3. Użytkonik podaje hasło
4. System weryfikuje hasło jako poprawne
5. System prosi o dwukrotne podanie nowego hasła
6. Nowe hasło zostaje zaszyfrowane i zapisane w bazie

### scenariusze poboczne:

4a. System weryfikuje hasło jako błędne

4a1. Powrót do punktu 2

5a. Podane hasła są różne

5a1. Powrót do punktu 5

## Autor poniższych: Dominik Kikla

## use case: odbieranie statusu super user

aktorzy: admin, super użytkownik

główny scenariusz:

1. Admin klika "odbierz status zaufany użytkownik" w przeglądzie profilu zaufanego użytkownika.
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
3. admin wybiera opcje kontynuacji działania (zatwierdza cofanie statusu).
4. Wyślij wiadomość dot. cofnięcia statusu zaufanego użytkownika do wcześniej wybranego zaufanego użytkownika.
5. Zmień status wcześniej wybranego "zaufanego użytkownika" na "zalogowany użytkownik".

### scenariusze poboczne:

3a. admin wybiera opcję "anuluj".

## use case: Zrezygnowanie ze statusu zaufanego użytkownika

aktorzy: super użytkownik

główny scenariusz:

1. zaufany użytkownik klika w swoim profilu "zrezygnuj ze statusu zaufanego użytkownika".
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
3. zaufany użytkownik wybiera opcje kontynuacji działania (zatwierdza cofanie statusu).
4. Zmień status zaufanego użytkownika na "zalogowany użytkownik".
5. Wyświetl komunikat o sukcesie operacji.

### scenariusze poboczne:

3a. zaufany użytkownik wybiera opcję "anuluj".

## use case: zmiana adresu email

aktorzy: super użytkownik, zaufany użytkownik, zalogowany użytkownik

główny scenariusz:

1. Aktor klika w edycji swojego profilu "zmień e-mail".
2. Pokaż okno z możliwością wpisania nowego e-mail.
3. Aktor (ten co w pkt 1) wpisuje nowy e-mail.
4. Aktor klika "zatwierdź".
5. Wyślij na nowy e-mail link potwierdzający.
6. link zostaje kliknięty.
7. Przypisz do konta aktora (tego co w pkt 1) nowy, wpisany przez niego e-mail.
8. Wyswietl komunikat o powodzeniu.

### scenariusze poboczne:

3a. aktor (ten co w pkt 1) wybiera opcję "anuluj".
6a. link nie zostaje kliknięty.
6a1. Po upływie 24 godzin wyślij do aktora (tego co w pkt 1) wiadomość o niepowodzeniu zmiany e-mail.

## use case: Przyznanie statusu super user

aktorzy: admin, zalogowany użytkownik

główny scenariusz:

1. Admin w profilu zalogowanego użytkownika klika "przyznaj zaufanego użytkownika".
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
3. Admin wybiera opcje kontynuacji działania.
4. Zmień status wcześniej wybranego "zalogowany użytkownika" na "zaufany użytkownik".
5. Pokaż komunikat o sukcesie.
6. Wyślij wiadomość do zalogowanego użytkownika dot. zmiany jego uprawnień.

### scenariusze poboczne:

3a. Admin klika anuluj.

---

## PROFIL ADMINA

### Use case - odbieranie statusu super user

aktorzy: admin, super użytkownik

główny scenariusz:

1. Admin klika "odbierz status zaufany użytkownik" w przeglądzie profilu zaufanego użytkownika.
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
3. admin wybiera opcje kontynuacji działania (zatwierdza cofanie statusu).
4. Wyślij wiadomość dot. cofnięcia statusu zaufanego użytkownika do wcześniej wybranego zaufanego użytkownika.
5. Zmień status wcześniej wybranego "zaufanego użytkownika" na "zalogowany użytkownik".

scenariusze poboczne:
3a. admin wybiera opcję "anuluj".

### Use case - Zrezygnowanie ze statusu zaufanego użytkownika

aktorzy: super użytkownik

główny scenariusz:

1. zaufany użytkownik klika w swoim profilu "zrezygnuj ze statusu zaufanego użytkownika".
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
3. zaufany użytkownik wybiera opcje kontynuacji działania (zatwierdza cofanie statusu).
4. Zmień status zaufanego użytkownika na "zalogowany użytkownik".
5. Wyświetl komunikat o sukcesie operacji.

scenariusze poboczne:
3a. zaufany użytkownik wybiera opcję "anuluj".

### Use case - zmiana adresu email

aktorzy: super użytkownik, zaufany użytkownik, zalogowany użytkownik

główny scenariusz:

1. Aktor klika w edycji swojego profilu "zmień e-mail".
2. Pokaż okno z możliwością wpisania nowego e-mail.
3. Aktor (ten co w pkt 1) wpisuje nowy e-mail.
4. Aktor klika "zatwierdź".
5. Wyślij na nowy e-mail link potwierdzający.
6. link zostaje kliknięty.
7. Przypisz do konta aktora (tego co w pkt 1) nowy, wpisany przez niego e-mail.
8. Wyswietl komunikat o powodzeniu.

scenariusze poboczne:
3a. aktor (ten co w pkt 1) wybiera opcję "anuluj".
6a. link nie zostaje kliknięty.
6a1. Po upływie 24 godzin wyślij do aktora (tego co w pkt 1) wiadomość o niepowodzeniu zmiany e-mail.

### Use case - Przyznanie statusu super user

aktorzy: admin, zalogowany użytkownik

główny scenariusz:

1. Admin w profilu zalogowanego użytkownika klika "przyznaj zaufanego użytkownika".
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
3. Admin wybiera opcje kontynuacji działania.
4. Zmień status wcześniej wybranego "zalogowany użytkownika" na "zaufany użytkownik".
5. Pokaż komunikat o sukcesie.
6. Wyślij wiadomość do zalogowanego użytkownika dot. zmiany jego uprawnień.

scenariusze poboczne:
3a. Admin klika anuluj.

---

## PÓŁKA

### Use case - Usuwanie własnej półki

Aktorzy: Użytkownik

1. Użytkownik wybiera opcję "usuń półkę"
2. System wyświetla komunikat o nieodwracalnej operacji usuwania danych i prośbę o potwierdzenie wykonania operacji
3. użytkownik potwierdza chęć wykonania operacji
4. System usuwa dane o półce

### Use case - Scenariusze poboczne

3a. Uźytkownik nie potwierdza chęci wykonania operacji
3a1. Półka nie zostaje usunięta

### Use case - Skopiowanie połki innego użytkownika

Aktorzy: Użytkownik

1. użytkownik wybiera widoczną dla niego pułkę innego użytkownika
2. Użytkownik wybiera opcję "kopiuj półkę"
3. Informacje o półce i zawartości zostają skopiowane i przypisane do konta Użytkownika.

### Use case - Zmienianie widoczności półki

Aktorzy: Użytkownik

1. Użytkownik wybiera opcję zmiany widoczności półki
2. System wyświetla okno dialogowe z możliwością wyboru nowych opcji widoczności
3. Użytkownik wybiera nowe opcje widoczności
4. Użytkownik naciska przycisk "zapisz"
5. System stosuje nowe opcje widoczności

### Use case - Scenariusze poboczne

4a. Użytkownik naciska przyciks "anuluj"
4a1. Ustawienia widoczności nie zostają zmienione

### Use case - Dodawanie filmu do półki

Aktorzy: Użytkownik

1. Użytkownik wybiera film
2. Użytkownik wybiera dodaj do półki
3. System presentuje okno dialogowe z listą pułek użytkownika
4. Użytkownik wybiera półkę
5. System dodaje książkę do półki

### Use case - Scenariusze poboczne

3a. Uźytkownik wybiera utwóż nową półkę
3a1. System wyświetla okno dialogowe z prośbą o podanie nazwy nowej półki oraz ustawieniami widoczności
3a2. Użytkownik wprowadza nazwę i ustawienia widoczności
3a3. uzytkownik wybiera opcję utwórz nową półke
3a4. Pułka zostaje utworzona a system dodaje do wybrany film.
3a3a. Użytkownik wybiera opcję anuluj
3a3a1. Proces zostaje przerwany

### Use case - Usuwanie z półki

Aktorzy: Użytkownik

1. Użytkownik wybiera film
2. Użytkownik wybiera opcję "usuń z półki"
3. System usuwa informacje o przypisaniu filmu do półki

### Use case - Przeglądanie publicznych półek

Aktorzy: Gość, zalogoway użytkownik, zaufany użytkownik, admin

1. Aktor klika w "przeglądaj półkę" w profilu użytkownika.
2. Pokaż zawartość półki aktorowi.

scenariusze poboczne:
2a. Półka danego użytkownika nie jest dostępna.
2a1. Wyświetl komunikat o niepowodzeniu.

### Use case - Usuwanie półki

Aktorzy: Admin

1. Admin klika w "usuń półkę" w przeglądzie półek.
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
3. Admin wybiera opcje kontynuacji działania.
4. Usuń wybraną półkę z systemu.
5. Wyświetl komunikat o powodzeniu.

scenariusze poboczn:
3a. Admin wybiera "anuluj".

### Use case - Tworzenie półki

Aktorzy: Zalogowany użytkownik, zaufany użytkownik.

1. Aktor klika "dodaj półkę" w swoim przeglądzie półek.
2. Wyświetl formularz do tworzenia nowej półki z polami "widoczność", "nazwa", "filmy".
3. Aktor wypełnia wszystkie pola.
4. Aktor klika "zatwierdź".
5. Utwórz nową półkę przypisaną do tego użytkownika.
6. Wyświetl komunikat o powodzeniu.

scenariusze poboczne:
3a. Użytkownik nie wypełnił wszystkich pól.
3a1. Użytkownik klika "zatwierdź".
3a2. Wyświetl komunikat o konieczności wypełnieniu wszystkich pól. idź do 2.

Autor 3 ostatnich: Dominik Kikla
Autor reszty: Antoni Lasoń

use case: dodawanie znajomego
aktorzy: zalogowany użytkownik,
super użytkownik

główny scenariusz:
1.dowolny z aktorów klika przycisk
"dodaj znajomego" w swoim profilu 2. Umożliwij wpisaniu nazwy użytkownika 3. Wyszukaj w systemie użytkownika o takiej nazwie. 4. Powiadom użytkownika o podanej nazwie, że ma zaproszenie do znajomych.
5a1. Użytkownik akceptuje zaproszenie
5b1. Użytkownik odrzuca zaproszenie
5a2. Użytkownicy zostają umieszczenie nawzajem na swoich listach znajomych.
5b2. Użytkownik wysyłający zaproszenie dostaje komunikat o odrzuceniu zaproszenia.
5a3. Użytkownik wysyłający zaproszenie dostaje komunikat o zaakceptowaniu zaproszenia.

scenariusze poboczne:
3a. W systemie nie ma użytkownika o takiej nazwie
3a1. Wyświetl komunikat dot. nieistniejącego użytkownika

---

## ZNAJOMI

### Use case - usunięcie znajomego

aktorzy: zalogowany użytkownik,
super użytkownik

główny scenariusz:
1. dowolny z aktorów klika przycisk
"usuń znajomego" w przeglądzie listy swoich znajomych. 
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania). 
3. Użytkownik wybiera opcje kontynuacji działania (zatwierdza usuwanie). 
4. Usuwany użytkownik z listy znajomych i usuwający znikają nawzajem ze swoich list znajomych.

scenariusze poboczne:

### Use case - wysłanie wiadomości do innego usera

aktorzy: zalogowany użytkownik,
super użytkownik

główny scenariusz:
1.  Dowolny z aktorów klika przycisk "wyślij wiadomość" w przeglądzie profilu wybranego użytkownika lub w panelu "moje konwersacje" wybiera użytkownika klikając na niego. 
2. Pokaż użytkownikowi okno, w którym może wpisać wiadomość. 
3. Użytkownik wpisuje wiadomość i klika "wyślij".
4. Wyślij wybranemu wcześniej użytkowniku wiadomość. 
5. Powiadom otrzymującego, że dostał nową wiadomość.
6. Otrzymujący klika w powiadomienie.
7. Pokaż otrzymującemu wiadomość, która do niego przyszła i miejsce do odpowiedzenia na nią.
8. Odpowiadający pisze wiadomość i potem klika "odpowiedz". idź do punktu 4.

### scenariusze poboczne:

3a. Użytkownik klika "anuluj".

6a. Otrzymujący klika w "moje konwersacje".

6a1. Otrzymujący klika w wybranego użytkownika. idź do punktu 2.


### Use case - usuwanie konta

aktorzy: admin

główny scenariusz:
1. Admin wchodzi w profil użytkownika i klika "usuń konto". 
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania). 
3. Admin wybiera opcje kontynuacji działania (zatwierdza usuwanie). 
4. Wyślij wiadomość dot. usunięcia konta na adres e-mail usuwanego konta. 
5. Usuń konto z systemu.

### scenariusze poboczne:

3a. admin wybiera opcję "anuluj".

### Use case - Wysłanie ostrzerzenia o naruszeniu regulaminu

aktorzy: admin, zalogowany użytkownik, super użytkownik

główny scenariusz:
1. Admin klika w profil użytkownika i klika "wyślij ostrzeżenie".
2. Pokaż adminowi okno, w którym może wybrać powód ostrzeżenia i wpisać opcjonalny komentarz.
3. Admin wybiera powód ostrzeżenia oraz wpisuje komentarz.
4. Admin klika "wyślij". 
5. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania).
6.  Admin wybiera opcje kontynuacji działania (zatwierdza wysyłanie ostrzeżenia). 
7.  Uzględnij to ostrzeżenie w systemie. 
8.  Wyślij do użytkownika wiadomość o ostrzeżeniu zawierającą wybrany powód i komentarz.

### scenariusze poboczne:

3a. Admin klika "anuluj".

6a. Admin klika "anuluj". idź do 2.

### Use case - Cofnięcie ostrzerzenia o naruszeniu regulaminu

aktorzy: admin, zalogowany użytkownik, super użytkownik

główny scenariusz:
1. Admin klika w menu "wysłane ostrzeżenia".
2. Pokaż listę wysłanych ostrzeżeń.
3. Admin klika przy wybranym ostrzeżeniu w "cofnij ostrzeżenie". 
4. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania). 
5. Admin wybiera opcje kontynuacji działania (zatwierdza cofanie ostrzeżenia). 
6. Uzględnij to cofnięcie ostrzeżenia w systemie.
7. Wyślij do użytkownika wiadomość o cofnięciu ostrzeżenia zawierającą wybrany powód i komentarz.

### scenariusze poboczne:

5a. Admin klika "anuluj".

### Use case - blokowanie konta

aktorzy: admin

główny scenariusz:
1. Admin wchodzi w profil użytkownika i klika "zablokuj konto".
2. Wyświetlenie monitu dot. potwierdzenia czynności (z opcją kontynuacji lub przerwania działania). 
3. Admin wybiera opcje kontynuacji działania (zatwierdza blokowanie). 
4. Wyślij wiadomość dot. zablokowania konta na adres e-mail blokowanego konta.
5. Zablokuj konto z systemu (uniemożliwij wykonywanie czynności inne niż dostępne niezalogowanemu użytkownikowi).

### scenariusze poboczne:

3a. admin wybiera opcję "anuluj".

autor: Dominik Kikla

---

### Use case - Edycja filmu

Dodawanie opinii o wybranym filmie
Aktorzy: zalogowany użytkownik lub super użytkownik

1. Użytkownik wybiera funkcję dodaj opis
2. Użytkownik wpisuje opis filmu w polu tekstowym
3. Użytkownik naciska przycisk „opublikuj”
4. System sprawdza obecność wulgarnych lub nieodpowiednich słów
5. Opinia jest zapisywana na serwerze

scenariusze poboczne:
3a) Użytkownik naciska przycisk anuluj, opinia nie jest publikowana
4a) System informuje o wystąpieniu niedozwolonych słów, opinia nie jest zapisywana

### Use case - Wycofanie oceny filmu

Aktorzy: zalogowany użytkownik lub super użytkownik

1. Użytkownik wybiera wystawioną wcześniej ocenę
2. Użytkownik wybiera opcję usuń
3. Użytkownik potwierdza chęć usunięcia oceny
4. Ocena zostaje usunięta

Scenariusze poboczne
3a) Użytkownik nie potwierdza chęci usunięcia oceny, ocena nie jest usuwana

### Use case - Usunięcie własnej opinii o wybranym filmie

Aktorzy: zalogowany użytkownik lub super użytkownik

1. Użytkownik wybiera swoją opinie
2. Użytkownik wybiera opcję usuń
3. Użytkownik potwierdza chęć usunięcia opinii
4. Opinia zostaje usunięta

Scenariusze poboczne
3a) Użytkownik nie potwierdza chęci usunięcia opinii, okpienia nie jest usuwana

### Use case - Dodawanie do półki ulubionych

Aktorzy: zalogowany użytkownik lub super użytkownik

1. Użytkownik wybiera film
2. Użytkownik wybiera opcję „dodaj do ulubionych”
3. Film zostaje dodany do pułki ulubionych danego użytkownika

### Use case - Edytowanie własnego komentarza

Aktorzy: zalogowany użytkownik lub super użytkownik

1. Użytkownik wybiera napisany przez siebie komentarz
2. Użytkownik wybiera opcję „edytuj”
3. System wyświetla edytowalne pole tekstowe z aktualną treścią komentarza
4. Użytkownik wprowadza zmiany w treści
5. Użytkownik wybiera opcję zapisz
6. Zmiany zostają zapisane

### scenariusze poboczne:

5a) Użytkownik wybiera opcję odrzuć zmiany

5a1)Zmiany nie zostają zapisane

### Use case - Dodawanie oceny filmu

Aktorzy: zalogowany użytkownik lub super użytkownik

1. Użytkownik wybiera opcję dodaj ocenę
2. Użytkownik wybiera ocenę ze skali
3. Ocena zostaje zapisana

### Use case - Przeglądanie treści powiązanych z filmem

Aktorzy: zalogowany użytkownik lub gość

1. Użytkownik otwiera stronę filmu
2. System prezentuje informacje o filmie, średnią ocen, pozycję w rankingu, najnowsze opinie użytkowników oraz zwiastuny

### Use case - Przeglądanie zwiastunów

Aktorzy: zalogowany użytkownik lub gość

1. Użytkownik wybiera zwiastun do odtworzenia
2. System przekierowuje użytkownika na stronę serwisu streamingowi z danym zwiastunem

Scenariusze poboczne
2a) System nie może odnaleźć strony i wyświetla komunikat o błędzie

### Use case - Usuwanie filmów

Aktorzy: Administrator

1. Administrator wybiera film do usunięcia
2. System prezentuje Administratorowi informacje o filmie oraz opcje „usuń” lub „anuluj”
3. Administrator wybiera opcje usunięcia filmu
4. System usuwa film z bazy

Scenariusze poboczne
3a) Administrator wybiera opcję „anuluj”
3ai) Film nie jest usuwany

### Use case - Edytowanie opisu filmu

Aktorzy: Administrator lub super użytkownik

1. Osoba uprawniona wybiera opcję edycji opisu filmu
2. System wyświetla edytowalne pole tekstowe z dotychczasowym opisem filmu
3. Osoba uprawniona wprowadza zmiany w opisie
4. Edytor wybiera opcje „zapisz”
   a. Edytor wybiera opcje „nie zapisuj”
   i. Zmiany nie są zapisywane
5. Zmiany zostają zapisane

### Use case - Edytowanie komentarzy przy cenzurze

Aktorzy: Administrator lub super użytkownik

1. System sprawdza poprawność napisanych komentarzy w programie. 
2. Aktor wybiera komentarz potrzebujący edycji.
3. Aktor wybiera opcję „edytuj”
4. Aktor wprowadza zmiany w treści.
5. Aktor wybiera opcję zapisz i system zostaje zaaktulizowany.

 Scenariusze poboczne: 
5a. Zmiany nie zostają zapisane
Autor: Kamila Baizakova

### Use case - Usuwanie komentarzy

Aktorzy: Administrator lub super użytkownik

1. Administrator wybiera komentarz
2. System prezentuje treść komentarza oraz dane autora
3. Administrator wybiera opcję „usuń”
   a. Administrator wybiera opcję anuluj
   i. Komentarz nie zostaje usunięty
4. Komentarz zostaje usunięty z bazy

### Use case - Dodawanie zwiastun filmu

Aktorzy: Administrator lub super użytkownik

1. Administrator wybiera film
2. Administrator wybiera opcję dodania zwiastuny
3. System wyświetla okno dialogowe z możliwością wprowadzenia linku do zwiastun
4. System sprawdza poprawność linku
5. Zwiastun zostaje dodany na podstawie linku

Antoni Lasoń
