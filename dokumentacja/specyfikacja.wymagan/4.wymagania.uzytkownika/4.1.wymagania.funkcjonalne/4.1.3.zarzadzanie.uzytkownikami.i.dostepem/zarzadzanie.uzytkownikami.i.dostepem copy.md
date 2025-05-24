#### Diagram

:[Diagram](diagram.puml)

#### Przypadki użycia

#### UC0021 Logowanie do systemu
**nazwa:** Logowanie do systemu

**aktorzy:** Użytkownik systemu, System
**opis:**
System umożliwia użytkownikowi zalogowanie się do aplikacji za pomocą poprawnych danych uwierzytelniających (login i hasło). Proces logowania obejmuje weryfikację danych użytkownika oraz przyznanie dostępu do systemu w przypadku poprawnej autoryzacji.

**kroki:**

1. **Użytkownik systemu** wprowadza login i hasło w odpowiednich polach formularza.
1. **Użytkownik systemu** zatwierdza logowanie.
1. **System** weryfikuje poprawność wprowadzonych danych uwierzytelniających.
1. **System** sprawdza, czy konto użytkownika jest aktywne.
1. **System** przyznaje dostęp do systemu i przekierowuje użytkownika na stronę główną.


**alt 1 Niepoprawne dane uwierzytelniające:**
1. **System** wykrywa, że wprowadzone dane uwierzytelniające są niepoprawne.
1. **System** wyświetla komunikat o błędzie i prosi użytkownika o ponowne wprowadzenie danych.

**alt 2 Konto zablokowane:**
1. **System** wykrywa, że konto użytkownika zostało zablokowane (np. z powodu zbyt wielu nieudanych prób logowania).
1. **System** wyświetla komunikat informujący o blokadzie konta i sugeruje kontakt z administratorem.


#### UC0022 Zmiana hasła użytkownika
**nazwa:** Zmiana hasła użytkownika

**aktorzy:** Użytkownik systemu, System  
**opis:**  
System umożliwia użytkownikowi zmianę hasła na nowe. Proces obejmuje weryfikację starego hasła, wprowadzenie nowego hasła oraz jego zapisanie w systemie.  

**kroki:**  
1. **Użytkownik systemu** przechodzi do sekcji zmiany hasła.  
2. **Użytkownik systemu** wprowadza aktualne hasło w odpowiednim polu.  
3. **Użytkownik systemu** wprowadza nowe hasło.
4. **Użytkownik systemu** zatwierdza zmianę hasła.
5. **System** weryfikuje poprawność aktualnego hasła.  
6. **System** sprawdza zgodność nowego hasła z zasadami bezpieczeństwa.
7. **System** zapisuje nowe hasło i wyświetla komunikat o pomyślnej zmianie hasła.  

**alt 1 Niepoprawne aktualne hasło:**
1. **System** wykrywa, że wprowadzone aktualne hasło jest niepoprawne.  
2. **System** wyświetla komunikat o błędzie i prosi użytkownika o ponowne wprowadzenie aktualnego hasła.  

**alt 2 Nowe hasło nie spełnia wymagań bezpieczeństwa:**
1. **System** wykrywa, że nowe hasło nie spełnia wymagań bezpieczeństwa.
2. **System** wyświetla komunikat z prośbą o wprowadzenie nowego hasła zgodnego z zasadami bezpieczeństwa.  


#### UC0023 Dodanie użytkownika
**nazwa:** Dodanie użytkownika

**aktorzy:** Administrator systemu, System  
**opis:**  
System umożliwia administratorowi dodanie nowego użytkownika do systemu. Proces obejmuje wprowadzenie danych użytkownika, przypisanie odpowiednich ról oraz zapisanie informacji w systemie.  

**kroki:**
1. **Administrator systemu** wybiera opcję dodania nowego użytkownika.  
2. **Administrator systemu** wprowadza dane nowego użytkownika.  
3. **Administrator systemu** przypisuje role i uprawnienia nowemu użytkownikowi.  
4. **Administrator systemu** zatwierdza dodanie użytkownika.  
5. **System** weryfikuje poprawność wprowadzonych danych.  
6. **System** zapisuje dane nowego użytkownika w bazie danych.  
7. **System** wyświetla komunikat o pomyślnym dodaniu użytkownika.  

**alt 1 Niepoprawne dane użytkownika:**
1. **System** wykrywa, że wprowadzone dane użytkownika są niepoprawne.
2. **System** wyświetla komunikat o błędzie i prosi administratora o poprawienie danych.  

**alt 2 Konflikt loginu:**
1. **System** wykrywa, że wprowadzony login jest już zajęty przez innego użytkownika.  
2. **System** wyświetla komunikat o konflikcie loginu.  


#### UC0024 Przyznanie dostępu do systemu
**nazwa:** Przyznanie dostępu do systemu

