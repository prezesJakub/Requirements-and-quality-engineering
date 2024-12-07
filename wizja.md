# Wizja projektu

## Nazwa produktu
TaxiDispatcher5000

## Dziedzina problemu
Firma Dedal jest prosperującą korporacją taksówkową w mieście. W firmie pracują dyspozytorzy i kierowcy. Składanie zamówień odbywa się w ten sposób, że dyspozytor siedzi w biurze i odbiera telefony klientów. Ma do dyspozycji prosty system pokazujący mu lokalizację kierowców na podstawie nadajników umieszczonych w taksówkach. Następnie wysyła do wybranego kierowcy szczegóły zlecenia przez SMS, informując o miejscu startowym i docelowym danego zlecenia. Kierowca po odczytaniu SMSa, w przypadku potwierdzenia odebrania zlecenia, daje znać dyspozytorowi krótką odpowiedzią SMS. Następnie ręcznie ustawia nawigację w zewnętrznej aplikacji nawigacyjnej. W przypadku chęci zgłoszenia przerwy lub zaistniałych problemów, kierowca także kontaktuje się z dyspozytorem telefonicznie. Cena kursu jest obliczana na bieżąco na podstawie obowiązującej taryfy w danej godzinie, za pomocą przestarzałego taksometru zamontowanego w każdym firmowym pojeździe.

## Problemy do rozwiązania

Głównym problemem w firmie jest brak oprogramowania umożliwiającego sprawniejszy kontakt między dyspozytorem, a kierowcą. 

Dyspozytor musi ręcznie wpisywać szczegóły zlecenia przez SMS i wysyłać je do konkretnego kierowcy, co bywa często bardzo czasochłonne i niewygodne. Przy przydzielaniu zleceń, musi on też pamiętać o tym, który kierowca jest dostępny, gdyż obecne narzędzie pokazuje jedynie lokalizację kierowców, bez informacji o tym, czy są w trakcie kursu. Powoduje to czasem, że proces znalezienia kierowcy do zlecenia trwa dłużej niż powinien. Dyspozytor musi także pamiętać o zgłoszonych przez kierowców przerwach, gdyż nie ma tego zapisanego w systemie. Zdarzają się sytuacje, że klienci zamawiając przejazd, pytają się o jego cenę. Dyspozytor wówczas samodzielnie musi dokonać obliczeń, gdyż nie istnieje system, który by go w tym wyręczył.

Kierowca musi ręcznie odpisywać na SMSy, potwierdzając zlecenie, a także informując o jego zakończeniu, co bywa bardzo czasochłonne i zabiera kierowcy czas, który mógłby sposiłkować na realizację kolejnego zlecenia. Jest to także dość niewygodne, ponieważ kierowca musi przełączać się między dwoma zewnętrznymi aplikacjami: do SMSów i do nawigacji, w czasie gdy jest w trakcie pracy. Kierowca musi ręcznie ustawiać nawigację, wpisując adresy otrzymane przez dyspozytora w wiadomości SMS, co również bywa uciążliwe, gdyż pochłania czas. Zdarzały się sytuacje, że kierowca błędnie przepisał adres podany od dyspozytora, przez co klient został obsłużony w błędny sposób. Taksometr, który podlicza na bieżąco wartość zamówienia jest dość starym urządzeniem, przez co zdarzają się jego usterki i ewentualne podliczenie ceny kursu wówczas spoczywa na barkach kierowcy, co czasem prowadzi do pewnych nieścisłości i pretensji ze strony klienta.

## Aktorzy i zewnętrzne systemy

* **Dyspozytor** - odbiera telefony od klientów i następnie ręcznie przekazuje informacje o otrzymanym zleceniu do wybranego kierowcy. Ma podgląd na mapę z aktualnymi lokalizacjami kierowców. Nadzoruje raporty finansowe z wykonanych przez firmę zleceń przewozu. Stanowi rolę pośrednika między kierowcą, a menedżerem oraz między kierowcą, a pasażerem.

* **Kierowca** - wykonuje zlecenia przewozów otrzymane przez dyspozytora. 

* **Google Maps** - znane oprogramowanie nawigacyjne mające szczegółowe dane lokalizacyjne

## Oczekiwany efekt projektu

Produkt będzie się składał z dwóch odrębnych aplikacji skomunikowanych ze sobą: internetowej przeznaczonej dla dyspozytorów oraz mobilnej dla kierowców. 

Za pomocą aplikacji internetowej, dyspozytor będzie mógł przesłać szczegóły zlecenia do kierowcy wpisując je w aplikacji, za pomocą komputera, co znacznie przyspieszy ten proces. Dzięki temu, dyspozytor nie będzie musiał ręcznie wybierać kierowcy, do którego wyśle zlecenie, gdyż aplikacja automatycznie będzie namierzać najbliższego dostępnego kierowcę na podstawie danych lokalizacyjnych. Dyspozytor w aplikacji będzie miał podgląd na mapę z lokalizacjami kierowców, gdzie w prosty i klarowny sposób będzie przedstawiony obecny status kierowcy, w tym informacja czy znajduje się on na przerwie. Przy dodawaniu zlecenia, system automatycznie podliczy cenę kursu.

W aplikacji mobilnej, kierowca będzie miał wbudowaną mapę, która będzie pobierana z Google Maps. Po otrzymaniu zlecenia, w aplikacji przyjdzie powiadomienie, gdzie kierowca będzie miał podgląd szczegółów zlecenia, w tym ceny przejazdu, a także możliwość przyjęcia, bądź odrzucenia zlecenia. Po akceptacji danego kursu, system automatycznie ustawia nawigację i ustawia w systemie status kierowcy jako zajętego. W przypadku chęci zgłoszenia przerwy lub jakiegokolwiek innego problemu, kierowca będzie miał możliwość zmienienia statusu lub wysłania odpowiedniej wiadomości do dyspozytora za pomocą aplikacji.

## Główne funkcje systemu

**Dyspozytor**:
* Logowanie
* Dodanie nowego zlecenia
* Wyświetlenie mapy z aktualnymi lokalizacjami kierowców
* Wyświetlenie listy dostępnych kierowców
* Wyświetlenie listy zajętych kierowców
* Wyświetlenie szczegółowych informacji o danym kierowcy
* Wyświetlenie szczegółowych informacji o danym zleceniu
* Wyświetlenie aktywnych zleceń
* Wyświetlenie historii zleceń
* Wyświetlenie uwag otrzymanych od kierowców


**Kierowca**:
* Logowanie
* Akceptacja zlecenia
* Odrzucenie zlecenia
* Zgłoszenie przerwy
* Zgłoszenie uwagi / usterki do dyspozytora
* Zakończenie obecnego kursu
* Anulowanie obecnego kursu
* Wyświetlenie historii swoich zleceń

**Google Maps**:
* Ustawienie nawigacji

**Pozostałe**:
* Przychodzenie powiadomień o nowym zleceniu
* Przychodzenie powiadomień o nowej wiadomości / nowych uwagach

## Ograniczenia i wymagania niefunkcjonalne
Oprogramowanie będzie kompatybilne z wieloma urządzeniami: będzie dostępna aplikacja mobilna dla kierowców, która działa zarówno na urządzeniach z systemem Android, jak i iOS. Aplikacja internetowa dla dyspozytorów będzie miała przejrzysty interfejs i będzie prosta w obsłudze. Mapy w aplikacji będą pobierane z serwerów Google Maps, dzięki czemu wszystkie funkcjonalności niezbędne do pracy dla kierowcy i dyspozytora będą dostępne w ramach jednego oprogramowania.