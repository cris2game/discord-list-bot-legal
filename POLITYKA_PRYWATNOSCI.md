# Polityka prywatności — Discord List Bot

**Data wejścia w życie:** [15-10-2026]  
**Ostatnia aktualizacja:** [16-10-2026]

## 1. Administrator danych i kontakt

Administratorem danych osobowych przetwarzanych w związku z obsługą Discord List Bota jest **cris2game** („Administrator”).

## 2. Zakres Polityki

Polityka opisuje przetwarzanie danych w związku z korzystaniem z bota Discord **Discord List Bot**, który pozwala tworzyć, publikować, edytować, odhaczać i usuwać listy na serwerach Discord.

Discord jest odrębną platformą, która przetwarza dane zgodnie z własnymi dokumentami i zasadami. Niniejsza Polityka dotyczy danych przetwarzanych przez Administratora za pośrednictwem instancji Bota, w zakresie opisanym poniżej.

## 3. Jakie dane są przetwarzane

W zależności od sposobu korzystania z Bota mogą być przetwarzane:

- **Treść list:** nazwa listy, jej elementy oraz informacja, które elementy zostały odhaczone.
- **Identyfikatory techniczne Discord:** identyfikatory serwera, kanału, wiadomości i inne identyfikatory wiadomości potrzebne do aktualizacji lub usuwania list.
- **Dane techniczne sesji tworzenia listy:** treść wiadomości przesyłanych w celu dodania elementów, identyfikatory wiadomości źródłowych i kanału, w którym rozpoczęto tworzenie listy.
- **Dane interakcji:** informacje niezbędne do obsługi komend aplikacji i przycisków. Kod Bota nie zapisuje w bazie nazw użytkowników ani identyfikatorów użytkowników jako pól listy, ale Discord może przetwarzać takie informacje w ramach działania platformy i interakcji.
- **Dane diagnostyczne:** w konsoli mogą pojawić się komunikaty o błędach i identyfikatory wiadomości lub kanałów. Zakres dodatkowych logów zależy od konfiguracji środowiska, w którym uruchomiono Bota.

Nie należy umieszczać w listach danych wrażliwych, haseł, danych płatniczych ani innych informacji poufnych, które nie są niezbędne do działania listy.

## 4. Cele i podstawy przetwarzania

Dane są przetwarzane w celu:
1. tworzenia, publikowania, wyświetlania, aktualizowania i usuwania list;
2. zapisywania stanu wykonania list i przywracania obsługi przycisków po restarcie Bota;
3. rozpoznawania serwera i kanału, do których należy lista, oraz zapobiegania mieszaniu list pomiędzy serwerami;
4. diagnozowania błędów i utrzymania bezpieczeństwa oraz stabilności usługi;
5. rozpatrywania zapytań dotyczących usługi i prywatności.

## 5. Sposób i miejsce przechowywania

1. Kod Bota zapisuje dane list w lokalnej bazie SQLite.
2. Baza zawiera nazwy list, elementy, stan odhaczenia, stronę listy oraz identyfikatory wiadomości, kanałów i serwerów.
3. Faktyczna lokalizacja pliku bazy zależy od konfiguracji i miejsca uruchomienia Bota.

## 6. Wiadomości używane do utworzenia listy

Po uruchomieniu komendy `/lista` Bot odczytuje treść wiadomości użytkownika wysyłanych na tym samym kanale w celu zebrania elementów listy. Treść jest dzielona na elementy, a pojedynczy element jest ograniczany do 80 znaków.

Po opublikowaniu listy Bot próbuje usunąć wiadomości źródłowe użyte do jej utworzenia. Jeśli użytkownik anuluje tworzenie listy, Bot również próbuje usunąć zebrane wiadomości źródłowe. Usunięcie zależy od uprawnień Bota i możliwości Discord. Nie należy zakładać, że wiadomości zostały usunięte, jeśli operacja się nie powiedzie.

## 7. Odbiorcy danych

Dane mogą być przetwarzane lub udostępniane w zakresie niezbędnym do działania usługi:
- platformie Discord, która obsługuje komunikację, komendy, kanały i wiadomości;
- osobom upoważnionym przez Administratora do utrzymania i zabezpieczenia Bota.

## 8. Okres przechowywania

- Dane list są przechowywane w bazie tak długo, jak dana lista istnieje i jest potrzebna do działania Bota, chyba że zostaną wcześniej usunięte.
- Po usunięciu listy odpowiedni wpis w bazie jest usuwany przez Bota. Jeśli nie uda się usunąć powiązanej wiadomości z Discord, może ona nadal istnieć na platformie.
- Wiadomości źródłowe zebrane podczas tworzenia listy są usuwane przez Bota, gdy operacja usuwania jest możliwa.

## 9. Dane osób niepełnoletnich

Bot działa na platformie Discord. Użytkownicy powinni przestrzegać zasad Discord dotyczących wieku i korzystania z usługi. Administrator nie kieruje Bota celowo do dzieci i prosi, aby nie umieszczać na listach danych dzieci, jeśli nie jest to konieczne i nie ma odpowiedniej podstawy prawnej.

## 10. Zmiany Polityki

Polityka może być aktualizowana w przypadku zmian funkcjonalności Bota, infrastruktury lub obowiązujących przepisów. Aktualna wersja będzie publikowana pod adresem **https://github.com/cris2game/discord-list-bot-legal/blob/main/POLITYKA_PRYWATNOSCI.md**. Data ostatniej aktualizacji znajduje się na początku dokumentu.