**aktorzy:** Administrator systemu, System  
**opis:**  
System umożliwia administratorowi przyznanie dostępu do systemu wybranemu użytkownikowi. Proces obejmuje wybór użytkownika, określenie poziomu dostępu oraz zapisanie zmian w systemie.  

**kroki:**  
1. **Administrator systemu** wybiera opcję przyznania dostępu użytkownikom.  
2. **Administrator systemu** wybiera użytkownika, któremu chce przyznać dostęp.  
3. **Administrator systemu** określa poziom dostępu.
4. **Administrator systemu** zatwierdza zmiany.  
5. **System** weryfikuje poprawność wprowadzonych danych.  
6. **System** zapisuje zmiany w bazie danych.  
7. **System** wyświetla komunikat o pomyślnym przyznaniu dostępu.  

**alt 1 Niepoprawne dane:**
1. **System** wykrywa, że wprowadzone dane są niepoprawne.  
2. **System** wyświetla komunikat o błędzie i prosi administratora o poprawienie danych.  

**alt 2 Użytkownik już posiada dostęp:** 
1. **System** wykrywa, że użytkownik już posiada przyznany dostęp na wybranym poziomie.  
2. **System** wyświetla komunikat informujący o istniejącym dostępie.


#### UC0025 Usunięcie użytkownika
**nazwa:** Usunięcie użytkownika

**aktorzy:** Administrator systemu, System  
**opis:**  
System umożliwia administratorowi usunięcie użytkownika z systemu. Proces obejmuje wprowadzenie danych użytkownika i usunięcie go z systemu.  

**kroki:**
1. **Administrator systemu** wybiera opcję usunięcia użytkownika.  
2. **Administrator systemu** wprowadza dane użytkownika.  
3. **Administrator systemu** zatwierdza usunięcie użytkownika.  
4. **System** weryfikuje poprawność wprowadzonych danych.  
5. **System** zapisuje usuwa dane użytkownika z bazy danych.  
6. **System** wyświetla komunikat o pomyślnym usnięciu użytkownika.  

**alt 1 Niepoprawne dane użytkownika:**
1. **System** wykrywa, że wprowadzone dane użytkownika są niepoprawne.
2. **System** wyświetla komunikat o błędzie i prosi administratora o poprawienie danych.  


#### UC0026 Usunięcie dostępu do systemu
**nazwa:** Usunięcie dostępu do systemu

**aktorzy:** Administrator systemu, System  
**opis:**  
System umożliwia administratorowi usunięcie dostępu do systemu wybranemu użytkownikowi. Proces obejmuje wybór użytkownika, określenie poziomu dostępu oraz zapisanie zmian w systemie.  

**kroki:**  
1. **Administrator systemu** wybiera opcję usunięcia dostępu użytkownikom.  
2. **Administrator systemu** wybiera użytkownika, któremu chce usunąć dostęp.  
3. **Administrator systemu** określa poziom dostępu.
4. **Administrator systemu** zatwierdza zmiany.  
5. **System** weryfikuje poprawność wprowadzonych danych.  
6. **System** zapisuje zmiany w bazie danych.
7. **System** wyświetla komunikat o pomyślnym przyznaniu dostępu.  

**alt 1 Niepoprawne dane:**
1. **System** wykrywa, że wprowadzone dane są niepoprawne.  
2. **System** wyświetla komunikat o błędzie i prosi administratora o poprawienie danych.  

**alt 2 Użytkownik nie posiada usuwanego dostępu:** 
1. **System** wykrywa, że użytkownik nie posiada dostępu na wybranym poziomie.  
2. **System** wyświetla komunikat informujący o nieistniejącym dostępie.


#### UC0027 Audyt dostępu
**nazwa:** Audyt dostępu

**aktorzy:** Administrator systemu, System  
**opis:**  
System umożliwia administratorowi przeprowadzenie audytu dostępu użytkowników do systemu. Proces obejmuje generowanie raportu zawierającego informacje o poziomach dostępu użytkowników oraz ich aktywności.  

**kroki:**  
1. **Administrator systemu** przechodzi do sekcji audytu dostępu.  
2. **Administrator systemu** wybiera zakres danych do audytu.
3. **Administrator systemu** zatwierdza żądanie wygenerowania raportu.  
4. **System** przetwarza żądanie i generuje raport audytu dostępu.  
5. **System** wyświetla raport audytu dostępu administratorowi.  

**alt 1 Brak danych do audytu:**  
1. **System** wykrywa brak danych spełniających kryteria audytu.  
2. **System** wyświetla komunikat informujący o braku danych do audytu.  

**alt 2 Błąd podczas generowania raportu:**  
1. **System** napotyka błąd podczas generowania raportu. 
2. **System** wyświetla komunikat o błędzie.  