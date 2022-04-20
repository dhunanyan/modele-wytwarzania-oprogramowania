## REJESTRACJA / LOGOWANIE

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
    - Jeżeli tekst wpisany w polu mailowym nie ma formatu mailwego, to wyświetli się mały popup **Warningu** przy danym polu, z komunikatem **'Dany format nie jest mailowy'**. Czynność będzie się powtarzać dopóki wszystkie pola nię będą wypełnione.
    - Jeżeli istnieje inne konto z podanym przez użytkownika mailem, to wyświetli się mały popup **Erroru** przy polu z mailem z komunikatem **'Użytkownik z podanym mailem już istnieje'**. Scenariusz będzie się powtarzać, dopóki użytkownik nie wpisze taki Email, którego nie ma zarejestrowanego w systemie.
    - Jeżeli potwierdzające hasło wpisane przez użytkownika nie zgadza się z pierwszym, to usuwają się obie pola i wyświetla się mały popup **Rrroru** przy polu z hasłem, z komunikatem **'Hasła się nie zgadzają'**. Scenariusz się powtarza, dopóki hasła wpisane przez użytkownika nie będą takie same.
    - Jeżeli hasła się zgadzają
