# news_app

Tu należy dodać opis aplikacji, który będzie modyfikowany w miarę postępów.

inteliJ: git clone
1. Uruchom IntelliJ IDEA:
- Otwórz IntelliJ IDEA. Jeśli nie masz otwartego żadnego projektu, zobaczysz ekran powitalny.
2. Wybierz opcję Klonowania Repozytorium:
- Na ekranie startowym wybierz Get from Version Control.
- Jeśli masz już otwarty projekt, wybierz File > New > Project from Version Control.
3. Wprowadź Adres URL Repozytorium:
- W oknie dialogowym, które się pojawi, znajdziesz pole do wpisania adresu URL repozytorium Git.
- Wklej tam URL repozytorium, które chcesz sklonować.
4. Określ Lokalizację na Dysku:
- Wybierz lokalizację na swoim komputerze, gdzie chcesz sklonować repozytorium. Możesz to zrobić, klikając na ikonę folderu obok pola „Directory” i wybierając odpowiednią ścieżkę.
5. Klonowanie Repozytorium:
- Kliknij Clone. Jeśli repozytorium jest prywatne lub wymaga uwierzytelnienia, IntelliJ poprosi Cię o dane logowania.
6. Otwarcie Projektu:
- Po zakończeniu procesu klonowania, IntelliJ zaproponuje otwarcie projektu. Wybierz opcję otwarcia, a IntelliJ załaduje projekt.
7. Konfiguracja Projektu:
- IntelliJ może automatycznie wykryć konfigurację projektu (np. pliki Maven, Gradle) i zaoferować ich zaimportowanie. Postępuj zgodnie z instrukcjami IntelliJ, aby skonfigurować projekt.
8. Gotowe:
- Po zakończeniu tych kroków, masz już sklonowane repozytorium w IntelliJ IDEA, gotowe do pracy.


Komunikat błędu "Push failed remote: Permission to gitRepoOwner/news_app.git denied to gitUser. unable to access 'https://github.com/gitRepoOwner/news_app.git/': The requested URL returned error: 403" wskazuje, że masz problem z uprawnieniami podczas próby wykonania operacji push na repozytorium Git. Oto kilka kroków, które możesz podjąć, aby rozwiązać ten problem:

Sprawdź swoje Uprawnienia na Repozytorium:

Upewnij się, że masz odpowiednie uprawnienia do repozytorium na GitHub. Aby móc wysyłać zmiany (push), musisz być albo właścicielem repozytorium, albo zostać dodanym jako współpracownik (collaborator) z odpowiednimi uprawnieniami.
Sprawdź Ustawienia Autentykacji:

Upewnij się, że jesteś prawidłowo uwierzytelniony. Od sierpnia 2021 roku, GitHub wymaga korzystania z tokenów dostępu osobistego (Personal Access Token - PAT) zamiast tradycyjnych haseł do operacji Git na HTTPS.
Sprawdź, czy używasz tokena dostępu osobistego jako hasła, gdy wykonujesz operację push.
Utwórz i Skonfiguruj Personal Access Token:

Jeśli nie masz jeszcze tokena, możesz go utworzyć w ustawieniach swojego konta GitHub w sekcji "Developer settings".
Podczas tworzenia tokena, upewnij się, że nadałeś mu odpowiednie uprawnienia (scopes), takie jak repo, które są potrzebne do operacji na repozytoriach.
Sprawdź Konfigurację Git:

Sprawdź, czy Twoja konfiguracja Git jest poprawna. Możesz to zrobić, używając polecenia git config --list i sprawdzając, czy Twój użytkownik i email są prawidłowo skonfigurowane.
Aktualizuj Poświadczenia:

Jeśli wcześniej korzystałeś z hasła, a teraz masz token dostępu osobistego, być może będziesz musiał zaktualizować swoje poświadczenia w menedżerze poświadczeń systemu lub w cache Git.
Wykonaj Ponownie Push:

Po skonfigurowaniu tokena dostępu i upewnieniu się, że masz odpowiednie uprawnienia, spróbuj ponownie wykonać operację push.
Sprawdź Konfigurację Remote URL:

Sprawdź, czy adres URL zdalnego repozytorium (remote URL) jest poprawny. Możesz to zrobić za pomocą git remote -v.