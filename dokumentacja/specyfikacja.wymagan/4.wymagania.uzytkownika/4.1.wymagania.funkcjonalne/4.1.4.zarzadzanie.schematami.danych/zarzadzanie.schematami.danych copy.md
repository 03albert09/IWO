#### Diagram

:[Diagram](diagram.puml)

#### Przypadki użycia


#### UC0028 Tworzenie schematów danych
**nazwa:** Tworzenie schematów danych

**aktorzy:** Administrator systemu, System, CKAN  
**opis:**  
System umożliwia administratorowi tworzenie nowych schematów danych. Proces obejmuje wprowadzenie szczegółów schematu, zapisanie go w systemie oraz synchronizację z platformą CKAN.  

**kroki:**  
1. **Administrator systemu** wybiera opcję tworzenia nowego schematu danych.  
2. **Administrator systemu** wprowadza szczegóły schematu.  
3. **Administrator systemu** zatwierdza utworzenie schematu.  
4. **System** weryfikuje poprawność wprowadzonych danych.
5. **System** zapisuje nowy schemat danych w bazie danych.
6. **System** synchronizuje schemat z platformą CKAN, przesyłając odpowiednie dane.
7. **System** wyświetla komunikat o pomyślnym utworzeniu schematu danych.  

**alt 1 Niepoprawne dane schematu:**  
1. **System** wykrywa, że wprowadzone dane schematu są niepoprawne.
2. **System** wyświetla komunikat o błędzie i prosi administratora o poprawienie danych.  

**alt 2 Błąd synchronizacji z CKAN:**  
1. **System** napotyka błąd podczas synchronizacji z platformą CKAN. 
2. **System** zapisuje schemat lokalnie i wyświetla komunikat o błędzie synchronizacji. 


#### UC0029 Aktualizacja schematów danych
**nazwa:** Aktualizacja schematów danych

**aktorzy:** Administrator systemu, System, CKAN  
**opis:**  
System umożliwia administratorowi aktualizację istniejących schematów danych. Proces obejmuje edycję szczegółów schematu, zapisanie zmian w systemie oraz synchronizację z platformą CKAN.  

**kroki:**  
1. **Administrator systemu** wybiera schemat danych do edycji.  
2. **Administrator systemu** wprowadza zmiany w szczegółach schematu.
3. **Administrator systemu** zatwierdza zmiany.  
4. **System** weryfikuje poprawność wprowadzonych danych.  
5. **System** zapisuje zmiany w bazie danych. 
6. **System** synchronizuje zmiany z platformą CKAN.  
7. **System** wyświetla komunikat o pomyślnej aktualizacji schematu danych.  

**alt 1 Niepoprawne dane schematu:**  
1. **System** wykrywa, że wprowadzone dane schematu są niepoprawne.  
2. **System** wyświetla komunikat o błędzie i prosi administratora o poprawienie danych.  

**alt 2 Błąd synchronizacji z CKAN:**  
1. **System** napotyka błąd podczas synchronizacji z platformą CKAN.  
2. **System** zapisuje zmiany lokalnie i wyświetla komunikat o błędzie synchronizacji. 


#### UC0030 Listowanie schematów danych
**nazwa:** Listowanie schematów danych

**aktorzy:** Administrator systemu, System  
**opis:**  
System umożliwia administratorowi przeglądanie listy dostępnych schematów danych. Lista zawiera szczegóły schematów, takie jak nazwa, opis i data ostatniej modyfikacji.  

**kroki:**  
1. **Administrator systemu** przechodzi do sekcji zarządzania schematami danych.  
2. **System** pobiera z bazy danych listę schematów danych.  
3. **System** wyświetla listę schematów danych administratorowi.  

**alt 1 Brak schematów danych:**  
1. **System** wykrywa, że w bazie danych nie ma dostępnych schematów.  
2. **System** wyświetla komunikat informujący o braku schematów danych.  


#### UC0031 Usuwanie schematów danych
**nazwa:** Usuwanie schematów danych

**aktorzy:** Administrator systemu, System, CKAN  
**opis:**  
System umożliwia administratorowi usunięcie istniejących schematów danych. Proces obejmuje wybór schematu do usunięcia, usunięcie go z systemu oraz synchronizację zmian z platformą CKAN.  

**kroki:**
1. **Administrator systemu** wybiera schemat danych do usunięcia.  
2. **Administrator systemu** zatwierdza usunięcie schematu.  
3. **System** weryfikuje poprawność operacji.  
4. **System** usuwa schemat danych z bazy danych.  
5. **System** synchronizuje usunięcie schematu z platformą CKAN.  
6. **System** wyświetla komunikat o pomyślnym usunięciu schematu danych.  

**alt 1 Schemat danych jest używany:**  
1. **System** wykrywa, że schemat danych jest powiązany z istniejącymi zbiorami danych.  
2. **System** wyświetla komunikat o błędzie i uniemożliwia usunięcie schematu.  

**alt 2 Błąd synchronizacji z CKAN:**  
1. **System** napotyka błąd podczas synchronizacji z platformą CKAN.  
2. **System** zapisuje zmiany lokalnie i wyświetla komunikat o błędzie synchronizacji.