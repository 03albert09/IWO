##### Administrator
[Użytkownik](#użytkownik) z najwyższymi uprawnieniami w systemie, odpowiedzialny za zarządzanie [użytkownikami](#użytkownik), dostępami, oraz konfiguracją systemu. Administrator ma pełny wgląd w operacje związane z nadawaniem i odbieraniem uprawnień, dostęp do pełnego audytu systemowego oraz możliwość zarządzania kontami [użytkowników](#użytkownik). Do jego uprawnień należy także [zmiana haseł](#zmiana-hasła-użytkownika) użytkowników (w przypadku, gdy ten zapomniał swojego [hasła](#hasło)), usuwanie dostępu, tworzenie, edytowanie i zarządzanie [schematami danych](#schemat-danych).

##### Adres zbioru
Lokalizacja umożliwiająca dostęp do danego [zbioru danych](#zbiór-danych). Jest to element widoczny przy [wyświetlaniu zbiorów danych](#wyświetlanie-zbiorów-danych).

##### Aktualizacja danych
Proces modyfikowania istniejących danych w systemie. W przypadku aktualizacji przez [API](#api-application-programming-interface), zmiany są wprowadzane tylko wtedy, gdy [użytkownik](#użytkownik) posiada odpowiednie uprawnienia do dodawania i edytowania danych.

##### Anomalie
Przypadki, w których dane w systemie odbiegają od ustalonych norm lub założeń, np. nieoczekiwane zmiany w istniejących danych. Może to obejmować błędy, nieprawidłowości lub niezgodności z oczekiwanymi wartościami.

##### API (Application Programming Interface)
Interfejs umożliwiający komunikację między różnymi systemami, pozwalający na wymianę danych i wykonywanie operacji na danych. API w tym przypadku umożliwia dodawanie i edytowanie zbiorów danych w systemie.

##### Archiwizacja zbiorów danych
Proces przechowywania kopii zapasowych [metadanych zbiorów danych](#metadane-zbioru-danych) w systemie, aby zapewnić możliwość ich odzyskania w przypadku awarii. Archiwizacja obejmuje tworzenie kopii zapasowych zgodnie z ustalonym [harmonogramem](#harmonogram-archiwizacji). Same [zbiory danych](#zbiór-danych) nie są objęte archwizacją.

##### Archiwizacja danych
Proces, w którym dane są przechowywane w specjalnym, zabezpieczonym miejscu przed ich usunięciem z systemu. Archiwizacja zapewnia, że dane nie zostaną utracone, mimo iż nie są już dostępne w systemie.

##### Atrybuty zbioru danych (metadane)
Właściwości opisujące [zbiór danych](#zbiór-danych), takie jak: [adres zbioru](#adres-zbioru-danych), [podmiot odpowiedzialny za zbiór danych](#podmiot-odpowiedzialny-za-zbiór-danych), [opis](#opis), [data aktualizacji](#data-aktualizacji), przechowywane w [bazie zbiorów danych](#baza-zbiorów-danych). W kontekście [API](#api-application-programming-interface), atrybuty (metadane) są przesyłane i edytowane w formatach takich jak [XML](#xml) i [JSON](#json).

##### Automatyczne przesyłanie danych
Proces, w którym dane są automatycznie przesyłane do CKAN bez potrzeby ręcznego inicjowania, np. w odpowiedzi na zmiany w systemie.

##### Baza zbiorów danych
Centralne miejsce przechowywania [metadanych](#metadane-zbioru-danych) zbiorów danych dostępnych w systemie. System powinien pobierać z bazy danych informacje ([metadane](#metadane-zbioru-danych)) o wszystkich dostępnych zbiorach danych. W przypadku awarii bazy danych, system powinien informować o jej niedostępności.

##### Blokada konta
Mechanizm uniemożliwiający użytkownikowi zalogowanie się do systemu, bez usuwania jego danych. Blokada może być nałożona przez [administratora](#administrator) w wyniku decyzji administracyjnej lub naruszenia zasad bezpieczeństwa.

##### CAPTCHA
System mający na celu weryfikację, czy użytkownik jest człowiekiem, a nie automatycznym botem. Jest częścią procesu [logowanie do systemu](#logowanie-do-systemu) i polega na rozwiązaniu prostego zadania (np. zaznaczenie odpowiednich obrazków, odczytaniu tekstu ze zniekształconych liter).

##### CKAN
Platforma open-source do zarządzania danymi, umożliwiająca ich publikację, integrację z innymi systemami oraz stosowanie standardów tworzenia i udostępniania [schematów danych]. W tym przypadku system synchronizuje swoje dane z CKAN.

##### Data aktualizacji
Data ostatniej modyfikacji [danego zbioru](#zbiór-danych). Jest to element widoczny przy [wyświetlaniu zbiorów danych](#wyświetlanie-zbiorów-danych).

##### Eksport danych z systemu
Proces umożliwiający [użytkownikowi](#użytkownik) pobranie wybranych danych w formatach [JSON](#json) lub [YAML](#yaml). Eksport danych jest dostępny dla wszystkich [użytkowników](#użytkownik), nie wymagając specjalnych [uprawnień eksportu](#uprawnienia-eksportu).

##### Endpoint
Punkt końcowy [API](#api-application-programming-interface), do którego aplikacje mogą wysyłać żądania w celu wykonania operacji na danych (np. dodawanie, edytowanie, pobieranie danych). Każdy endpoint ma określoną funkcję, jaką wykonuje w systemie.

##### Format danych
Struktura, w jakiej dane są przesyłane do przeglądarki. Format musi być zgodny z wymaganiami przeglądarki oraz odpowiedni dla rodzaju wizualizacji, np. [JSON](#json), [XML](#xml).

##### Formaty eksportu
Różne struktury, w jakich dane mogą być eksportowane z systemu. Obsługiwane formaty eksportu to [XML](#xml), [JSON](#json), oraz inne formaty, zgodne z wymaganiami użytkowników i systemu.

##### Gwiazdki
Sposób oceniania, w którym użytkownik wybiera liczbę gwiazdek (od 1 do 5) w celu wyrażenia swojej opinii o danym [zbiorze danych](#zbiór-danych). Liczba gwiazdek jest obowiązkowa, a komentarz jest opcjonalny.

##### Harmonogram archiwizacji
Zasady określające częstotliwość tworzenia kopii zapasowych i czasu ich przechowywania. W systemie obowiązuje następujący harmonogram:
- Kopie dzienne przechowywane przez tydzień.
- Kopie tygodniowe przez kolejne 2 tygodnie.
- Kopie miesięczne przez 6 miesięcy.
- Kopie roczne przechowywane przez 2 lata.

##### Hasło
Ciąg znaków służący jako sekretne dane do weryfikacji tożsamości użytkownika w procesie logowania. Hasło jest powiązane z [loginem](#login) i umożliwia uzyskanie dostępu do systemu. Hasło przy tworzeniu bądź zmianie musi spełniać wymagania dotyczące długości hasła, użycia znaków specjalnych, liczb i wielkich liter.

##### Historia wyszukiwania zbiorów danych
Zapis wszystkich zapytań wyszukiwania wprowadzonych przez [użytkowników](#użytkownik). System prowadzi pełny audyt i rejestruje pytania wyszukiwarki. Te statystyki powinny być dostępne dla [administratorów](#administrator).

##### Integracja z CKAN
Proces umożliwiający wymianę danych pomiędzy systemem zewnętrznym a platformą [CKAN](#ckan), który umożliwia przesyłanie, synchronizowanie i udostępnianie danych w sposób zorganizowany i zgodny z wymaganiami CKAN. Integracja ta może być realizowana w trybie jednokierunkowym (dane przesyłane tylko z systemu do CKAN) lub dwukierunkowym (dane mogą być wymieniane zarówno z systemu do CKAN, jak i odwrotnie). Integracja z CKAN pozwala na automatyczne publikowanie danych w zbiorach danych (datasets), zarządzanie metadanymi, a także na integrację z innymi systemami i aplikacjami, które korzystają z platformy CKAN do przechowywania i udostępniania danych. Proces ten obejmuje użycie API CKAN, które pozwala na dodawanie, modyfikowanie oraz usuwanie danych, a także na pobieranie informacji o dostępnych zasobach.

##### JSON
Format wymiany danych, który przechowuje dane w postaci strukturalnej. Jest to format tekstowy oparty na parze klucz-wartość, który jest łatwy do odczytania i zapisania zarówno przez ludzi, jak i maszyny.

##### Komentarz
Tekstowy opis lub uwaga dodawana przez użytkownika do oceny [zbioru danych](#zbiór-danych), który stanowi uzupełnienie dla przypisanej liczby [gwiazdek](#gwiazdki). Komentarz jest opcjonalny, ale jeśli zostanie dodany, nie można go edytować ani usuwać po zapisaniu oceny.

##### Komunikat o niedostępności bazy danych
Informacja zwracana [użytkownikowi](#użytkownik) w przypadku awarii [bazy zbiorów danych](#baza-zbiorów-danych), informująca o braku dostępu do informacji o [zbiorach danych](#zbiór-danych).

##### Kopie zapasowe
Pełne kopie [metadanych zbiorów danych](#metadane-zbiorów-danych), które są tworzone regularnie, w celu ochrony przed utratą danych. Kopie zapasowe są przechowywane zgodnie z ustalonymi zasadami i [harmonogramem](#harmonogram-archiwizacji).

##### Login
Unikalny identyfikator użytkownika, który jest wykorzystywany podczas logowania do systemu. Login jest wymagany do weryfikacji tożsamości [użytkownika](#użytkownik) i jest powiązany z odpowiednim [hasłem](#hasło).

##### Logowanie do systemu
Proces umożliwiający użytkownikowi dostęp do systemu poprzez uwierzytelnienie za pomocą [loginu](#login) i [hasła](#hasło). [Użytkownik](#użytkownik) wprowadza swoje dane, a system weryfikuje poprawność wprowadzonych informacji w celu przyznania dostępu. Logowanie do systemu wymaga rozwiązania zadania [CAPTCHA](#captcha) i może wymagać dodatkowego uwierzytelnienia za pomocą [logowania dwuskładnikowego (2FA)](#logowanie-dwuskładnikowe-2fa). System nie obsługuje logowania za pomocą adresu e-mail ani OAuth.

##### Logowanie dwuskładnikowe (2FA)
Proces uwierzytelniania użytkownika, który wymaga dwóch kroków w celu potwierdzenia tożsamości. Po podaniu [loginu](#login) i [hasła](#hasło), [użytkownik](#użytkownik) musi dodatkowo podać jednorazowy kod przesłany na e-mail.

##### Komunikat o anomalii
Powiadomienie, które jest wysyłane, gdy wykryta zostaje anomalia w systemie. Komunikat informuje [administratorów](#administrator) o wystąpieniu incydentu, ale nie wskazuje bezpośrednio osoby odpowiedzialnej.

##### Komunikat o błędzie zmiany hasła
Komunikat wyświetlany użytkownikowi, informujący o błędach w procesie [zmiany hasła](#zmiana-hasła-użytkownika), np. w przypadku wprowadzenia dwóch różnych [nowych haseł](#nowe-hasło) ("hasło nieprawidłowe").

##### Menadżer (Przedstawiciel firmy)
Użytkownik reprezentujący podmiot odpowiedzialny za [zbiór danych](#zbiór-danych) oraz posiadający uprawnienia do przyznawania dostępu do określonego obszaru systemu. Może nadawać i odbierać uprawnienia użytkownikom związanym z danym obszarem oraz przeglądać audyty dotyczące operacji na [zbiorach danych](#zbiór-danych).

##### Monitorowanie problemów
W przypadku wystąpienia problemu wydajnościowych [administrator](#administrator) decyduje, czy wymaga on monitorowania. Jeśli tak, określa, które wskaźniki wydajnościowe powinny być śledzone.

##### Nowe hasło
[Hasło](#hasło), które użytkownik wprowadza dwukrotnie, aby je ustalić jako nowe. W przypadku niezgodności obu wprowadzonych nowych haseł, system wyświetli komunikat o błędzie: "hasło nieprawidłowe".

##### Ocena
Ocena przypisywane do [zbiorów danych](#zbiór-danych) przez użytkowników. Ocena przyjumje formę [gwiazdek](#gwiazdki) z opcjonalnym [komentarzem](#komentarz). Ilości [gwiazdek](#gwiazdki) ani [komentarza](#komentarz) nie można zmienić. Nie ma możliwości wystawienia opinii dla danej oceny.

##### Odwiedziny zbioru
Zdarzenie, w którym użytkownik wchodzi na stronę danego zbioru danych w celu jego [przeglądania](#wizualizacja-zbioru-danych-przeglądanie-zbioru-danych). Dane o odwiedzinach są zbierane anonimowo, bez ujawniania tożsamości odwiedzających.

##### Operacje na metadanych
Działania wykonywane na metadanych zbiorów danych, takie jak dodawanie, edytowanie lub usuwanie metadanych. Te operacje obsługują formaty takie jak [XML](#xml) i [JSON](#json), które pozwalają na przechowywanie i przesyłanie informacji o zbiorach danych w 
odpowiednim formacie.

##### Opis
Krótki tekst charakteryzujący zawartość i przeznaczenie danego [zbioru danych](#zbiór-danych). Jest to element widoczny przy [wyświetlaniu zbiorów danych](#wyświetlanie-zbiorów-danych).

##### Podmiot odpowiedzialny za zbiór danych (dostawca danych)
Osoba bądź instytucja dostarczająca dane i odpowiedzialna za tworzenie danego [zbiór danych](#zbiór-danych), jego aktualność i poprawność. Jest to element widoczny przy [wyświetlaniu zbiorów danych](#wyświetlanie-zbiorów-danych).

##### Powiadomienie o zmianie uprawnień
Automatyczna wiadomość wysyłana na e-mail'a do [użytkownika](#użytkownik) informująca o przyznaniu, odebraniu lub zmianie jego uprawnień w systemie.

##### Proces archiwizacji
Procedura obejmująca tworzenie, przechowywanie i zarządzanie kopiami zapasowymi [metadanych zbiorów danych](#metadane-zbioru-danych) w systemie. Celem archiwizacji jest zapewnienie bezpieczeństwa danych przez długoterminowe przechowywanie kopii zapasowych.

##### Pracownik
Użytkownik z podstawowym dostępem do systemu, ograniczonym do funkcji wymaganych do wykonywania obowiązków w danym obszarze. Nie posiada uprawnień do zarządzania innymi użytkownikami.

##### Przyznanie dostępu do systemu
Proces nadawania użytkownikowi odpowiednich uprawnień w systemie w zależności od jego roli. Przyznawanie dostępu może być wykonywane przez [administratora](#administrator) lub [menadżera](#menadżer-przedstawiciel-firmy) uprawnionego do zarządzania dostępem do zbiorów danych dostarczanych przez firmę, dla której pracuje.

##### Raporty o ruchu
Zestawienia przedstawiające dane o odwiedzinach i interakcjach użytkowników z systemem, takie jak liczba odwiedzin zbiorów danych, w tym dane anonimowe.

##### Raport wydajności
Zestawienie i analiza dotyczące wydajności systemu, obejmujące dane o działaniu serwerów, baz danych, endpointów, backendu itp. Raporty wydajnościowe nie obejmują monitorowania czasu wykonywania requestów, a zamiast tego koncentrują się na innych aspektach wydajności systemu, takich jak obciążenie serwerów, liczba obsługiwanych zapytań czy stan zasobów systemowych.

##### Schemat danych
Struktura opisująca sposób organizacji zbioru danych. Może być definiowana w postaci kodu źródłowego, [XML](#xml), [JSON](#json) lub innego formatu zgodnego z [CKAN](#ckan) oraz podlega wersjonowaniu. Podlega śledzeniu zmian w nim wprowadzanych, zachowanie historii modyfikacji oraz umożliwia przywracanie wcześniejszych wersji.

##### Sortowanie ocen
Możliwość sortowania ocen na podstawie różnych kryteriów, takich jak data wystawienia oceny lub ilość [gwiazdek](#gwiazdki).

##### Sortowanie wyników wyszukiwania
Uporządkowanie [zbiorów danych](#zbiór-danych) zwróconych jako [wyniki wyszukiwania](#wyniki-wyszukiwania-zbiorów-danych), zgodnie z zasadami [sortowania zbiorów danych](#sortowanie-zbiorów-danych), według wartości w wybranej kolumnie jednego z ich [atrybutów](#atrybuty-zbiorów-danych).

##### Sortowanie zbiorów danych
Uporządkowanie [zbiorów danych](#zbiór-danych), według kolumny jednego z wyświetlanych [atrybutów zbiorów](#atrybuty-zbioru-danych-metadane): [adres zbioru](#adres-zbioru), [podmiot odpowiedzialny za zbiór danych](#podmiot-odpowiedzialny-za-zbiór-danych-dostawca-danych), [opis](#opis), [data aktualizacji](#data-aktualizacji).

##### Statystyki i metryki
Dane liczbowe i mierniki, które pozwalają ocenić wydajność systemu, takie jak obciążenie serwera, czas odpowiedzi endpointów, przepustowość itp.

##### Stare hasło
[Hasło](#hasło) aktualnie przypisane do konta [użytkownika](#użytkownik), które jest wymagane do zatwierdzenia [zmiany hasła](#zmiana-hasła-użytkownika). Użytkownik musi poprawnie wprowadzić stare hasło przed podaniem [nowego hasła](#nowe-hasło).

##### Token
Unikalny identyfikator używany do autoryzacji dostępu do API. Token jest generowany i przekazywany użytkownikowi po weryfikacji jego uprawnień, umożliwiając mu autoryzację i wykonanie operacji na zbiorach danych.

##### Trafność zapytania
Stopień zgodności [wyników wyszukiwania zbiorów danych](#wyniki-wyszukiwania-zbiorów-danych) z [zapytaniem](#zapytanie) użytkownika, oceniany na podstawie dopasowania treści [opisów](#opis) oraz innych [atrybutów zbiorów danych](#atrybuty-zbiorów-danych) do zapytania.

##### Typy wizualizacji
Różne formy prezentacji danych, takie jak wykresy, tabele, mapy, diagramy czy inne graficzne reprezentacje danych, które są używane w zależności od charakterystyki [zbioru danych](#zbiór-danych) i wymagań interesariuszy.

##### Uprawnienia do aktualizacji
Zestaw praw dostępu przypisanych [pracownikowi](#pracownik), które umożliwiają wykonywanie operacji aktualizacji danych. Aktualizacja nie będzie mogła zostać przeprowadzona bez odpowiednich uprawnień.

##### Uprawnienia do generowania raportów
Osoby posiadające wyższe uprawnienia, takie jak administratorzy czy uprawnieni pracownicy, mogą generować raporty o ruchu w systemie.

##### Uprawnienia do usunięcia danych
Zestaw praw dostępu przyznanych użytkownikowi lub administratorowi, umożliwiający usuwanie danych. Tylko administratorzy i pracownicy z odpowiednimi uprawnieniami mogą przeprowadzać operację usuwania danych.

##### Uprawnienia eksportu
Brak ograniczeń dotyczących [eksportu danych](#eksport-danych-z-systemu). Każdy [użytkownik](#użytkownik) ma możliwość pobrania danych w formacie [JSON](#json) lub [YAML](#yaml) bez specjalnych wymagań dotyczących poziomu uprawnień.

##### Usunięcie danych
Proces trwałego usuwania danych z systemu. W tym przypadku dane są usuwane, ale przed fizycznym usunięciem są archiwizowane, co pozwala na ich odzyskanie w razie potrzeby.

##### Usunięcie dostępu do systemu
Proces polegający na odebraniu pewnego poziomu dostępu do systemu, wykonywany wyłącznie przez [administratora](#administrator). Dane użytkownika pozostają w bazie, ale nie ma on dostępu do żadnej funkcjonalności systemu.

##### Usunięcie użytkownika (dezaktywacja konta)
Proces polegający na trwałym odebraniu użytkownikowi dostępu do systemu bez usuwania jego konta z bazy. Dezaktywowany użytkownik nie może się logować ani korzystać z funkcjonalności systemu, jednak jego dane oraz historia operacji pozostają zachowane w celach audytowych.

##### Użytkownik
Osoba korzystająca z systemu w celu wyszukiwania i przeglądania [zbiorów danych](#zbiór-danych), mająca możliwość eksportu danych w formacie [JSON](#json) lub [YAML](#yaml).

##### Weryfikacja treści
Proces sprawdzania danych pod kątem zgodności z określonymi standardami. W tym przypadku nie jest przeprowadzane sprawdzanie treści danych pod kątem wulgaryzmów.

##### Widoki danych
Zestaw wstępnie zdefiniowanych sposobów prezentacji danych, które są zaprojektowane przez programistów na podstawie wymagań interesariuszy. Użytkownik nie ma możliwości edytowania lub tworzenia własnych widoków; widoki są ustalane i wdrażane przez zespół deweloperski.

##### Wizualizacje raportu (szczegóły raportu)
Wykresy, tabele lub inne formy wizualizacji, które przedstawiają wyniki analizy wydajności systemu. Wizualizacje mogą być generowane w przeglądarkach na podstawie zebranych danych.

##### Wizualizacja zbioru danych (przeglądanie zbioru danych)
Proces przedstawiania [odwiedzanego zbioru](#odwiedziny-zbioru) w formie graficznej, umożliwiający użytkownikowi łatwiejsze zrozumienie i analizowanie informacji. Wizualizacja może przybierać różne formy, takie jak wykresy, tabele, mapy czy inne przedstawienia danych. Wizualizacje są generowane w przeglądarkach, które oczekują strumienia danych w odpowiednim [formacie danych](#format-danych).

##### Wycofywanie zmian
Wszelkie operacje na [zbiorach danych](#zbiór-danych) są rejestrowane, a zmiany nie są usuwane ani cofane. System zapewnia pełny audyt operacji na [metadanych](#metadane-zbioru-danych), podobnie jak w systemie kontroli wersji (takich jak Git).

##### Wykrywanie anomalii
Proces monitorowania danych w celu identyfikacji sytuacji, które nie spełniają ustalonych norm. W tym przypadku dane są okresowo walidowane pod kątem zmian, a w przypadku wykrycia anomalii [komunikat](#komunikat-o-anomalii) o tym zostaje wysłany do [administratorów](#administrator).

##### Wyniki wyszukiwania zbiorów danych
Podzbiór [zbiorów danych](#zbiorów-danych), który jest zgodny z wybranymi przez użytkwonika [atrybutami zbiorów danych](#atrybuty-zbioru-danych-metadane) i jest prezentowany w ramach [wyświetlania zbiorów danych](#wyświetlanie-zbiorów-danych). Lista wyników zależy od [trafności zapytania](#trafność-zapytania), a kolejność wyników może być modyfikowana przez [sortowanie wyników wyszukiwania](#sortowanie-wyników-wyszukiwania).

##### Wyświetlanie zbiorów danych
Prezentacja [użytkownikowi](#użytkownik) tabeli zawierającej [zbiory danych](#zbiór-danych) wraz z ich [atrybutami](#atrybuty-zbioru-danych-metadane). Lista wyświetlanych [zbiorów danych](#zbiór-danych) może obejmować zarówno wszystkie dostępne [zbiory danych](#zbiór-danych), jak i [wyniki wyszukiwania zbiorów danych](#wyniki-wyszukiwania-zbiorów-danych). O kolejności i zakresie wyświetlanych zbiorów decydują [trafność zapytania](#trafność-zapytania) oraz [sortowanie wyników wyszukiwania](#sortowanie-wyników-wyszukiwania).

##### YAML
Format danych oparty na strukturze tekstowej, wykorzystywany do przechowywania danych w formie zrozumiałej dla człowieka. Jego składnia jest bardziej przyjazna dla [użytkownika](#użytkownik) w porównaniu do [JSON](#json), używając wcięć do wskazywania hierarchii danych.

##### XML
Język znaczników służący do przechowywania i wymiany danych w formie tekstowej. XML pozwala na tworzenie własnych znaczników, co sprawia, że jest elastyczny i niezależny od platformy. Dokumenty XML są używane do reprezentowania danych w sposób hierarchiczny, umożliwiając przechowywanie zarówno prostych, jak i złożonych struktur danych. Jest powszechnie stosowany w integracji systemów, bazach danych oraz w przesyłaniu danych między aplikacjami.

##### Zapytanie
Fraza wprowadzona przez [użytkownika](#użytkownik) do wyszukiwarki, która jest analizowana przez system w celu dopasowania wyników. System wyszukuje [zbiory danych](#zbiór-danych), które mają najlepszą [trafność zapytania](#trafność-zapytania).

##### Zgłoszenie usunięcia dostępu
Proces inicjowany przez dział kadr, gdy pracownik traci swoje uprawnienia wynikające z zatrudnienia. Kadry przekazują informację o konieczności usunięcia użytkownika, co skutkuje jego dezaktywacją.

##### Zmiana hasła użytkownika
Proces umożliwiający użytkownikowi zmianę swojego hasła w systemie. Zmiana hasła wymaga podania [starego hasła](#stare-hasło), [nowego hasła](#nowe-hasło) dwukrotnie oraz weryfikacji, czy oba wprowadzone hasła są identyczne i spełniają wymagania bezpieczeństwa. System nie umożliwia zmiany hasła bez znajomości aktualnego [hasła](#hasło), chyba że [administrator](#administrator) wykonuje tę operację w przypadku, gdy użytkownik zapomniał [hasła](#hasło).

##### Zbiór danych
Kolekcja danych udostępnianych przez systemie. Posiada następujące [atrybuty](#atrybuty-zbioru-danych-metadane): [adres zbioru](#adres-zbioru), [podmiot odpowiedzialny za zbiór danych](#podmiot-odpowiedzialny-za-zbiór-danych), [opis](#opis), [data aktualizacji](#data-aktualizacji).