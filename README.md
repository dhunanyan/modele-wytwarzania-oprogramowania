# SCENARIUSZE USE CASE-ÓW

---

## STRONA GŁÓWNA

### Use case - wyszukiwanie filmów

aktorzy: gość, zalogowany użytkownik, super użytkownik
główny scenariusz:

1. Dowolny z aktorów klika przycisk "wyszukiwanie filmów" na stronie głównej
2. System prosi użytkownika o wprowadzenie informacji o filmie (nazwa,rezyser, tytuł, opis, gatunki)
3. Użytkownik wprowadza dane filmu
4. System sprawdza bazę danych.
5. Jeśli dane są poprawne, system proponuje wszystkie możliwe opcji filmow.
6. Uzytkownik wybiera jedna opcje i system pokazuje ten film na nowej stronie.
   scenariusze poboczne:
   3a. Użytkownik rezygnuje z wyszukiwania
   5a. W systemie nie ma filmu o takiej nazwie
   5b. Jeśli dane są nieprawidłowe to wystapi blad "Nie istnije taki film"

### Use case - przeglądanie popularnych półek miesiąca

aktorzy: gość, zalogowany użytkownik, super użytkownik
główny scenariusz:  
1.System wyświetla listę kilku najlepszych wedlug rankingu polek miesiąca. 2. Użytkownik wybiera jedna z tych polek.
3.System otwiera nowa strone z wybrana polka 4. System prezentuje informacje o filmach w wybranej półce.
Scenariusze poboczne:
1a. System nie wyświetla nowego rankingu półek, bo nie zostal zaktualizowany.
2a. Użytkownik rezygnuje z wybora polek.
3a. System nie może odnaleźć strony, bo właściciel usunął połkę i wyświetla komunikat o błędzie

### Use case - przeglądanie cytatu dnia

aktorzy: gość, zalogowany użytkownik, super użytkownik
główny scenariusz:

1. System wyświetla codziennie nowy cytat dnia.
   2.Użytkownik czyta cytat dnia.
   3.Użytkownik może przejść na stronę filmu z którego był wzięty cytat.
   Scenariusze poboczne:
   1a.System nie może odnaleźć cytatu, bo on nie został dodany.
   3a. W systemie nie ma filmu z takim cytatem i występuje błąd.

### Use case - przeglądanie top 10 ranking filmów

aktorzy: gość, zalogowany użytkownik, super użytkownik
główny scenariusz:  
1.System wyświetla listę 10 najlepszych wedlug rankingu filmow. 2. Użytkownik wybiera jeden z tych filmow.
3.System przekieruje Użytkownika na nowa strone 4. System prezentuje informacje o filmach w wybranej półce.
Scenariusze poboczne:
1a. System nie wyświetla nowego rankingu filmów, bo nie zostal zaaktulizowany.
2a. Użytkownik rezygnuje z wyboru filmu.
3a. System nie może odnaleźć strony, bo właściciel usunął film i wyświetla komunikat o błędzie.

### Use case - przeglądanie własnych rekomendacji

aktorzy: zalogowany użytkownik, super użytkownik
główny scenariusz:  
1.System prosi użytkownika o zaznaczenie kilka gatunków filmu, które go interesują 2. Użytkownik spełnia polecenie i zatwierdza swój wybór 3. System przeszukuje bazę danych w poszukiwaniu filmow o danych gatunkach  
4. System wyświetla listę kilku filmow i polek najlepiej spełniających kryteria wyszukiwania użytkownika
5.Użytkownik ma możliwość ponownego wyszukania lub zobaczenia strony danego filmu z listy rekomendacji
6.Użytkownik dostaje listę rekomendowanych filmow na podstawie wprowadzonych informacji

Scenariusze poboczne:
2a.Użytkownik rezygnuje z wyboru.
2b. Użytkownik wybiera tylko jeden gatunek, ktorego nie wystarczy do rekomendacji.
4a. System nie może odnaleźć strony, bo właściciel usunął film i wyświetla komunikat o błędzie.
6a.Nie istnieją filmu spełniającego kryteria

### Use case - śledzenie aktywności znajomego

aktorzy: zalogowany użytkownik, super użytkownik
główny scenariusz:
1)Użytkownik widzi aktualna informacje o aktywnosci go znajomych.
2)Użytkownik moze ukryc aktywnosc wybranego znajomego
Scenariusze poboczne
1a.Użytkownik nie widzi aktywnosci znajomego, bo jeszcze nie ma znajomych w systemie.

### Use case - dodanie cytatu dnia

aktorzy: super użytkownik
główny scenariusz:

1. System prosi użytkownika o wprowadzenie nowego cytatu dnia z dowolnego filmu.
2. System prosi o dodanie linku do tego filmu z opisem.
3. Użytkownik wpisuje wymagane dane.
4. System sprawdza poprawność wprowadzonych danych
5. System tworzy nowy cytat i umieszcza go w bazie danych.
   Scenariusze poboczne:
   2a. System wyświetla błąd, bo film nie istnieje na stronie.
   3a. Użytkownik rezygnuje z dodania cytatu.
   3b.Użytkownik dodał nieprawidłowe dane.
   4a.System informuje użytkownika, które z wprowadzonych przez niego danych są nieprawidłowe
   5a.System nie wyświetla nowego cytatu, bo on nie został zaaktulizowany.

---

## REJESTRACJA / LOGOWANIE

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

### Use case - Złożenie podania o status zaufanego użytkownika

Aktorzy Użytkownik

1. Wybranie opcji "złóż podanie o status zaufanego użytkownika"
2. System wysyła prośbę do rozpatrzenia administratora

### Use case - Anulowanie podania o status zaufanego użytkownika

Aktorzy: Użytkownik

1. Wybranie opcji "Anuluj podanie o status zaufanego użytkownika"

##Usuwanie własnego konta
Aktorzy: Użytkownik

1. Użytkownik wybiera opcję usuń konto
2. System wyświetla powiadomienie o konsekwencjach tej akcji
3. System wyświetla zapytanie o chęć kontynuacji usuwania konta
4. Użytkownik potwierdza chęć usunięcia konta
5. Użytkonik podaje hasło
6. Konto jest usuwane z bazy

scenariusze poboczne:
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

scenariusze poboczne
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

scenariusze poboczne
4a. System weryfikuje hasło jako błędne
4a1. Powrót do punktu 2
5a. Podane hasła są różne
5a1. Powrót do punktu 5

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
