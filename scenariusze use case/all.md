# SCENARIUSZE

## REJESTRACJA

### USER:

- Użytkownik wpisuje dane do rejestracji (firstName, lastName, email, password, confirmPassword).

### FRONTEND:

- Za pomocą **POST-u** wysyła wprowadzone dane przez użytkownika do Backendu na API, u którego **baseURL** może być np: **_http://localhost:5000_**, natomiast dalsza ścieżka **_"/account/signup"_** (która była już wcześniej skonfigurowana w routes-ach), po czym dostaje **response-a** z Backendu.

### BACKEND:

- Jako pierwszy krok pobiera z **ciała request-a** wszystkie wprowadzone dane.

- Jako drugi krok sprawdza czy istnieje już w bazie użytkownik z wporwadzonym e-mailem:

  - > Jeżeli nie istnieje przechodzi do kroku trzeciego.
  - > Jeżeli istnieje, to zwraca Frontendowi **response ze statusem 400 i z wiadomością 'User already exists.'**.

- Jako trzeci krok sprawdza czy **password** i **confirmPassword** są takie same (hasło i potwierdzenie hasła)

  - > Jeżeli są takie same przechodzi do kroku czwartego.
  - > Jeżeli się różnią, zwraca Frontendowi **response ze statusem 401 i z wiadomością 'Passwords don't match.'**.

- Jako czwarty krok sprawdza moc hasła, upewniając się, że występują w nim w sumie 12 znaków, w tym przynajmniej 2 liczby i 1 wielka litera

  - > Jeżeli występują przechodzi do kroku piątego.
  - > Jeżeli nie występuje, zwraca Frontendowi **response ze statusem 401 i z wiadomością 'Your password is too weak.'**.

- Jako piąty krok **Hash-uje** hasło, aby dane uzytkownika były bezpieczne, jeśli ktoś się włamie do bazy.

- Jako szósty krok tworzy **Model** zwracania danych Frontendowi.

- Jako siódmy krok tworzy **Token** z emailem pobranym z **Modelu**, **Secret-em** i z **datą wygaśnięcia** (aby użytkownik nie miał nieskończonej sesji, tylko żeby musiał wydłużać go np: co 1h).

- W przypadku **Suckesu** Backend wysyła Frontendowi **response ze statusem 201, w którym się znajduje Model i Token**

- W przypadku **Niepowodzenia** Backend wysyła Frontendowi **response ze statusem 500 oraz wiadomość 'Something went wrong.'**

### FRONTEND:

- **Response**, o którym wspomniano przed sekcją **BACKENDU**, to jest właśnie ten z **Modelem** i **Tokenem** LUB odpowiedni **Error** wraz ze swoim **statusem**.
  - Jeżeli jest to komunikat z błedem, to Frontend wyświetla go w popupie, pokazująć **USEROWI**, że coś poszło nie tak.
  - Jeżeli otrzymaliśmy natomiast pozytywną odpowiedź z Backendu, to wyświetlamy informacje danych użytkownika w **Menu** oraz w **Profilu** użytkownika

Davit Hunanyan
