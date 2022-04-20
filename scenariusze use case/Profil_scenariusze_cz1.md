# Use Case: Profil


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

