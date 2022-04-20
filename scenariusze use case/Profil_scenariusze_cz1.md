# Use Case: Profil


## Autor Poniższych: Antoni Lasoń

## Złożenie podania o status zaufanego użytkownika
Aktorzy Użytkownik
1. Wybranie opcji "złóż podanie o status zaufanego użytkownika"
2. System wysyła prośbę do rozpatrzenia administratora


## Anulowanie podania o status zaufanego użytkownika
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

### scenariusze poboczne
3a. Użytkownik anuluje operacje
5a. Użytkownik podaje błędne hasło
5a1. System informuje o podaniu błędnego hasła
5a2. Spwrót do punktu 5.

## Wylogowanie
Aktorzy: urzytkownik
1. Użytkownik wybiera opcję wyloguj
2. System zmienia stan urzytkownika z zalogowanego na niezalogowanego

## Edytowanie profilu
Aktorzy: użytkownik lub super użytkownik lub Administrator
1. Użytkownik wubiera opcję edycji profilu.
2. System prezentuje użytkownikowi okna dialogowe z możliwością zmiany swoich danych
3. Użytkownik edytuje swoje dane
4. Użytkownik wybiera opcję zapisz
5. Zmiany zostają zapisane

### Scenariusze poboczne
4a. Użytkonik wybiera opcję " anuluj" 
4a1. Zmiany nie zostają zapisane 

## Zmiana hasła 
Aktorzy: użytkownik lub super użytkownik lub Administrator
1. Użytkonik wybiera opcje zmiany hasła
2. System prosi o podanie dotychczasowego hasła 
3. Użytkonik podaje hasło
4. System weryfikuje hasło jako poprawne
5. System prosi o dwukrotne podanie nowego hasła 
6. Nowe hasło zostaje zaszyfrowane i zapisane w bazie 

### Scenariusze poboczne
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

