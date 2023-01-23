# GymRegister
Założenia:
- stworzenie systemu automatycznej generacji kart członkowskich siłowni akademickiej
- stworzenie bazy danych członków siłowni oraz rejestru wejść/wyjść danego członka siłowni (w celu utrzymania kontroli) w danym dniu
- możliwość automatycznego uzupełniania bazy danych rejestru poprzez skanowanie QRcodu (lub czegoś innego) przypisanego danemu członkowi
- generowanie raportów (częstotliwości korzystania, ...)

Opis procesów:
1) Tworzenie karty członkowskiej
W tym momencie samo zgłoszenie się studenta, aby otrzymać kartę członkowską odbywa się poprzez email. Następnie zostaje mu wydrukowana karta wyrysowana w Microsoft 
Word. Po uiszczeniu opłaty student zostaje dopisany do listy członkowskiej, która jest sprawdzana przez Panią na portierni, a następnie takiemu koledze jest wydawany klucz do siłowni.

Jak zautomatyzować rozwiązanie?
- Automatyczne sprawdzanie poprawności danych -> imie, nazwisko, nr pokoju, nr telefonu, zdjecie, adres mailowy
- Auto generowanie karty członkowskiej
- Sprawdzenie wpływu płatności poprzez jakieś API bankowe
- Po wykonaniu obu powyższych punktów automatyczne drukowanie karty oraz wysłanie maila do interesanta z informacją o możliwości odbioru karty.

2) Sprawdzanie członka siłowni na liście przez Panią portierkę
W tym momencie odbywa się to poprzez manualne sprawdzanie oczami Pani z portierni i wyszukiwaniu nazwiska na liście (po okazaniu karty członkowskiej)
Listę taką muszę przygotować ja, wydrukować dostarczyć.

Jak zautomatyzować?
Telefon podłączony do sieci, w której znajduje się serwer. Skanowanie QRCodu -> sprawdzenie czy cżłonek jest w bazie (czy jego karta jest ważna). Wiadomość zwrotna do Pani ze smartfona. Następnie po skanowaniu takiego delikwenta kolega zostaje utworzony rekord wejścia na siłownie z datą i godziną otrzymania klucza. 


Technologie:
Python - docx, 
Word,
mySQL, 
