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
    - Jeżeli tekst wpisany w polu mailowym nie ma formatu mailwego, to wyświetli się mały popup **Warningu** przy danym polu, z komunikatem **'Dany format nie jest mailowy'**. Czynność będzie się powtarzać dopóki dane mailowe nie będą miały formatu mailowego.
    - Jeżeli istnieje inne konto z podanym przez użytkownika mailem, to wyświetli się mały popup **Erroru** przy polu z mailem z komunikatem **'Użytkownik z podanym mailem już istnieje'**. Scenariusz będzie się powtarzać, dopóki użytkownik nie wpisze taki email, którego nie ma zarejestrowanego w systemie.
    - Jeżeli potwierdzające hasło wpisane przez użytkownika nie zgadza się z pierwszym, to usuwają się obie pola i wyświetla się mały popup **Erroru** przy polu z hasłem, z komunikatem **'Hasła się nie zgadzają'**. Scenariusz się powtarza, dopóki hasła wpisane przez użytkownika nie będą takie same.
  - Jeżeli po drodze nie napotkano na żadne inne błedy, to następuje **hashowanie** (szyfrowanie) hasła oraz generowanie **tokena** z podanym czasem wygaśnięcia, po czym użytkownik automatycznie loguje się do systemu i przekierowuje go na główną stronę bez możliwości cofania się do panelu rejestracji/logowania.
  - Jeżeli natomiast napotkano na jakiekolwiek inne błędy, to wyświetla się duży popup **Erroru**, z komunikatem **Oops, coś poszło nie tak :(**.

- Jeżeli natomiast wybrał logowanie to:
  - Wyświetla się panel logowania z wymaganymi pustymi polami do wprowadzenia:
    - Emaila
    - Hasła
  - Jeżeli użytkownik przy wpisaniu danych zostawi którąś/eś pole/a puste, to wyświetli się mały popup **Warningu** przy pierwszym pustym polu, z komunikatem **'Jest to pole wymagane'**. Czynność będzie się powtarzać dopóki wszystkie pola nię będą wypełnione.
    - Jeżeli tekst wpisany w polu mailowym nie ma formatu mailwego, to wyświetli się mały popup **Warningu** przy danym polu, z komunikatem **'Dany format nie jest mailowy'**. Czynność będzie się powtarzać dopóki dane mailowe nie będą miały formatu mailowego.
    - Jeżeli nie ma w systemie konta z podanym przez użytkownika mailem, to wyświetli się mały popup **Erroru** przy polu z mailem z komunikatem **'Użytkownik z podanym mailem nie istnieje'**. Scenariusz będzie się powtarzać, dopóki użytkownik nie wpisze taki email, który jest zarejestrowy w systemie.
    - Jeżeli hasło wpisane przez użytkownika nie zgadza się z tym co jest w systemie, to usuwają się obie pola i wyświetla się mały popup **Erroru** przy polu z hasłem, z komunikatem **'Nie prawidłowe hasło lub email'**. Scenariusz się powtarza dopóki użytkownik nie wpisze takiego maila, który jest w systemie oraz dla hasło, które bedzię w bazie odpowiadać temu mailowi.
  - Jeżeli po drodze nie napotkano na żadne inne błedy, to następuje generowanie **tokena** z podanym czasem wygaśnięcia, po czym użytkownik loguje się do systemu i przekierowuje go na główną stronę bez możliwości cofania się do panelu rejestracji/logowania.
  - Jeżeli natomiast napotkano na jakiekolwiek inne błędy, to wyświetla się duży popup **Erroru**, z komunikatem **Oops, coś poszło nie tak :(**.
