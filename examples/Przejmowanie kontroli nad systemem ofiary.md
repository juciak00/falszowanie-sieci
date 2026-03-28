Przejmowanie kontroli nad systemem ofiary


           Krzysztof Pietrucha
            Andrzej Kozłowski
             Kacper Majcher
           Michał Włodarczyk


---


Spis treści:
1. Przejmowanie systemu ofiary za pomocą sieci (Krzysztof Pietrucha)
   1.1.      Wprowadzenie
   1.2.      Badanie systemu ofiary
   1.3.      Włamanie do sieci WIFI
   1.4.      Ataki na warstwę aplikacji
   1.5.      Zabezpieczenia sieci
2. Definicje i kontekst ataków DDoS (Kacper Majcher)
   2.1.      Wyjaśnienie kluczowych pojęć związanych z atakami DDoS
   2.2.      Typy ataków DDoS i ich różnice
   2.3.      Metody przeprowadzania ataków DDoS
   2.4.      Wpływ ataków DDoS na infrastrukturę
   2.5.      Przykłady i studia przypadków
   2.6.      Zapobieganie i ochrona przed atakami DDoS
   2.7.      Podsumowanie i wnioski
3. Ogólne wprowadzenie (phishing, ransomware, socjotechnika oraz
   bezpieczeństwo aplikacji internetowych) (Andrzej Kozłowski)
   3.1.      Cel i zakres projektu
   3.2.      Zagrożenia phishingowe
   3.3.      Ransomware - Analiza, zabezpieczenia i strategie ochronne
   3.4.      Social Engineering
   3.5.      Bezpieczeństwo aplikacji internetowych
   3.6.      Bezpieczna wymiana informacji - rola kryptografii
   3.7.      Social Engineering w praktyce
4. Wirusy przejmujące kontrolę systemu (Michał Włodarczyk)
   4.1.      Trojany
   4.2.      Rodzaje Trojanów
   4.3.      Ochrona przed Trojanami
   4.4.      Black Bastia
   4.5.      Krypta 7 (Vault 7)
   4.6.      Część 1 - "Rok Zero"
   4.7.      Najpopularniejsze rodzaje Trojanów / wirusów
   4.8.      Watykańczyk
   4.9.      Podsumowanie i wnioski


---


1.1 Wprowadzenie

Wraz z dynamicznym rozwojem sieci komputerowych i coraz większym
znaczeniem internetu w dzisiejszym świecie, korzystanie z sieci stało się
nieodłączną częścią naszego życia codziennego. Sieci komputerowe zapewniają
nam niezliczone możliwości komunikacji, dostępu do informacji oraz interakcji z
technologią na wielu poziomach. Jednakże, w miarę jak nasza zależność od sieci
rośnie, tak samo rośnie również ryzyko związane z cyberatakami i naruszeniami
bezpieczeństwa danych.

Zagrożenia związane z cyberprzestępczością są coraz bardziej wyrafinowane i
niebezpieczne. Ataki cybernetyczne mogą prowadzić do kradzieży danych,
utraty poufności informacji, zakłóceń w działaniu systemów informatycznych
oraz szkód finansowych i reputacyjnych dla firm i użytkowników. W miarę jak
technologie stają się coraz bardziej zaawansowane, tak samo rosną
umiejętności i zasoby dostępne dla cyberprzestępców, co sprawia, że są one
bardziej groźne i trudniejsze do wykrycia.

W tej prezentacji skupimy się na omówieniu różnych technik wykorzystywanych
przez cyberprzestępców do przejęcia systemów ofiar za pomocą sieci.
Przeanalizujemy różne metody ataków, ich mechanizmy działania oraz skutki dla
użytkowników i organizacji. Ponadto przyjrzymy się również środkom obronnym
i strategiom zapobiegania atakom, które mogą pomóc w zwiększeniu
bezpieczeństwa naszych systemów informatycznych w obliczu stale
ewoluującego zagrożenia cyberprzestępczością.




1.2 Badanie systemu ofiary


---


Badanie systemu ofiary zazwyczaj rozpoczyna się od zbierania informacji o
infrastrukturze, takich jak adresy IP i otwarte porty. Następnie przeprowadza się
skanowanie w poszukiwaniu podatności, a po ich zidentyfikowaniu atakujący
próbuje wykorzystać je w celu uzyskania dostępu do systemu, dokumentując
każdy krok tego procesu dla analizy i raportowania.



a) Program do Skanowania Sieci:

- Advanced IP Scanner jest narzędziem o dużej wydajności i darmowym
dostępie, stworzonym z myślą o skanowaniu sieci. Pozwala na szybką
identyfikację wszystkich urządzeń w sieci oraz umożliwia łatwe nawiązanie z
nimi kontaktu. Dzięki niemu użytkownik może wygodnie zarządzać zdalnymi
komputerami, kontrolując ich działanie i łącząc się z nimi za pomocą aplikacji
jednym kliknięciem.




- LAN scaner to mocno podstawowe narzędzie do skanowania urządze w sieci
dzięki któremu możemy poznać nazwę urządzenia, adres IP i MAC. Program


---


łatwy w instalacji na system operacyjny Windows. Dzięki temu programowi
dowiemy się również czy urządzenie jest aktualnie włączone.




- PortScan & Stuff to program z naprawdę mocnymi elementami takimi jak:

   • Skanowanie urządzeń posiadające kartę sieciową oraz otwarte porty i
      różne ich dane techniczne.
   • Pingowanie (testowanie połączenia).
   • Śledzenie trasy np. do serwera 8.8.8.8 (www.google.com). W moim
      przypadku zapytanie przeszło przez 9 serwerów DNS.
   • Testowanie prędkości połączenia podawane w MByte/sec.
   • A także informacje domenowe, adres publiczny, nazwa urządzenia i
      posiadane karty oraz ich specyfikacja.


---


b) Weryfikacja portów:


---


Jednym z zagrożeń płynących od strony naszego routera są otwarte porty przez
które haker może dostać się do ukrytych danych. Programem, który po wejściu
do sieci ofiary pokaże nam wszystkie otwarte porty jest CurrPorts.




Dzięki temu programowi możemy odczytać wszystkie otwarte porty, czego one
dotyczą i jakie usługi się z tym łączą. Narzędzie bardzo ładnie wyświetla dane i z
poziomu systemu ofiary ciężko to zablokować. Oczywiście większość firm
otwiera tylko te porty, które nie narażają jej na atak z oczywistych względów.
Bywają przypadki, gdzie firma korzystała z jakiegoś programu i z biegiem czasu
został wyłączony jednak porty nie zostały zablokowane.

Innym sposobem i na pewno bardziej stosowanym przez profesjonalistów jest
pozyskiwanie informacji przez wiersz poleceń (CMD) i komendę „netstat”.
Polecenie, które pokaże nam informacje o portach jest „netstat -aon”. Dopisek
„-aon” pozwoli nam wyświetlić informacje o zajętych portach wraz z ich


---


identyfikatorem. Dzięki wyświetleniu statusu portu uzyskujemy informację o
tym co nasz komputer/serwer robi na tym porcie.

-LISTENING – serwer oczekuje na przyjęcie połączenia.

-ESTABILISHED – serwer odesłał pakiet do klienta i połączenie zostało
zestawione.

-CLOSE_WAIT – serwer otrzymał pakiet od klienta




c) informacje z adresu IP

Bardzo duża część ludzi myśli, że adres IP to tylko nazwa potrzebna do
komunikacji. Niestety adres IP mówi bardzo dużo o nas, na przykład:
-nasza geolokalizacja


---


-dostawca internetu
-rodzaj sieci (domowa, firmowa, publiczna itp.)
-ilość urządzeń w sieci

W większych firmach wskazane jest dzielenie sieci na Vlany, utrudnia to
skuteczny atak hakerów, ale również oddziela ważniejsze elementy
infrastruktury od dostępu reszty użytkowników.

Częstym modelem firmy jest:

-sieć publiczna, na przykład dla gości darmowe wifi lub miejsce, w którym
niema dostępu do dysków sieciowych lub połączenia do wirtualnych maszyn. W
tym przypadku możemy się dowiedzieć z jakich urządzeń jest zbudowana i z
jakiego UTM korzysta.

-sieć firmowa, tutaj działa większość firmy i to na tej sieci zależy nam najbardziej
jak chcemy zablokować funkcjonalność firmy. W tym segmencie możemy
sprawdzić aplikacje z dostępem do sieci publicznej oraz tych offline, czyli na
przykład systemów dokumentacji, ERP oraz innych używanych przez daną
specjalizację firmy.

-sieć produkcyjna, zazwyczaj jest to Vlan bez do dostępu do internetu oraz
systemów takich jak DHCP, DNS. Służy do komunikacji produkcji tak aby firma
nie straciła swoich informacji o produkcji lub nie była wystawiona na zakłócenia
płynące ze strony sieci firmowej/publicznej.

-sieć zarządu, tego typu sieć służy do zabezpieczenia najważniejszych decyzji
podejmowanych przez firmę. Działa na tej samej zasadzie co sieć firmowa
jednak jest mocno mniejsza.


---


Z tych wszystkich typów sieci haker największy zysk uzyskuje po włamaniu się
do sieci firmowej i wykradnięciu danych wrażliwych firmy.



1.3 Włamanie do sieci wifi ofiary

Jednym z najłatwiejszych sposobów na wejście do sieci ofiary jest włamanie do
WiFi. Ma to swoje plusy i minusy. Plusem jest fakt, że aktualne standardy
zabezpieczeń na rynku światowym są łatwe do złamania. Odpowiada za to
szyfrowanie, najczęściej jest to WPA2, chociaż coraz więcej firm zaczyna
przechodzić na WPA3, które jest aktualnie nie do złamania (według mojej
wiedzy technicznej). WPA2 powstało w okolicach 2006 roku, a to świadczy o
swoim wypaleniu i ilości prób złamania. WPA3 zostało wdrożone na przestrzeni
ostatnich kilku lat i póki co jest mniej popularne niż jego poprzednik. Minusem
jest fakt, że taki atak nie bez powodu jest nazywany „Man-in-the-Middle”
(MITM). Polega on na manipulowaniu istniejącymi sieciami lub tworzeniu
złośliwych sieci kontrolowanych przez cyberprzestępcę na miejscu lub w okolicy.
Tego nie jesteśmy w stanie zrobić z domu lub innego kraju, musimy być blisko
siedziby ofiary, aby było to maksymalnie skuteczne. Oczywiście możemy
również wykraść hasło do WiFi po przejściu zabezpieczeń UTM’a i włamaniu się
do domeny ofiary, ale jest to o wiele dłuższa droga. Do włamania się w siedzibie
ofiary do WiFi wystarczy laptop/komputer i karta sieciowa ważne, aby była to
mocna karta sieciowa, najlepiej zewnętrzna z anteną, aby móc w szybki i
wygodny sposób nawiązać mocny kontakt z Access
Pointem/modemem/routerem. Na urządzeniu osoby włamującej się, zaleca się
odmianę Linuksa o nazwie „Kali”. Jest to najpopularniejszy i darmowy system o
bardzo dużym wachlarzu narzędzi do łamania zabezpieczeń i testów
penetracyjnych. Jako odmiana Linuksa, hakerzy zazwyczaj używają tylko konsoli,


---


jest to zaawansowany sposób korzystania z systemu, który nie jest łatwy dla
zwykłych ludzi.



Wygląd systemu:


---


Zainstalowane domyślnie aplikacje hakowania sieci:




Górna część systemu to bardzo podobna struktura do paska zdań systemu
Windows. W dolnym prawym rogu możemy zobaczyć konsole razem z komendą
„ifconfig” która wyświetla informacje o kartach sieciowych. W moim przypadku
jest to wirtualna maszyna utworzona przez program Hyper-V.


---


a) Programem, który będzie używany do ataku na sieć WiFi ofiary, jest „wifite”.
Na początku instalujemy aplikację za pomocą poleceń „sudo apt-get install
wifite” lub w zależności od wersji obrazu systemu, może być ona już
zainstalowana domyślnie. Oczywiście może się zdarzyć, że będziemy
potrzebować pewnych plików. W takim przypadku musimy sprawdzić, czego
nam brakuje i dokonać odpowiedniej instalacji.

Po zainstalowaniu programu uruchamiamy komendę z uprawnieniami roota
„sudo wifite”. Program automatycznie na starcie rozpocznie wyszukiwanie
dostępnych sieci oraz ich parametrów, takich jak: nazwa, kanał, typ
zabezpieczeń, zasięg i liczba połączonych urządzeń.


---


Po zakończeniu wyszukiwania sieci program poprosi nas o wybór, którą
konkretnie sieć chcemy zaatakować. Oczywiście możemy wybrać kilka sieci na
raz. Po krótkiej chwili program powie czy się udało. Typów ataków jest wiele i
możemy je wybierać dowolnie na przykład atakowanie pinem, słownikiem itp.
Atak słownikowy to nic innego jak wgranie na naszą maszynę pliku na przykład z
wycieków danych, które posiadają tysiące haseł używanych w różnych
lokalizacjach.

Gdy program zakończy atakowanie wyświetli nam hasło w ostatniej linijce na
samym końcu.




W przypadku gdy nasz słownik nie uzyska hasła od ofiary, możemy go zmienić
poleceniem „sudo wifite –dict /ścieżka do lokalizacji naszego słownika.txt”.


---


Spis wszystkich komend programu wifite:




- Obrona przed przejęciem kontroli

Oczywiście firmy/ofiary mogą się przed tym zabezpieczyć na przykład długim
hasłem. Najlepiej, aby takie hasło składało się z minimum 15 znaków, znaków
specjalnych przekładanymi liczbami i słowami z wstawionymi w różnych
miejscach dużymi lub małymi literami.


---


Oczywiście programów do łamania haseł jest wiele i będą nadal powstawać.
Inne programy do łamania haseł:

-Aircrack-ng, mocno podstawowe narzędzie.

-Reaver, program ten potrafi śmiało łamać zabezpieczenia WPA/WPA2.
Potrzebuje dłuższego czasu i mocniejszej anteny, ale dojdzie do skutku.


---


-Fern WIFI Craker, prosty program graficzny, który pozwala nam na wybór karty
sieciowej a następnie zaczyna prosty atak.




-Wireshark, kolejny program graficzny, pozwala na śledzenie ruchu, protokołów
i pakietów na żywo oraz ich filtrowanie. Możliwa instalacja na systemy
Windows. Do wyboru mamy nie tylko atak na sieć wifi a również lokalne
połączenie internetowe, ruch na switchu i połączenie Bluetooth. Program ten


---


pokazuje wyniki na żywo z możliwością ich zapisu.




1.4 Ataki na warstwę aplikacji

a) atak SQL injection

SQL injection to jedna z częstych i niebezpiecznych podatności w aplikacjach
webowych i nie webowych. Nie bez powodu znajduje się w pierwszej (A1)
kategorii błędów według OWASP Top Ten. Nazwa sama wskazuje na problem –
atakujący wstrzykuje nieautoryzowany fragment zapytania SQL. Wstrzyknięcie
jest możliwe głównie przez brak odpowiedniej walidacji parametru
przekazanego przez użytkownika, który często jest bezpośrednio przekazywany
do zapytania SQL.

Skutki mogą być różne, w tym:
-Nieautoryzowany dostęp do bazy danych w trybie odczytu lub zapisu.
-Ominięcie mechanizmu uwierzytelnienia.
-Odczytanie wybranych plików z systemu operacyjnego, na którym działa baza


---


danych.
-Tworzenie plików w systemie operacyjnym.
-Wykonanie kodu w systemie operacyjnym.

Przykład praktyczny:
Wyobraźmy sobie prostą aplikację napisaną w PHP, komunikującą się z bazą
danych MySQL. Normalnie wyświetlanie newsa odbywa się poprzez odwołanie
do URL-a z określonym ID. Jednakże, modyfikując wartość zmiennej ID w
adresie URL, można uzyskać nieautoryzowany dostęp do danych bazy, odczytać
funkcje bazodanowe czy pobierać dane z innych tabel niż oryginalna. Przy braku
odpowiedniej walidacji, atakujący może także ominąć mechanizm
uwierzytelnienia, uzyskując nieautoryzowany dostęp do kont użytkowników, jak
pokazuje przykład logowania na użytkownika 'admin' bez znajomości hasła.



b) Atak Cross-Site Scripting (XSS)

Cross-Site Scripting (XSS) jest jednym z tych problemów, które znalazły swoje
miejsce w każdym zakamarku internetowej dyskusji o bezpieczeństwie. Jest to
również często tematem żartów w środowisku osób zajmujących się
bezpieczeństwem IT. Chociaż wydawać by się mogło, że o XSS napisano już
wszystko, to warto zwrócić uwagę na jego znaczenie w kontekście aktualnych
zagrożeń.

XSS zajmuje wysoką, trzecią pozycję na liście najbardziej aktualnych zagrożeń
według OWASP Top Ten. Dlatego warto bliżej przyjrzeć się tej podatności.

Podatność XSS polega na wstrzyknięciu fragmentu kodu JavaScript lub innego
języka skryptowego do przeglądarki ofiary. Skutkiem tego ataku jest możliwość


---


uruchomienia dowolnego kodu skryptowego w przeglądarce, co otwiera drogę
do różnych niepożądanych konsekwencji.

Możliwe skutki ataku XSS są różnorodne, począwszy od kradzieży sesji
użytkownika poprzez wykradanie ciasteczek, po zmianę zawartości stron
internetowych na niepożądane treści czy nawet uruchomienie keyloggera w
przeglądarce.

Błędy XSS można podzielić na trzy główne kategorie:

-Persistent (stored) XSS - najbardziej niebezpieczna forma, gdzie kod JavaScript
jest przechowywany po stronie serwera. To właśnie ta forma pozwala na
przejęcie sesji użytkownika bez znajomości hasła.

-Reflected XSS - kod JavaScript jest przesyłany do aplikacji za pomocą linku,
który następnie zostaje zwrócony przez aplikację w odpowiedzi, co skutkuje
wykonaniem kodu w przeglądarce.

-DOM Based XSS - mniej powszechna forma ataku, opisana w powyższym
tekście



1.5 Zabezpieczanie sieci

Firewall (Zapora sieciowa) - Zapora sieciowa działa jak strażnik, kontrolując
ruch wchodzący i wychodzący z sieci. Na przykład, jeśli pracownik próbuje
uzyskać dostęp do nieodpowiedniej strony internetowej podczas pracy, zapora
sieciowa może zablokować tę próbę dostępu na podstawie zdefiniowanych
reguł. Z drugiej strony, jeśli zewnętrzny atakujący próbuje uzyskać dostęp do
wrażliwych danych firmy, zapora sieciowa może zablokować te próby.


---


Antywirus - Programy antywirusowe działają przez skanowanie plików i
programów na obecność znanego złośliwego oprogramowania. Na przykład,
jeśli użytkownik pobiera plik z Internetu, program antywirusowy może
automatycznie przeskanować ten plik w poszukiwaniu znanego złośliwego
oprogramowania. Jeśli coś zostanie wykryte, program antywirusowy powiadomi
użytkownika i podjąć odpowiednie działania, takie jak usunięcie pliku lub
umieszczenie go w kwarantannie.



Szyfrowanie - Szyfrowanie jest procesem przekształcania czytelnych danych w
ciąg znaków, które są niezrozumiałe bez odpowiedniego klucza. Na przykład,
jeśli firma przesyła wrażliwe dane klienta przez Internet, te dane mogą być
szyfrowane, aby tylko osoba z odpowiednim kluczem mógła je odczytać. To
zapewnia, że nawet jeśli dane zostaną przechwycone, atakujący nie będzie mógł
ich zrozumieć.



   2. Definicje i kontekst ataków DDoS


Ataki DDoS, czyli ataki typu Distributed Denial of Service, stanowią jedno z
największych zagrożeń dla współczesnej infrastruktury internetowej. Są to ataki,
które polegają na przeciążeniu serwera, sieci lub systemu do tego stopnia, że
nie są one w stanie obsłużyć prawidłowego ruchu sieciowego.
Mówiąc prościej, ataki DDoS to sytuacja podobna do tej, kiedy ktoś blokuje
wejście do sklepu, wysyłając tam tłum ludzi, którzy nie mają zamiaru nic kupić,
tylko przeszkadzać. W ten sposób prawdziwi klienci nie mogą dostać się do
sklepu i zrobić zakupów.
Ataki DDoS mogą mieć różne cele i motywy, takie jak szantaż, sabotaż, protest
lub zwykła złośliwość.


---


Ewolucja ataków DDoS
Ataki Distributed Denial of Service ewoluowały wraz z postępem technologii.
Początkowo były stosunkowo proste i polegały na zasypywaniu serwera
ogromną ilością żądań, co prowadziło do jego przeciążenia.
Jednak wraz z rozwojem technologii, ataki DDoS stały się bardziej
zaawansowane, wykorzystując różne metody i techniki, aby uniknąć detekcji i
zwiększyć swoją skuteczność.


Znaczenie ataków DDoS dla współczesnej infrastruktury internetowej
Ataki te mają ogromne znaczenie dla współczesnej infrastruktury internetowej.
Mogą one powodować poważne zakłócenia w działaniu stron internetowych,
usług online i sieci, co może prowadzić do znacznych strat finansowych.
Ponadto, ataki Distributed Denial of Service mogą być wykorzystywane jako
narzędzie do przeprowadzania działań cyberprzestępczych, takich jak kradzież
danych osobowych lub finansowych, czy nawet samych finansów.
Należy jednak pamiętać, że ataki DDoS stanowią również zagrożenie dla
bezpieczeństwa narodowego i międzynarodowego. Mogą one być używane do
paraliżowania kluczowych instytucji, takich jak rządy, wojsko, służby zdrowia czy
media.
Przykładem takiego ataku jest atak na Estonię w 2007 roku, który sparaliżował
wiele stron rządowych i bankowych, a także uniemożliwił dostęp do mediów i
usług komunikacyjnych. Ataki mogą być również wykorzystywane do eskalacji
konfliktów lub wojen cybernetycznych między państwami lub grupami, czego
przykładem jest atak na Iran w 2019 roku, który miał na celu zakłócenie systemu
radarowego i obrony powietrznej kraju.




Konsekwencje ataków DDoS
Ataki DDoS, czyli rozproszone ataki odmowy usługi, polegają na zalewaniu
serwerów lub sieci ogromną ilością zapytań, które uniemożliwiają prawidłowe
funkcjonowanie usług lub zasobów online. Ataki te mogą mieć poważne


---


konsekwencje dla różnych sektorów, zarówno pod względem ekonomicznym,
społecznym, jak i politycznym.
W sektorze biznesowym, ataki DDoS mogą prowadzić do utraty dochodów,
szkód wizerunkowych i utraty zaufania klientów. W 2016 roku atak DDoS na
serwery firmy Dyn, która dostarczała usługi DNS dla wielu popularnych stron
internetowych, spowodował niedostępność takich serwisów jak Twitter, Netflix,
Spotify czy Amazon. Szacuje się, że atak ten kosztował firmy ponad 110
milionów dolarów.
W sektorze edukacji, ataki DDoS mogą zakłócać dostęp do platform e-
learningowych i innych zasobów online, co może utrudniać proces nauczania i
uczenia się. W 2020 roku atak DDoS na serwery Zoom, które były
wykorzystywane przez wiele szkół i uczelni do zdalnego nauczania, spowodował
przerwy w zajęciach i frustrację zarówno nauczycieli, jak i uczniów.
W sektorze usług online, ataki DDoS mogą powodować przerwy w dostępie do
usług, co może prowadzić do frustracji użytkowników i utraty zaufania. Co w
2017 roku pokazał atak DDoS na serwery PlayStation Network, które
umożliwiały grę online na konsolach PlayStation, spowodował niedostępność
usługi dla milionów graczy na całym świecie.
Ataki DDoS jednocześnie mogą mieć konsekwencje dla bezpieczeństwa
osobistego i prywatności. Mogą one umożliwić atakującym dostęp do
wrażliwych danych, takich jak hasła, numery kart kredytowych, dane medyczne
czy lokalizacja. Mogą one również naruszać prawa człowieka, takie jak wolność
słowa, dostęp do informacji czy prawo do pokojowego zgromadzania. Atak na
Telegram w 2019 roku, który miał na celu uniemożliwić komunikację opozycji w
Hongkongu był tego świetnym przykładem. Prawdopodobnie został on zlecony
przez rząd chiński, który chciał stłumić protesty w Hongkongu.
Ataki DDoS stanowią więc poważne zagrożenie dla stabilności i bezpieczeństwa
cyfrowego. Aby się przed nimi chronić, należy stosować odpowiednie środki
zapobiegawcze, takie jak zabezpieczenia firewall, filtrowanie ruchu,
monitorowanie aktywności sieciowej czy korzystanie z usług specjalizowanych
firm, które oferują ochronę przed atakami DDoS. O tym w dalszej części
artykułu.


2.1 Wyjaśnienie kluczowych pojęć związanych z atakami DDoS


---


I. Botnety: zagrożenie dla internetu rzeczy

Internet rzeczy (IoT) to termin, który odnosi się do połączenia różnych urządzeń
elektronicznych z internetem, takich jak kamery, routery, termostaty, żarówki,
lodówki czy samochody. IoT ma wiele zalet, takich jak zdalna kontrola,
automatyzacja, monitorowanie czy komunikacja. Jednak IoT ma także wiele
wad, zwłaszcza pod względem bezpieczeństwa.

Jednym z największych zagrożeń dla IoT są botnety, czyli sieci zainfekowanych
komputerów, które są zdalnie kontrolowane przez atakującego.

Komputery te, zwane botami, są często zainfekowane przez malware, czyli
złośliwe oprogramowanie, które pozwala atakującemu na kontrolę nad nimi.
Atakujący może następnie wykorzystać te boty do przeprowadzenia ataku DDoS,
polegającego na wysyłaniu ogromnej ilości ruchu do celu, takiego jak strona
internetowa, serwer czy usługa. Atak może spowodować przeciążenie,
spowolnienie lub całkowite wyłączenie celu, co może mieć poważne
konsekwencje dla użytkowników, właścicieli lub dostawców.

Przykładem takiego ataku jest botnet o nazwie Mirai, który przeprowadził jeden
z największych ataków DDoS w historii, paraliżując wiele dużych stron
internetowych, w tym Twitter, Netflix i CNN. Mirai wykorzystał setki tysięcy
zainfekowanych urządzeń IoT, takich jak kamery internetowe i routery, do
przeprowadzenia ataku. Mirai był w stanie zainfekować te urządzenia, ponieważ
wykorzystywał domyślne lub słabe hasła dostępu do nich. Mirai nie był jedynym
botnetem, który atakował IoT. Inne przykłady to BASHLITE, Reaper, Hajime czy
Satori.



Jak więc można się bronić przed botnetami i zwiększyć bezpieczeństwo IoT?

Oto kilka wskazówek:

Zmieniaj domyślne lub słabe hasła dostępu do swoich urządzeń IoT na silne i
unikalne. Używaj kombinacji liter, cyfr i znaków specjalnych. Nie używaj tego
samego hasła do różnych urządzeń lub kont.

Aktualizuj oprogramowanie swoich urządzeń IoT regularnie, aby naprawiać
ewentualne luki bezpieczeństwa. Sprawdzaj, czy producent urządzenia oferuje


---


aktualizacje i jak je instalować. Unikaj używania urządzeń, które nie są
aktualizowane lub nie mają wsparcia technicznego.

Wyłącz lub ogranicz dostęp do niepotrzebnych funkcji lub usług swoich
urządzeń IoT, takich jak zdalny dostęp, telnet, SSH czy FTP. Te funkcje mogą być
wykorzystane przez atakującego do zdobycia kontroli nad urządzeniem. Używaj
tylko tych funkcji, których naprawdę potrzebujesz i odpowiednio je zabezpiecz.

Używaj zapor sieciowych, antywirusów i innych narzędzi ochronnych, aby
chronić swoje urządzenia przed malware i innymi zagrożeniami. Skanuj swoje
urządzenia regularnie i usuwaj wszelkie podejrzane pliki lub programy. Nie
otwieraj podejrzanych linków, załączników lub wiadomości, które mogą
zawierać malware.

Bądź świadomy ryzyka związanego z IoT i edukuj się na temat bezpieczeństwa.
Śledź aktualne wiadomości i raporty na temat botnetów i ataków DDoS. Znajdź
wiarygodne źródła informacji i porad na temat bezpieczeństwa IoT. Nie ufaj
ślepo wszystkiemu, co widzisz lub słyszysz w internecie.

Aby zapobiec botnetom i zwiększyć bezpieczeństwo IoT, należy podjąć
odpowiednie środki ostrożności i dbać o higienę cyfrową.



II. IP Spoofing: metoda oszukiwania sieci

IP Spoofing to technika, która polega na fałszowaniu adresu IP źródłowego w
pakietach sieciowych, aby ukryć prawdziwe źródło ataku.

Adres IP to unikalny identyfikator, który przypisany jest każdemu urządzeniu
podłączonemu do internetu. Pozwala on na lokalizację i komunikację między
urządzeniami. Adres IP jednak może być wykorzystany do śledzenia i
blokowania niepożądanego ruchu.

Atakujący może fałszować adresy IP, aby wyglądało na to, że ruch pochodzi z
wielu różnych miejsc, co utrudnia obronę. Na przykład, atakujący może wysyłać
pakiety z fałszywymi adresami IP do serwera DNS, który jest odpowiedzialny za
tłumaczenie nazw domenowych na adresy IP. Serwer DNS może następnie
odesłać pakiety do prawdziwego celu ataku, zwiększając ilość ruchu i
obciążenie. Taka technika nazywa się amplifikacją ruchu i jest często
wykorzystywana w połączeniu z IP spoofingiem.


---


Przykładem takiego ataku jest atak na Spamhaus w 2013 roku, który był jednym
z największych ataków DDoS w historii. Atakujący wykorzystali IP spoofing do
przeprowadzenia ataku DDoS na skalę, która przekroczyła 300 Gb/s, co jest
równoważne przesyłaniu 18 milionów filmów HD na sekundę. Atak spowodował
poważne zakłócenia w działaniu internetu na całym świecie, wpływając na wiele
stron i usług. Atak był skierowany przeciwko Spamhaus, organizacji zajmującej
się zwalczaniem spamu i cyberprzestępczości. Atakujący byli niezadowoleni z
tego, że firma umieściła ich na czarnej liście jako źródło spamu.

Ciekawostka jest, że IP spoofing nie jest jedyną metodą oszukiwania sieci. Inne
metody to na przykład ARP spoofing, DNS spoofing czy HTTPS spoofing.
Wszystkie te metody polegają na podszywaniu się pod inny adres, serwer lub
protokół, aby wprowadzić w błąd odbiorcę lub ofiarę.

Jak więc można się bronić przed IP spoofingiem i innymi metodami
oszukiwania sieci?

Oto kilka wskazówek:

Używaj szyfrowania i uwierzytelniania, aby chronić swoje dane i komunikację.
Używaj protokołów, które zapewniają bezpieczeństwo i prywatność, takich jak
HTTPS, SSL, TLS czy VPN. Nie ufaj niezaszyfrowanym lub nieuwierzytelnionym
połączeniom lub wiadomościom.

Używaj filtrów i firewalli, aby monitorować i blokować podejrzany ruch. Używaj
narzędzi, które mogą wykrywać i zapobiegać IP spoofingowi, takich jak egress
filtering, ingress filtering czy reverse path forwarding. Nie pozwól na przesyłanie
pakietów z fałszywymi lub niezgodnymi adresami IP.

Używaj aktualnego i legalnego oprogramowania, aby chronić się przed
malwarem i innymi zagrożeniami. Malware to złośliwe oprogramowanie, które
może infekować i przejąć kontrolę nad twoim urządzeniem. Malware może być
wykorzystany do fałszowania adresów IP tak, jak w przypadku botnetu!

Bądź świadomy ryzyka związanego z oszukiwaniem sieci i edukuj się na temat
bezpieczeństwa. Śledź aktualne wiadomości i raporty na temat IP spoofingu i
innych metod oszukiwania sieci. Znajdź wiarygodne źródła informacji i porad na
temat bezpieczeństwa sieciowego. Bądź czujny online - nie wszystko, co widzisz
czy słyszysz, zasługuje na pełne zaufanie.


---


Podsumowując, IP spoofing to metoda, która polega na fałszowaniu adresu IP
źródłowego w pakietach sieciowych, aby ukryć prawdziwe źródło ataku. IP
spoofing może być wykorzystany do przeprowadzania ataków DDoS lub innych
celów. Aby zapobiegać IP spoofingowi i innym metodom oszukiwania sieci,
należy podjąć odpowiednie środki ostrożności i dbać o higienę cyfrową.



      III.    Traffic Amplification: sposób na zwiększenie mocy ataku

Traffic Amplification to technika, która polega na wykorzystaniu odpowiedzi na
małe żądania do generowania dużego ruchu. Atakujący może wysłać żądanie do
serwera, takiego jak serwer DNS lub NTP, z fałszywym adresem IP źródłowym.
Kiedy serwer odpowiada, wysyła odpowiedź do fałszywego adresu IP, który jest
rzeczywistym celem ataku. W ten sposób atakujący może zwiększyć ilość ruchu,
jaki generuje, nawet o kilka tysięcy razy.

Na przykład, w ataku na GitHub w 2018 roku, atakujący wykorzystali traffic
amplification, wykorzystując serwery memcached do generowania ruchu o
przepustowości przekraczającej 1,3 Tb/s, co jest największym znanym atakiem
DDoS.

Memcached to system pamięci podręcznej, który przechowuje dane w pamięci
RAM, aby przyspieszyć dostęp do nich. Często jest używany przez strony
internetowe, aby zwiększyć ich wydajność, jednak ma również podatność, która
pozwala na wysyłanie żądań z fałszywym adresem IP i otrzymywanie
odpowiedzi, które są znacznie większe niż żądania.

Atakujący wykorzystali tę cechę, aby przeciążyć GitHub, który jest popularną
platformą do hostowania i współpracy nad kodem.

Jak więc można się bronić przed traffic amplification i innymi technikami,
które zwiększają moc ataku?

Oto kilka wskazówek:

Używaj zabezpieczeń i ograniczeń, aby chronić swoje serwery i usługi przed
nadmiernym ruchem.


---


Używaj narzędzi, które mogą wykrywać i zapobiegać atakom DDoS, takich jak
rate limiting, load balancing, filtering czy scrubbing. Nie pozwól na przesyłanie
żądań lub odpowiedzi, które są zbyt duże lub niepotrzebne.

Używaj aktualnego i legalnego oprogramowania, aby chronić się przed
malwarem i innymi zagrożeniami

Bądź świadomy ryzyka związanego z traffic amplification i innymi technikami,
które zwiększają moc ataku.

Śledź aktualne wiadomości i raporty na temat traffic amplification i innych
technik, które zwiększają moc ataku.

Znajdź wiarygodne źródła informacji i porad na temat bezpieczeństwa
sieciowego.

Podsumowując, traffic amplification to technika, która polega na wykorzystaniu
odpowiedzi na małe żądania do generowania dużego ruchu. Traffic
amplification może być wykorzystany do przeprowadzania ataków DDoS lub
innych celów. Aby zapobiegać traffic amplification i innym technikom, które
zwiększają moc ataku, należy podjąć odpowiednie środki ostrożności i dbać o
higienę cyfrową. Pamiętaj, że lepiej zapobiegać niż leczyć.



2.2 Typy ataków DDoS i ich różnice
I. Wolumetryczne ataki DDoS

Wolumetryczne ataki DDoS to najczęstszy i najprostszy typ ataku DDoS. Ich
celem jest wykorzystanie całego dostępnego pasma pomiędzy ofiarą a
Internetem, co uniemożliwia obsługę prawdziwych zapytań od użytkowników.

Przykładem takiego ataku jest amplifikacja DNS, która polega na wysyłaniu
zapytań o nazwę DNS do otwartych serwerów DNS z podrobionym adresem IP
ofiary. Serwery DNS odpowiadają na te zapytania, wysyłając dużo większe
pakiety do ofiary, co powoduje jej przeciążenie.

Ataki wolumetryczne mogą być bardzo szkodliwe dla firm i organizacji, które
świadczą usługi online. Nie tylko powodują utratę dostępności i reputacji, ale


---


także mogą generować dodatkowe koszty związane z zużyciem pasma i ochroną
przed atakami.

Niektóre z największych w historii ataków DDoS były wolumetrycznymi, np. atak
na stronę KrebsOnSecurity w 2016 roku, który osiągnął ponad 600 Gbps.

Aby chronić się przed wolumetrycznymi atakami DDoS, nie wystarczy zwiększyć
pasma lub zainstalować firewall. Potrzebne są specjalne rozwiązania, które
potrafią odfiltrować niechciany ruch i zapewnić ciągłość działania usług. Takie
rozwiązania mogą być oferowane przez dostawców usług internetowych,
specjalistyczne firmy lub platformy chmurowe.



II. Protokołowe ataki DDoS

Protokołowe ataki DDoS to jeden z rodzajów ataków DDoS, których celem jest
uniemożliwienie dostępu do usługi internetowej poprzez wykorzystanie słabości
lub nadużycie protokołów z trzeciej i czwartej warstwy modelu OSI.

Przykładami takich protokołów są TCP, UDP i ICMP.

Atakujący wysyła do ofiary duże ilości pingów, czyli zapytań o odpowiedź, które
wymagają potwierdzenia odbioru. W ten sposób, atakujący zajmuje wszystkie
zasoby, którymi dysponuje ofiara, takie jak pamięć, procesor czy pasmo. Ofiara
nie jest w stanie obsłużyć prawidłowych zapytań od innych użytkowników i traci
połączenie z internetem.

Aby chronić się przed protokołowymi atakami DDoS, potrzebne są specjalne
rozwiązania, które potrafią odróżnić prawidłowy ruch od szkodliwego i
blokować ten drugi. Takie rozwiązania również jak w przypadku ataków
wolumetrycznych mogą być oferowane przez dostawców usług internetowych,
firmy specjalizujące się w ochronie przed DDoS lub platformy chmurowe.



III. Ataki DDoS na poziomie aplikacji

Ataki DDoS na poziomie aplikacji są jednym z rodzajów ataków DDoS, które
mają na celu zakłócenie lub uniemożliwienie działania określonych funkcji lub
operacji w obrębie aplikacji internetowej lub mobilnej.


---


Ataki te są często bardziej skuteczne i trudniejsze do wykrycia niż ataki DDoS na
poziomie sieci, ponieważ wymagają mniejszej ilości ruchu i mogą być ukryte
wśród prawidłowych żądań użytkowników. Ataki na poziomie aplikacji mogą
mieć różne formy, takie jak:



      Ataki na formularze logowania:

      polegają na wysyłaniu wielu nieprawidłowych danych logowania do
      formularza logowania na stronie internetowej lub w aplikacji, co może
      spowodować przeciążenie serwera lub zablokowanie dostępu do kont
      prawdziwych użytkowników.



      Ataki na interfejsy API:

      polegają na wysyłaniu wielu zapytań do interfejsu API, który jest używany
      do komunikacji między aplikacjami lub usługami, co może spowodować
      opóźnienia, błędy lub niedostępność usług.



      Ataki na koszyki zakupowe:

      polegają na dodawaniu wielu produktów do koszyka zakupowego na
      stronie internetowej lub w aplikacji e-commerce, co może spowodować
      zwiększenie obciążenia serwera lub zapobiec dokonaniu zakupu przez
      prawdziwych klientów.



      Ataki na wyszukiwarki:

      polegają na wysyłaniu wielu złożonych zapytań do wyszukiwarki na
      stronie internetowej lub w aplikacji, co może spowodować spadek
      wydajności lub niedostępność wyników wyszukiwania.



Ataki DDoS na poziomie aplikacji mogą mieć poważne konsekwencje dla firm,
które są zależne od swojej obecności online. Nie tylko mogą one spowodować


---


utratę przychodów, reputacji i zaufania klientów, ale także narazić firmę na
ryzyko naruszenia danych, szantażu lub wymuszenia okupu.
Ważne jest, aby podjąć odpowiednie środki zapobiegawcze i ochronne, takie
jak:

- Monitorowanie ruchu i zachowania użytkowników na stronie internetowej lub
w aplikacji, aby wykrywać i blokować podejrzane lub nieprawidłowe żądania.

- Używanie zabezpieczeń na poziomie aplikacji, takich jak firewall, captcha,
autoryzacja dwuetapowa lub ograniczenie liczby prób logowania, aby zapobiec
nieautoryzowanemu dostępowi lub nadużyciom.

- Korzystanie z usług ochrony przed atakami DDoS, takich jak Cloudflare, Akamai
lub AWS Shield, które mogą zapewnić dodatkową warstwę ochrony i łagodzenia
ataków DDoS na poziomie sieci i aplikacji.



2.3 Metody przeprowadzania ataków DDoS
Szczegółowy opis różnych metod przeprowadzania ataków DDoS


Atak SYN flood
jest jednym z najczęstszych i najprostszych ataków DDoS na poziomie protokołu
TCP, który należy do czwartej warstwy modelu OSI. Atak ten wykorzystuje
trójfazowy proces nawiązywania połączenia TCP, zwany trzema uściskami dłoni
(three-way handshake). Proces ten wygląda następująco:

   1. Klient wysyła do serwera pakiet z ustawioną flagą SYN, sygnalizując chęć
      nawiązania połączenia.
   2. Serwer odpowiada pakietem z ustawionymi flagami SYN i ACK,
      potwierdzając otrzymanie pakietu SYN i zgadzając się na połączenie.
   3. Klient wysyła do serwera pakiet z ustawioną flagą ACK, kończąc proces
      nawiązywania połączenia.

W ataku SYN flood, atakujący wysyła do serwera duże ilości pakietów SYN,
często ze sfałszowanym adresem IP źródłowym, aby uniknąć wykrycia lub
zwiększyć skuteczność ataku.


---


Serwer, otrzymując te pakiety, próbuje odpowiedzieć pakietami SYN-ACK, ale
nie otrzymuje pakietów ACK od atakującego. W ten sposób, serwer traci zasoby
na utrzymywanie półotwartych połączeń, które nigdy nie zostaną zakończone.
Serwer ma ograniczoną liczbę gniazd (sockets), które może przeznaczyć na
nowe połączenia, więc jeśli atak jest wystarczająco intensywny, może
doprowadzić do wyczerpania tych zasobów i uniemożliwienia nawiązania
połączeń przez prawdziwych użytkowników.
Oto cztery sposoby, jak można się bronić przed atakiem SYN flood:

   ● Użycie specjalnych programów, zwanych firewallami, które sprawdzają,
     czy pakiety SYN, które przychodzą do serwera, są prawidłowe i nie
     pochodzą od atakującego. Jeśli firewall wykryje, że pakiet SYN jest
     podejrzany, na przykład ma zły adres IP, port lub numer sekwencyjny, to
     może go odrzucić i nie przekazywać do serwera.

   ·      Można ustawić, że serwer nie będzie czekać zbyt długo na pakiet ACK
   od klienta, który wysłał pakiet SYN. Jeśli pakiet ACK nie przyjdzie w
   określonym czasie, to serwer uzna, że połączenie jest nieprawidłowe i zwolni
   gniazdo, które było na nie przeznaczone. W ten sposób, serwer nie będzie
   tracił zasobów na półotwarte połączenia, które nigdy się nie zakończą.

   ● Zwiększenie ilości gniazd, które serwer ma do dyspozycji na
     nawiązywanie nowych połączeń. Gniazda to miejsca w pamięci serwera,
     które są używane do przechowywania informacji o połączeniach. Im
     więcej gniazd ma serwer, tym więcej połączeń może obsłużyć
     jednocześnie. W ten sposób, serwer może lepiej radzić sobie z dużym
     ruchem i nie odrzucać prawdziwych użytkowników.
   ● Można używać specjalnej techniki, zwanej SYN cookies, która polega na
     tym, że serwer nie przechowuje informacji o półotwartych połączeniach
     w pamięci, tylko w numerze sekwencyjnym, który wysyła do klienta w
     pakiecie SYN-ACK. Numer sekwencyjny jest obliczany tak, że zawiera
     informacje o połączeniu, takie jak adres IP, port, numer sekwencyjny i
     flagi. Kiedy serwer otrzyma pakiet ACK od klienta, to sprawdza, czy
     numer sekwencyjny jest poprawny i czy pasuje do informacji o
     połączeniu. Jeśli tak, to serwer kończy proces nawiązywania połączenia.
     W ten sposób, serwer nie musi trzymać informacji o półotwartych


---


      połączeniach w pamięci, tylko w numerze sekwencyjnym, co oszczędza
      zasoby.




Atak UDP Flood
jest jednym z rodzajów ataków DDoS, które mają na celu uniemożliwienie lub
utrudnienie dostępu do usługi internetowej poprzez zalewanie jej dużą ilością
pakietów UDP.
UDP jest protokołem komunikacyjnym, który nie wymaga nawiązywania
połączenia ani potwierdzania odbioru danych. Dzięki temu jest szybki i prosty,
ale również podatny na nadużycia. Atakujący może wysyłać pakiety UDP na
losowe porty zdalnego hosta, często ze sfałszowanym adresem IP, aby uniknąć
wykrycia lub zwiększyć skuteczność ataku.
Zdalny host, otrzymując te pakiety, musi sprawdzić, czy na danym porcie jest
jakaś aplikacja, która oczekuje na dane. Jeśli nie, to host musi wysłać pakiet
ICMP z informacją, że port jest zamknięty. Jeśli tak, to host musi przekazać
pakiet UDP do aplikacji, która może go zignorować lub próbować odpowiedzieć.
W obu przypadkach, host traci zasoby na przetwarzanie i wysyłanie pakietów, co
może spowodować spadek wydajności lub niedostępność usługi.
Atak UDP Flood może być bardzo szkodliwy dla ofiar, ponieważ może
powodować:

   ● Zwiększenie obciążenia procesora i pamięci hosta, co może spowolnić lub
     zatrzymać jego działanie.
   ● Zwiększenie zużycia pasma sieciowego, co może wpłynąć na jakość i
     prędkość transmisji danych.
   ● Zwiększenie zużycia energii elektrycznej, co może podnieść koszty
     operacyjne lub spowodować przegrzanie sprzętu.
   ● Utratę przychodów, reputacji i zaufania klientów, jeśli usługa jest ważna
     lub płatna.

Oto kilka metod, jak można zabezpieczyć się przed atakiem UDP Flood:


---


   ● Można zainstalować specjalne oprogramowanie, zwane firewallami, które
     analizują, czy pakiety UDP, które docierają do serwera, są prawidłowe i
     nie pochodzą od atakującego. Jeśli firewall zauważy, że pakiet UDP jest
     nieprawidłowy, na przykład ma niepoprawny adres IP, port lub rozmiar, to
     może go zignorować i nie przekazać do serwera. W ten sposób, firewall
     zapobiega przeciążeniu serwera niepotrzebnymi pakietami i chroni go
     przed atakiem.
   ● Możliwe jest skorzystanie z usług ochrony przed atakami DDoS, takich jak
     Cloudflare, które mogą wykrywać i blokować ataki UDP Flood na
     poziomie sieci. Usługi te działają jako pośrednik między serwerem a
     użytkownikami, filtrując ruch i odrzucając podejrzane pakiety UDP. Usługi
     te mogą również zapewnić dodatkowe funkcje, takie jak optymalizacja,
     szyfrowanie i buforowanie danych, co poprawia wydajność i
     bezpieczeństwo serwera.
   ● Można używać protokołów komunikacyjnych, które wymagają nawiązania
     połączenia lub potwierdzania odbioru danych, takich jak TCP lub HTTP,
     które są trudniejsze do zaatakowania za pomocą ataku UDP Flood.
     Protokoły te zapewniają większą niezawodność i kontrolę nad transmisją
     danych, ponieważ wymagają potwierdzenia odbioru każdego pakietu i
     ponawiania transmisji w przypadku błędów lub utraty danych. Protokoły
     te również umożliwiają stosowanie dodatkowych zabezpieczeń, takich jak
     uwierzytelnianie, autoryzacja i szyfrowanie danych.

Atak HTTP Flood
jest atakiem wolumetrycznym siódmej warstwy modelu OSI, która odpowiada
za warstwę aplikacji.
W tej warstwie działają protokoły komunikacyjne, takie jak HTTP, które
umożliwiają wymianę danych między serwerem a klientem. Atak HTTP Flood
polega na tym, że atakujący wysyła do serwera wiele żądań HTTP, wykorzystując
metody GET lub POST.
Żądania te mogą być prawidłowe lub nie, ale ich celem jest zmuszenie serwera
do wykonania jak najwięcej operacji, takich jak przetwarzanie danych, dostęp
do bazy danych, generowanie odpowiedzi, itp.


---


W ten sposób, atakujący chce wyczerpać zasoby serwera, takie jak procesor,
pamięć, pasmo, itp. i uniemożliwić obsługę innych użytkowników.
Atak HTTP Flood może być bardzo szkodliwy dla ofiar, ponieważ może
powodować:

   ● Spadek wydajności lub niedostępność serwera lub aplikacji internetowej,
     co może prowadzić do utraty przychodów, reputacji i zaufania klientów.
   ● Naruszenie bezpieczeństwa lub prywatności danych, jeśli atakujący
     wykorzysta luki lub błędy w serwerze lub aplikacji, aby uzyskać dostęp do
     nich lub je zmodyfikować.
   ● Zwiększenie kosztów operacyjnych lub prawnych, jeśli ofiara musi ponieść
     dodatkowe wydatki na naprawę uszkodzeń, zwiększenie zabezpieczeń,
     odszkodowania, itp.

Aby zapobiec lub złagodzić atak HTTP Flood, można zastosować następujące
środki:

   ● Używać rozproszonej sieci serwerów, takiej jak Cloudflare, która może
     rozłożyć obciążenie na wiele maszyn i zapewnić ciągłość działania usługi.
   ● Używać firewalli, które mogą filtrować lub odrzucać podejrzane żądania
     HTTP, na przykład te, które mają niepoprawny adres IP, nagłówek,
     ciasteczko, itp.
   ● Używać zabezpieczeń na poziomie aplikacji, takich jak captcha,
     autoryzacja dwuetapowa, ograniczenie liczby żądań, itp. aby zapobiec
     nieautoryzowanemu dostępowi lub nadużyciom.
   ● Monitorować logi dostępu i statystyki ruchu, aby wykrywać i analizować
     podejrzane zachowania i reagować na nie.



2.4 Wpływ ataków DDoS na infrastrukturę
Ataki DDoS, czyli rozproszonej odmowy usługi, polegają na zalewaniu serwera
lub infrastruktury sieciowej ogromną ilością ruchu, co prowadzi do
spowolnienia lub zablokowania działania usług internetowych. Ataki te mogą
mieć różne cele i motywacje, takie jak szantaż, sabotaż, protest, konkurencja,
zemsta lub zabawa.


---


Niezależnie od tego, ataki DDoS stanowią poważne zagrożenie dla
bezpieczeństwa i ciągłości działania organizacji, które oferują lub korzystają z
usług internetowych.
Wpływ ataków DDoS na infrastrukturę zależy od wielu czynników, takich jak
rodzaj, skala i czas trwania ataku, rodzaj i konfiguracja infrastruktury, rodzaj i
znaczenie usług oraz zdolność do reagowania i obrony. W zależności od tych
czynników, ataki DDoS mogą spowodować różnorodne skutki, takie jak:

      Utrata dostępności usług:

      Ataki DDoS mogą uniemożliwić lub utrudnić dostęp do usług
      internetowych, zarówno dla użytkowników wewnętrznych, jak i
      zewnętrznych. Może to mieć negatywny wpływ na funkcjonowanie
      organizacji, jej reputację, zaufanie klientów, satysfakcję użytkowników,
      dochody, koszty, zobowiązania prawne i regulacyjne.

      Przykładowo, atak DDoS na platformę e-commerce może spowodować
      utratę sprzedaży, atak na system bankowy może spowodować utratę
      transakcji, atak na system edukacyjny może spowodować utratę dostępu
      do materiałów i testów, atak na system zdrowotny może spowodować
      utratę dostępu do danych pacjentów i lekarzy.

      Utrata integralności i poufności danych:

      Ataki DDoS mogą również wpływać na atrybuty integralności i poufności
      danych, generując wysokie ryzyko ich utraty, uszkodzenia, kradzieży lub
      manipulacji. Może to mieć poważne konsekwencje dla bezpieczeństwa
      informacji, ochrony danych osobowych, praw własności intelektualnej,
      tajemnicy handlowej i innych wartości.

      Przykładowo, atak DDoS na system telekomunikacyjny może spowodować
      utratę lub przechwycenie rozmów, wiadomości i danych, atak na system
      energetyczny może spowodować utratę lub zmianę parametrów sieci,
      atak na system wojskowy może spowodować utratę lub zmianę danych
      wywiadowczych i operacyjnych.



      Utrata zasobów i wydajności:


---


      Ataki DDoS mogą również zużywać i obciążać zasoby i wydajność
      infrastruktury sieciowej, takie jak pasmo, procesory, pamięć, dyski,
      zasilanie, chłodzenie i inne. Może to prowadzić do degradacji jakości
      usług, zwiększenia kosztów operacyjnych, zużycia energii i emisji CO2, a
      nawet uszkodzenia sprzętu.

      Przykładowo, atak DDoS na system monitoringu ruchu może
      spowodować przeciążenie kamer i czujników, atak na system
      meteorologiczny może spowodować przeciążenie stacji i satelitów, atak
      na system lotniczy może spowodować przeciążenie radarów i wież
      kontroli.

W związku z rosnącym zagrożeniem ataków DDoS, rozwijają się również usługi
ochrony przed DDoS oraz innowacje w dziedzinie infrastruktury sieciowej, które
pomagają w radzeniu sobie z tym problemem.
      Niektóre z nich to:

      Aktywne zarządzanie routingiem:

      Polega na dynamicznej zmianie ścieżek ruchu sieciowego w celu
      uniknięcia lub ograniczenia wpływu ataków DDoS. Może to obejmować
      takie techniki jak: blackholing (odrzucanie ruchu atakującego), BGP flow
      specification (określanie reguł filtrowania ruchu na poziomie protokołu
      BGP), usługi cleaning center (przekierowywanie ruchu do specjalnych
      centrów oczyszczania, które usuwają ruch atakujący i przekazują ruch
      prawidłowy), rozwiązania chmurowe (korzystanie z zasobów i usług
      chmurowych do absorbowania i ochrony przed atakami DDoS) .

      CDN:

      Polega na wykorzystaniu sieci dystrybucji treści (Content Delivery
      Network), która składa się z wielu serwerów rozproszonych geograficznie,
      które przechowują i dostarczają treść internetową. CDN pomaga w
      ochronie przed atakami DDoS, ponieważ rozprasza ruch sieciowy,
      zmniejsza obciążenie serwera głównego, zwiększa dostępność i szybkość
      usług, a także zapewnia dodatkowe funkcje bezpieczeństwa, takie jak
      filtrowanie, autoryzacja i szyfrowanie .

      Nadmiarowe pasmo:


---


      Polega na zapewnieniu wystarczającej ilości pasma łącza internetowego,
      aby móc obsłużyć duże ilości ruchu, w tym ruch atakujący. Nadmiarowe
      pasmo pomaga w ochronie przed atakami DDoS, ponieważ zapobiega
      przeciążeniu i utracie dostępności usług, a także umożliwia łatwiejsze
      wykrywanie i analizę ruchu atakującego .




      Rozwiązania inline:

      Polegają na instalowaniu specjalnych urządzeń lub oprogramowania w
      infrastrukturze sieciowej, które są w stanie wykrywać i blokować ruch
      atakujący na poziomie warstwy łącza danych, sieci, transportu lub
      aplikacji. Rozwiązania inline pomagają w ochronie przed atakami DDoS,
      ponieważ zapewniają szybką i skuteczną obronę, a także umożliwiają
      monitorowanie i raportowanie ruchu sieciowego .

      Load balancing i proxowanie:

      Polegają na rozdzielaniu i równoważeniu ruchu sieciowego pomiędzy
      wiele serwerów lub proxy, które obsługują usługi internetowe. Load
      balancing i proxowanie pomagają w ochronie przed atakami DDoS,
      ponieważ zwiększają skalowalność i niezawodność usług, a także
      ukrywają prawdziwy adres IP serwera głównego, co utrudnia atakowanie
      go .



2.5 Przykłady i studia przypadków
Przedstawienie kilku znanych przypadków ataków DDoS


Atak DDoS na Sony PlayStation Network w 2014 roku

W grudniu 2014 roku PSN padło ofiarą zmasowanego ataku DDoS
przeprowadzonego przez grupę hakerską znana jako Lizard Squad. Ta
incydentalna akcja miała daleko idące skutki zarówno dla samego PSN, jak i dla
firmy Sony jako całości.


---


Atak, który był na tyle poważny, że wymagał interwencji FBI i Departamentu
Bezpieczeństwa Krajowego USA, spowodował masowe zakłócenia w dostępie
do usług sieciowych Sony, w tym do gier online, zakupów w sklepie PlayStation
Store oraz innych funkcji oferowanych przez PSN.

W efekcie użytkownicy PSN doświadczyli znacznych trudności w korzystaniu z
platformy, co wywołało frustrację i niezadowolenie wśród milionów graczy na
całym świecie.

Skutki ataku były odczuwalne nie tylko w sferze użytkowania serwisu, ale
również miały istotne konsekwencje finansowe dla firmy Sony.

Szacuje się, że straty spowodowane przez atak DDoS wyniosły około 15
milionów dolarów w utraconych przychodach. Ponadto, aby zrekompensować
użytkownikom za doznane niedogodności oraz zbudować ponownie zaufanie do
platformy, Sony musiało zaoferować swoim klientom różnego rodzaju
rekompensaty, takie jak bezpłatne gry, przedłużenie subskrypcji oraz zniżki na
zakupy w sklepie PlayStation Store. Te dodatkowe koszty oraz straty finansowe
tylko pogłębiły negatywne skutki ataku DDoS dla Sony.

Jednakże, skutki ataku DDoS na PSN nie ograniczyły się jedynie do sfer
finansowych i technicznych. Atak ten miał także poważne konsekwencje dla
sprawiedliwości i egzekwowania prawa.

Działania podejmowane przez organy ścigania, takie jak aresztowania
podejrzanych oraz postępowania sądowe, odzwierciedlają powagę tego rodzaju
cyberprzestępczości. Na przykład, Julius Kivimaki, jeden z podejrzanych za atak
na PSN, został skazany przez sąd fiński na dwuletni nadzór kuratorski oraz
nakazano mu zapłacenie odszkodowania w wysokości 6,9 tys. euro. Podobnie, w
Stanach Zjednoczonych, osoby podejrzane o przeprowadzenie ataku DDoS na
PSN również poniosły konsekwencje prawne, w tym skazanie na więzienie oraz
nakaz zapłaty wysokich odszkodowań.

W związku z atakiem na PSN, Sony było zmuszone także do podjęcia działań w
celu poprawy swojej infrastruktury oraz zabezpieczeń, aby zapobiec podobnym
incydentom w przyszłości. Inwestycje w bezpieczeństwo cybernetyczne stały się
priorytetem dla firmy, która musiała przystosować się do zmieniającego się
krajobrazu zagrożeń w cyberprzestrzeni.


---


Atak DDoS na PlayStation Network miał szeroko zakrojone skutki, obejmujące
sferę techniczną, finansową, a także prawno-organizacyjną. Wpłynął nie tylko na
użytkowników PSN, ale także na firmę Sony jako całość, wymuszając zmiany w
strategii bezpieczeństwa oraz podkreślając konieczność lepszego egzekwowania
prawa w dziedzinie cyberprzestępczości. Atak ten stanowił ostrzeżenie dla firm
działających w obszarze usług online o konieczności podjęcia odpowiednich
środków zaradczych wobec rosnącego zagrożenia atakami cybernetycznymi.



Atak DDoS na Dyn w 2016 roku
Dyn jest dostawcą usług DNS, które odpowiadają za tłumaczenie nazw domen
internetowych na adresy IP.
21 października 2016 roku Dyn był celem trzech kolejnych ataków DDoS, które
spowodowały niedostępność wielu popularnych platform i usług internetowych
w Europie i Ameryce Północnej, takich jak Twitter, Netflix, Reddit, CNN i wiele
innych.
Ataki DDoS polegały na wykorzystaniu botnetu Mirai, który składał się z wielu
urządzeń podłączonych do internetu, takich jak kamery IP, rejestratory DVR i
monitory dla dzieci, zainfekowanych złośliwym oprogramowaniem. Botnet
wysyłał ogromną liczbę zapytań do serwerów Dyn, przeciążając ich
infrastrukturę i uniemożliwiając obsługę prawidłowych żądań.
Ataki wykorzystywały również technikę amplifikacji, polegającą na nadużyciu
usługi memcached, która jest systemem pamięci rozproszonej używanym do
zwiększania wydajności aplikacji internetowych. Usługa ta była nieumyślnie
dostępna w internecie z włączonym protokołem UDP, który umożliwia
fałszowanie adresów IP.
W ten sposób atakujący mogli kierować odpowiedzi z serwerów memcached do
adresów IP należących do Dyn, wysyłając więcej danych niż potrzebne.
Współczynnik amplifikacji wynosił do 51 000, co oznacza, że za każdy bajt
wysłany przez atakującego, do Dyn trafiało do 51 KB danych. Szacuje się, że
szczytowy ruch osiągnął 1,35 Tbps, co czyni go największym znanym atakiem
DDoS w historii.
Dyn zareagował na ataki, angażując dodatkowe zasoby i partnerów, takich jak
Akamai, Cloudflare i Google, aby pomóc w blokowaniu i filtrowaniu


---


niepożądanego ruchu. Ataki trwały około 11 godzin, zanim zostały ostatecznie
powstrzymane.
Atak na Dyn miał poważne konsekwencje dla bezpieczeństwa i stabilności
internetu, pokazując podatność usług DNS na ataki DDoS i zagrożenie, jakie
stanowią niezabezpieczone urządzenia IoT. Atak ten wywołał również debatę na
temat odpowiedzialności i regulacji dostawców usług internetowych,
producentów urządzeń IoT i użytkowników końcowych za zapobieganie i
zwalczanie takich ataków.


Atak DDoS na GitHub w 2018 roku
GitHub jest platformą do hostowania i zarządzania kodem źródłowym, która jest
szeroko używana przez programistów i organizacje na całym świecie. 28 lutego
2018 roku GitHub był ofiarą ataku DDoS, który spowodował niedostępność
serwisu przez około 10 minut.
Atak był podobny do tego, który dotknął Dyn w 2016 roku, ponieważ również
wykorzystywał botnet Mirai i technikę amplifikacji memcached. Jednak atak na
GitHub był jeszcze większy, osiągając szczytowy ruch 1,35 Tbps, co czyni go
największym znanym atakiem DDoS w historii.
GitHub szybko zauważył anomalię w stosunku ruchu przychodzącego do
wychodzącego i podjął decyzję o przeniesieniu ruchu do Akamai, który mógł
zapewnić dodatkową pojemność sieciową na krawędzi. Akamai zastosował
technikę nazywaną “scrubbing”, która polega na usuwaniu i blokowaniu danych
uznanych za złośliwe. Po ośmiu minutach od rozpoczęcia ataku, atakujący
zrezygnowali z ataku i DDoS się zakończył.
Atak na GitHub pokazał, że ataki DDoS wykorzystujące amplifikację memcached
są bardzo skuteczne i trudne do obrony, ponieważ generują ogromny ruch z
niewielkim nakładem zasobów. Atak ten również zwrócił uwagę na problem
nieodpowiedniej konfiguracji usługi memcached, która powinna być
ograniczona do sieci lokalnych, a nie dostępna publicznie z protokołem UDP.
GitHub podzielił się swoim raportem z incydentu i podziękował Akamai za
pomoc w złagodzeniu ataku. GitHub zapowiedział również, że będzie
kontynuował wdrażanie dodatkowej pojemności sieciowej i rozwijanie solidnych
relacji z partnerami, aby zapewnić wysoką dostępność i odporność na ataki
DDoS.


---


Atak DDoS na Spamhaus w 2013 roku
Spamhaus jest organizacją non-profit, która zajmuje się zwalczaniem spamu i
cyberzagrożeń w internecie.
W marcu 2013 roku Spamhaus był celem jednego z największych ataków DDoS
w historii, który osiągnął szczytowy ruch 300 Gbps. Atak został zorganizowany
przez grupę Cyberbunker, która była niezadowolona z tego, że Spamhaus
umieścił ją na czarnej liście jako źródło spamu. Atakujący wykorzystali technikę
amplifikacji DNS, polegającą na wysyłaniu zapytań do podatnych serwerów DNS
z fałszywym adresem IP ofiary. Serwery DNS odpowiadały następnie do
Spamhaus, generując ruch o wielkości 50-100 razy większej niż zapytanie.
Atak był tak silny, że wpłynął na działanie niektórych usług internetowych w
Europie, takich jak Netflix i BBC. Spamhaus również zwrócił się o pomoc do
Cloudflare, firmy specjalizującej się w ochronie przed atakami DDoS.
Cloudflare pomogło w rozproszeniu i filtrowaniu ruchu, a także w
zaangażowaniu innych dostawców usług internetowych i operatorów sieci, aby
zablokować źródła ataku. Po dwóch tygodniach atak został zakończony, a
sprawcy zostali zidentyfikowani i aresztowani.
Atak na Spamhaus pokazał, że ataki DDoS mogą mieć globalny wpływ na
infrastrukturę internetową i wymagają współpracy między różnymi
podmiotami, aby im przeciwdziałać. Atak ten również ujawnił lukę w
zabezpieczeniach protokołu DNS, który powinien być lepiej chroniony przed
nadużyciami.


Atak DDoS na Estonię w 2007 roku
Estonia jest jednym z najbardziej cyfrowo rozwiniętych krajów na świecie, z
ponad 90% usług publicznych dostępnych online.
W kwietniu i maju 2007 roku Estonia była ofiarą serii ataków DDoS, które
sparaliżowały jej kluczowe instytucje i usługi, takie jak rząd, banki, media, szkoły
i transport.
Ataki były związane z konfliktem dyplomatycznym między Estonią a Rosją, który
wybuchł po przeniesieniu pomnika żołnierzy radzieckich z centrum Tallinna na


---


cmentarz wojskowy. Decyzja ta wywołała protesty i zamieszki wśród mniejszości
rosyjskiej w Estonii, a także falę ataków cybernetycznych, które miały na celu
zakłócenie funkcjonowania państwa.
Ataki DDoS polegały na wykorzystaniu botnetów, które wysyłały duże ilości
ruchu do stron internetowych i serwerów celów, uniemożliwiając im obsługę
prawidłowych żądań. Niektóre z ataków były również skoordynowane z atakami
na systemy telefoniczne i e-mailowe. Ataki trwały kilka tygodni, zanim zostały
opanowane przez władze estońskie i ich sojuszników.
Atak na Estonię był pierwszym znanym przypadkiem, gdy atak DDoS był użyty
jako narzędzie wojny hybrydowej, mającej na celu osłabienie i zdestabilizowanie
kraju. Atak ten pokazał również, jak bardzo zależne są nowoczesne
społeczeństwa od internetu i jak ważne jest zapewnienie jego bezpieczeństwa i
odporności na zagrożenia.


   2.6 Zapobieganie i ochrona przed atakami DDoS


Omówienie strategii i narzędzi używanych do zapobiegania atakom DDoS
Ataki DDoS polegają na zalewaniu sieci lub serwera ofiary nadmiernym ruchem,
aby uniemożliwić jej normalne funkcjonowanie i obsługę prawidłowych żądań.
Ataki te mogą powodować znaczne straty finansowe i szkody dla reputacji firmy
lub organizacji. Aby zapobiec lub ograniczyć skutki takich ataków, stosuje się
różne strategie i narzędzia, takie jak:



Zapory sieciowe:

Zapory sieciowe to urządzenia lub programy, które filtrują, analizują i blokują
niepożądany ruch sieciowy na podstawie określonych reguł i polityk. Zapory
sieciowe mogą pomóc w zapobieganiu atakom DDoS poprzez odrzucanie
podejrzanych pakietów, blokowanie adresów IP atakujących lub ograniczanie
liczby połączeń do serwera.

Mogą być stosowane na różnych poziomach sieci, takich jak brama, router,
przełącznik lub serwer. Jednak zapory sieciowe nie są w stanie obronić się przed
wszystkimi rodzajami ataków DDoS, zwłaszcza tych, które wykorzystują techniki


---


amplifikacji lub odbijania, lub tych, które generują duże ilości ruchu, które mogą
przeciążyć zasoby zapory sieciowej.

Istnieją różne typy zapór sieciowych, które mają różne funkcje i zalety. Oto
niektóre z nich:

·    Zapory filtrujące – monitorują przepływające przez nie pakiety sieciowe i
przepuszczają tylko zgodne z regułami zapory. Zapory filtrujące są szybkie i
proste w konfiguracji, ale nie są w stanie analizować zawartości pakietów ani
rozpoznawać ataków na poziomie aplikacji.



·     Zapory pośredniczące (proxy) – wykonujące połączenie w imieniu klienta
lub serwera, zapory pośredniczące mogą sprawdzać i modyfikować treść
pakietów, a także autoryzować i uwierzytelniać użytkowników. Zapory
pośredniczące zapewniają wysoki poziom kontroli i bezpieczeństwa, ale są
wolniejsze i wymagają większej ilości zasobów.



·     Zapory z translacją adresów sieciowych (NAT) – polegają na dokonywaniu
zamiany adresu IP hosta wewnętrznego na inny adres IP widoczny na zewnątrz.
Zapory NAT chronią prywatność i tożsamość hostów wewnętrznych, a także
oszczędzają adresy IP. Zapory NAT mogą być podatne na ataki typu IP spoofing
lub ataki na porty.



·      Zapory osobiste – to programy zainstalowane na komputerach
użytkowników, które chronią je przed nieautoryzowanym dostępem z Internetu
lub z innych sieci. Zapory osobiste mogą być skonfigurowane indywidualnie
przez użytkowników lub przez administratorów sieci. Zapory osobiste mogą być
nieskuteczne, jeśli są wyłączone, zainfekowane lub źle skonfigurowane.



Systemy wykrywania i zapobiegania intruzjom (IDPS):


---


Systemy wykrywania i zapobiegania intruzjom to rozwiązania, które monitorują
sieć pod kątem zagrożeń, a następnie podejmują działania, aby zatrzymać te,
które są wykryte.

Systemy wykrywania intruzji (IDS) są odpowiedzialne za identyfikację i
alarmowanie o podejrzanym ruchu, podczas gdy systemy zapobiegania
intruzjom (IPS) są odpowiedzialne za blokowanie lub ograniczanie tego ruchu.
Systemy te mogą wykorzystywać różne metody do wykrywania ataków DDoS,
takie jak porównywanie sygnatur, analiza anomalii, analiza zachowań lub
uczenie maszynowe. Systemy mogą być wdrożone na różnych poziomach sieci,
takich jak host, sieć lub aplikacja; mogą być skuteczne w zapobieganiu atakom
DDoS na warstwie aplikacji lub protokołu, ale mogą również mieć trudności z
radzeniem sobie z atakami DDoS na warstwie sieci lub objętościowymi, które
mogą wymagać większej pojemności sieciowej.

Systemy IDPS są ważnym elementem cyberbezpieczeństwa, ponieważ pomagają
w ochronie sieci przed różnymi rodzajami ataków, takimi jak:

   ● Ataki na warstwie aplikacji – przykładami takich ataków są SQL injection,
     XSS, CSRF, czy ataki na serwery DNS lub HTTP.
   ● Ataki na warstwie protokołu – przykładami takich ataków są UDP flood,
     ICMP flood, czy amplification attack
   ● Ataki na warstwie objętościowej – przykładami takich ataków są DNS
     amplification, NTP amplification, czy SSDP amplification.



Systemy IDPS mogą być klasyfikowane według różnych kryteriów, takich jak:

   ● Poziom wdrożenia – systemy IDPS mogą być zainstalowane na hostach
     (HIDS, HIPS), na urządzeniach sieciowych (NIDS, NIPS), lub na poziomie
     aplikacji (AIDS, AIPS).
   ● Metoda detekcji – systemy IDPS mogą wykorzystywać różne techniki do
     wykrywania ataków, takie jak porównywanie sygnatur (signature-based),
     analiza anomalii (anomaly-based), analiza zachowań (behavior-based),
     lub uczenie maszynowe (machine learning-based).
   ● Rodzaj reakcji – systemy IDPS mogą mieć różne sposoby reagowania na
     wykryte zagrożenia, takie jak alarmowanie (alerting), blokowanie
     (blocking), ograniczanie (throttling), lub naprawianie (remediation).


---


Usługi ochrony przed DDoS:

Usługi ochrony przed DDoS to rozwiązania zewnętrzne, które zapewniają
ochronę przed atakami DDoS poprzez przeniesienie ruchu do centrów
czyszczenia, gdzie jest on filtrowany i oczyszczany z niechcianych pakietów.

Usługi te mogą być aktywne zawsze lub na żądanie, w zależności od potrzeb
klienta. Usługi często korzystają z różnych technologii, takich jak sieci
rozproszone, sieci anycast, zapory sieciowe, systemy wykrywania i zapobiegania
intruzjom, systemy równoważenia obciążenia lub systemy zarządzania ruchem.

Owe usługi muszą być skuteczne w zapobieganiu atakom DDoS na wszystkich
warstwach i skalach, ponieważ dysponują dużą pojemnością sieciową i
zaawansowanymi mechanizmami obronnymi.

Rozwiązania oferowane przez specjalistyczne firmy lub dostawców usług
internetowych, które mają na celu zabezpieczenie infrastruktury klienta przed
skutkami ataków DDoS działają poprzez przechwytywanie ruchu kierowanego
do klienta i przekierowywanie go do centrów czyszczenia, gdzie jest on
analizowany i filtrowany z niepożądanego lub szkodliwego ruchu.

Do klienta trafia jedynie prawidłowy i bezpieczny ruch, co zapewnia ciągłość i
jakość usług.
Usługi ochrony przed DDoS mogą mieć różne cechy i funkcjonalności, w
zależności od dostawcy i potrzeb klienta. Niektóre z nich to:
   ● Tryb działania – usługi ochrony przed DDoS mogą być aktywne zawsze
     (always-on) lub na żądanie (on-demand). W trybie zawsze aktywnym, cały
     ruch klienta jest stale monitorowany i filtrowany przez usługę, co
     zapewnia szybką i automatyczną reakcję na atak.

      W trybie na żądanie, usługa jest aktywowana tylko wtedy, gdy klient
      zgłosi atak lub gdy zostanie on wykryty przez systemy alarmowe. W tym
      przypadku, klient musi zmienić swoje ustawienia DNS lub BGP, aby
      przekierować ruch do usługi.


---


   ● Poziom ochrony – usługi ochrony przed DDoS mogą zapewniać ochronę
     na różnych warstwach modelu OSI, od warstwy fizycznej do warstwy
     aplikacji. Niektóre usługi mogą skupiać się na zapobieganiu atakom na
     warstwie sieci lub objętościowych, które polegają na generowaniu dużej
     ilości ruchu, aby przeciążyć łącza lub zasoby sieciowe.

      Inne usługi mogą skupiać się na zapobieganiu atakom na warstwie
      aplikacji lub protokołu, które polegają na wykorzystaniu luk w
      oprogramowaniu lub protokołach, aby uzyskać dostęp do danych lub
      zasobów.


   ● Technologie używane – usługi ochrony przed DDoS mogą korzystać z
     różnych technologii, aby zapewnić skuteczne i elastyczne filtrowanie
     ruchu. Niektóre z nich to:



Sieci rozproszone (CDN) – to sieci serwerów rozmieszczonych geograficznie,
które przechowują kopie treści klienta i dostarczają je do użytkowników
końcowych z najbliższego serwera. Sieci CDN mogą pomóc w zapobieganiu
atakom DDoS poprzez rozproszenie ruchu i obciążenia po wielu lokalizacjach, a
także poprzez stosowanie reguł zapory sieciowej i optymalizacji treści.

Sieci anycast – to sieci, w których jeden adres IP jest przypisany do wielu
serwerów lub lokalizacji. Sieci anycast mogą pomóc w zapobieganiu atakom
DDoS poprzez kierowanie ruchu do najbliższego lub najmniej obciążonego
serwera, a także poprzez izolowanie i odrzucanie szkodliwego ruchu.

Zapory sieciowe – to urządzenia lub programy, które filtrują, analizują i blokują
niepożądany ruch sieciowy na podstawie określonych reguł i polityk. Zapory
sieciowe mogą pomóc w zapobieganiu atakom DDoS poprzez odrzucanie
podejrzanych pakietów, blokowanie adresów IP atakujących lub ograniczanie
liczby połączeń do serwera. Zapory sieciowe mogą być stosowane na różnych
poziomach sieci, takich jak brama, router, przełącznik lub serwer.

Systemy wykrywania i zapobiegania intruzjom (IDPS) – to rozwiązania, które
monitorują sieć pod kątem zagrożeń, a następnie podejmują działania, aby
zatrzymać te, które są wykryte. Systemy wykrywania intruzji (IDS) są


---


odpowiedzialne za identyfikację i alarmowanie o podejrzanym ruchu, podczas
gdy systemy zapobiegania intruzjom (IPS) są odpowiedzialne za blokowanie lub
ograniczanie tego ruchu. Systemy te mogą wykorzystywać różne metody do
wykrywania ataków DDoS, takie jak porównywanie sygnatur, analiza anomalii,
analiza zachowań lub uczenie maszynowe.

Systemy równoważenia obciążenia (load balancing) – to rozwiązania, które
rozdzielają ruch i obciążenie po wielu serwerach lub zasobach, aby zapewnić
optymalną wydajność i dostępność. Systemy równoważenia obciążenia mogą
pomóc w zapobieganiu atakom DDoS poprzez zwiększenie pojemności i
odporności sieci, a także poprzez stosowanie reguł zapory sieciowej i
optymalizacji treści.

Systemy zarządzania ruchem (traffic shaping) – to rozwiązania, które kontrolują
i modyfikują ruch sieciowy na podstawie określonych kryteriów, takich jak
priorytet, pasmo, opóźnienie lub jakość usługi. Systemy zarządzania ruchem
mogą pomóc w zapobieganiu atakom DDoS poprzez ograniczanie lub
odrzucanie ruchu, który przekracza ustalone limity lub nie spełnia określonych
warunków.



Praktyczne aspekty związane z ochroną przed tego rodzaju zagrożeniami
Ochrona przed atakami DDoS nie polega tylko na stosowaniu odpowiednich
strategii i narzędzi, ale również na podejmowaniu praktycznych działań, które
mogą zwiększyć odporność i gotowość na takie zagrożenia. Oto niektóre z takich
działań:


Planowanie:
Planowanie to kluczowy element w zapobieganiu i reagowaniu na ataki DDoS.
Obejmuje ono ocenę ryzyka, identyfikację potencjalnych celów i scenariuszy
ataku, wybór odpowiednich rozwiązań i usług ochronnych, ustalenie procedur i
protokołów komunikacyjnych, przygotowanie planu awaryjnego i planu
naprawczego, a także szkolenie personelu i użytkowników.
Planowanie pomaga zminimalizować szanse na wystąpienie ataku, a także
skrócić czas reakcji i ograniczyć straty w przypadku ataku.


---


Monitorowanie:
Monitorowanie to niezbędny element w wykrywaniu i analizowaniu ataków
DDoS. Monitorowanie polega na ciągłym śledzeniu i pomiarze ruchu
sieciowego, wydajności systemów i infrastruktury, zachowania użytkowników i
aplikacji, a także alarmowaniu o wszelkich anomalii i podejrzanym ruchu.
Monitorowanie pomaga w szybkim zidentyfikowaniu i diagnozowaniu ataku, a
także w ocenie jego skali i wpływu na usługi i zasoby. Wymaga ono stosowania
odpowiednich narzędzi i technik, takich jak sondy, snifery, analizatory, systemy
wykrywania i zapobiegania intruzjom, systemy zarządzania zdarzeniami i
incydentami, a także systemy raportowania i wizualizacji.


Aktualizacje:
Aktualizacje to ważny element w utrzymaniu i poprawianiu bezpieczeństwa
systemów i infrastruktury przed atakami DDoS. Aktualizacje polegają na
regularnym instalowaniu i wdrażaniu najnowszych wersji oprogramowania,
systemów operacyjnych, sterowników, firmware, protokołów i innych
komponentów, które mogą zawierać poprawki błędów, łatki bezpieczeństwa,
ulepszenia funkcjonalności i wydajności.
Pomagają w eliminowaniu luk i podatności, które mogą być wykorzystane przez
atakujących, a także w zwiększaniu stabilności i niezawodności systemów i
infrastruktury. Aktualizacje wymagają stosowania odpowiednich procedur i
narzędzi, takich jak systemy zarządzania konfiguracją, systemy zarządzania
aktualizacjami, systemy zarządzania wersjami, a także systemy testowania i
weryfikacji .


Nowoczesne technologie i rozwiązania:
Oprócz tradycyjnych strategii i narzędzi używanych do zapobiegania atakom
DDoS, istnieją również nowoczesne technologie i rozwiązania, które są
skuteczne w zwalczaniu tego rodzaju zagrożeń. Oto przykłady:


Sztuczna inteligencja i uczenie maszynowe


---


Sztuczna inteligencja i uczenie maszynowe to technologie, które pozwalają na
tworzenie i wykorzystywanie systemów, które mogą uczyć się i dostosowywać
się do zmieniających się warunków i sytuacji. Mogą być stosowane do
zapobiegania atakom DDoS poprzez automatyzację i optymalizację procesów
monitorowania, wykrywania, analizy, reakcji i naprawy.
Sztuczna inteligencja i uczenie maszynowe mogą również pomóc w
identyfikowaniu i przewidywaniu nowych i złożonych rodzajów ataków DDoS, a
także w tworzeniu i wdrażaniu skutecznych strategii i narzędzi obronnych.


Blockchain i kryptografia
Blockchain i kryptografia to technologie, które pozwalają na tworzenie i
wykorzystywanie systemów, które są odporne na manipulacje i fałszerstwa.
Blockchain to rozproszona baza danych, która przechowuje informacje w postaci
łańcucha bloków, które są chronione przez kryptografię i konsensus sieciowy.
Kryptografia to nauka o zabezpieczaniu informacji poprzez stosowanie
matematycznych algorytmów i kluczy.
W połączeniu mogą być stosowane do zapobiegania atakom DDoS poprzez
tworzenie i wykorzystywanie systemów, które są niezależne od centralnych
punktów awarii, które są podatne na ataki. Wspólnie są również pomocne w
zapewnieniu integralności, poufności i dostępności informacji i usług, a także w
tworzeniu i wdrażaniu skutecznych mechanizmów uwierzytelniania i
autoryzacji.


Chmura i edge computing
Chmura i edge computing to technologie, które pozwalają na tworzenie i
wykorzystywanie systemów, które są skalowalne i elastyczne. Chmura to model
dostarczania usług i zasobów informatycznych poprzez internet, który
umożliwia dostęp do danych i aplikacji z dowolnego miejsca i urządzenia. Edge
computing to model przetwarzania danych i aplikacji na krawędzi sieci, czyli
blisko źródła danych i użytkowników, co zmniejsza opóźnienia i obciążenie sieci.
Wspolnie mogą być stosowane do zapobiegania atakom DDoS poprzez
tworzenie i wykorzystywanie systemów, które są zdolne do szybkiego
dostosowywania się do zmieniających się potrzeb i wymagań. Chmura i edge
computing są niesamowicie pomocne w rozproszeniu i zrównoważeniu ruchu


---


sieciowego, a także w tworzeniu i wdrażaniu skutecznych rozwiązań i usług
ochronnych.


   2.7 Podsumowanie i wnioski


Podsumowanie
Ataki DDoS są jednym z najpowszechniejszych i najgroźniejszych zagrożeń dla
bezpieczeństwa i dostępności usług internetowych. Polegają na wysyłaniu dużej
liczby zapytań do serwera, aby go przeciążyć i uniemożliwić normalne działanie
strony www lub aplikacji.
Istnieje wiele rodzajów ataków DDoS, które wykorzystują różne protokoły i
techniki, aby zwiększyć skuteczność i uniknąć wykrycia. Ataki DDoS mogą być
prowadzone przez różne podmioty, takie jak cyberprzestępcy, haktywiści,
nieuczciwi konkurenci lub państwa. Ataki DDoS mogą mieć poważne
konsekwencje dla ofiar, takie jak utrata reputacji, dochodów, danych lub
zaufania klientów.
Aby skutecznie przeciwdziałać atakom DDoS, potrzebne są zarówno techniczne,
jak i organizacyjne środki obronne. Niektóre z nich to:

   ● Monitorowanie ruchu sieciowego, aby wykryć i blokować nietypową
     aktywność.
   ● Utworzenie zapory ogniowej, aby ograniczyć przepływ ruchu sieciowego.
   ● Wykorzystanie usług filtrujących, które analizują i odrzucają podejrzane
     zapytania.
   ● Przekierowanie ruchu przez usługi ochrony przed DDoS, które dysponują
     większą przepustowością i zasobami.
   ● Aktualizowanie oprogramowania i sprzętu, aby zapobiegać wykorzystaniu
     luk bezpieczeństwa.
   ● Ustalenie procesów i procedur obsługi incydentów, aby szybko reagować i
     minimalizować szkody.



Wnioski wynikające z analizy ataków DDoS


---


Ataki DDoS są dynamicznym i złożonym problemem, który wymaga ciągłego
dostosowywania się do zmieniających się warunków i zagrożeń. W związku z
tym, należy oczekiwać, że ataki DDoS będą się rozwijać i stawać się coraz
bardziej zaawansowane i intensywne.
Niektóre z możliwych trendów i perspektyw na przyszłość to:

   ● Wykorzystanie sztucznej inteligencji i uczenia maszynowego, aby
     automatyzować i optymalizować ataki DDoS, a także tworzyć kontrataki i
     obronę.
   ● Wykorzystanie Internetu Rzeczy (IoT), aby tworzyć większe i potężniejsze
     botnety, składające się z podłączonych do sieci urządzeń, takich jak
     kamery, routery czy smartfony.
   ● Wykorzystanie technologii 5G, aby zwiększyć szybkość i skalę ataków
     DDoS, a także utrudnić ich wykrycie i śledzenie.
   ● Wykorzystanie kryptowalut i blockchainu, aby finansować i ukrywać ataki
     DDoS, a także tworzyć nowe formy wymuszeń i szantaży.
   ● Wykorzystanie ataków DDoS jako narzędzia wojny cybernetycznej,
     politycznej i gospodarczej, aby destabilizować i zaszkodzić przeciwnikom.

Podsumowując, ataki DDoS są poważnym wyzwaniem dla bezpieczeństwa i
funkcjonowania usług internetowych, które wymagają stałej uwagi i
zapobiegania. Aby skutecznie się bronić, należy stosować zarówno techniczne,
jak i organizacyjne środki, a także śledzić i przewidywać nowe zagrożenia i
możliwości. Ataki DDoS będą prawdopodobnie nadal ewoluować i stawać się
coraz trudniejsze do zwalczenia, dlatego ważne jest, aby być przygotowanym i
czujnym.




   3. Ogólne wprowadzenie (phishing, ransomware, socjotechnika oraz
   bezpieczeństwo aplikacji internetowych).



W obliczu dynamicznego rozwoju technologii oraz coraz bardziej skomplikowanej
struktury systemów informatycznych, bezpieczeństwo systemów i sieci


---


telekomunikacyjnych staje się jednym z najważniejszych wyzwań współczesnej
cyfrowej ery. W miarę postępu technologicznego, rośnie również zakres
zagrożeń, z jakimi muszą zmierzyć się użytkownicy, przedsiębiorstwa i instytucje.
W ramach niniejszego projektu skoncentrujemy się na tematyce przejęcia
kontroli nad systemem ofiary, zgłębiając kwestie związane z phisingiem,
ransomware, socjotechniką oraz bezpieczeństwem aplikacji internetowych.



a) Kontekst problematyki bezpieczeństwa systemów.

Zadaniem współczesnych specjalistów ds. bezpieczeństwa informatycznego jest
nie tylko reakcja na bieżące zagrożenia, lecz także antycypacja potencjalnych
ataków. W miarę jak cyberprzestępcy doskonalą swoje techniki, konieczne jest
ciągłe udoskonalanie systemów obronnych. W ramach tego projektu skupimy się
na zagrożeniach, które wynikają z zaawansowanych ataków, takich jak phising,
ransomware, a także na roli socjotechniki w manipulacji ludzkim czynnikiem w
kontekście bezpieczeństwa.



b) Cel i zakres projektu.

Celem niniejszego projektu jest przeprowadzenie wszechstronnej analizy technik
ataków, których celem jest przejęcie kontroli nad systemem. Skoncentrujemy się
na identyfikacji i zrozumieniu kluczowych zagrożeń związanych z phisingiem,
ransomware,      socjotechniką,   a    także    zagrożeniami    związanymi     z
bezpieczeństwem aplikacji internetowych. Opracujemy praktyczne przykłady
ataków, aby zilustrować różnorodność zagrożeń, z jakimi mierzą się organizacje
oraz jednostki korzystające z systemów informatycznych.


---


Zakres projektu obejmie również analizę środków ochronnych, które mogą być
skutecznie stosowane w celu zminimalizowania ryzyka ataków oraz zwiększenia
ogólnego poziomu bezpieczeństwa systemów. Będziemy bacznie przyglądać się
narzędziom i praktykom, które mogą służyć zarówno prewencji, jak i reakcji na
potencjalne zagrożenia.



c) Struktura projektu.

Projekt zostanie podzielony na sekcje, z których każda będzie skupiała się na
konkretnym aspekcie zagrożeń oraz środków ochronnych. Każda sekcja zawierać
będzie zarówno teoretyczne podstawy, jak i praktyczne przykłady, aby umożliwić
czytelnikowi pełne zrozumienie analizowanych problemów.

W miarę rozwoju projektu, skoncentrujemy się również na zastosowaniu
kryptografii w kontekście bezpieczeństwa, ze szczególnym uwzględnieniem roli
kryptografii w zapewnianiu bezpiecznej wymiany informacji.

d) Wyzwania bezpieczeństwa współczesnego świata cyfrowego

Bezpieczeństwo systemów informatycznych nie jest jedynie kwestią techniczną,
ale również społeczną i organizacyjną. W związku z tym, projekt skupi się na
analizie zarówno aspektów technicznych, jak i społecznych związanych z
zagrożeniami dla systemów i sieci telekomunikacyjnych. Analiza inżynierii
społecznej oraz wpływu socjotechniki na bezpieczeństwo pracowników ma na
celu podkreślenie kompleksowości wyzwań, jakie stawia przed nami współczesne
środowisko cybernetyczne.



2. Zagrożenia phishingowe


---


a) Czym tak właściwie jest phishing?

Phishing to forma ataku, w której cyberprzestępcy próbują uzyskać poufne
informacje, takie jak hasła czy dane finansowe, poprzez podszywanie się pod
zaufane instytucje lub osoby. Ataki phishingowe wykorzystują psychologiczne
triki i zmyłki, by skłonić użytkowników do ujawnienia swoich poufnych danych.
Zrozumienie podstaw definicji phishingu jest kluczowe dla skutecznej
identyfikacji i obrony przed tym typem zagrożenia.



b) Analiza technik phishingowych.

   • E-mail phishing:
E-mail phishing to jedna z najczęściej stosowanych technik. Przestępcy wysyłają
wiadomości e-mail udające oficjalne komunikaty od banków, instytucji czy
serwisów społecznościowych, zachęcając użytkowników do kliknięcia w
zainfekowane linki lub udostępnienia poufnych danych. Przyjrzymy się różnym
przypadkom ataków, jak również analizie struktur fałszywych e-maili.




c) Fałszywe komunikaty na przykład od banków, portali, instytucji itd.

   •   Skradanie Tożsamości: Atakujący starają się naśladować oficjalne
       komunikaty bankowe, wykorzystując logo, nazwę i styl komunikatów
       używanych przez bank. Często stosują techniki inżynierii społecznej,
       tworząc e-maile sugerujące pilną potrzebę potwierdzenia danych, co
       zmusza ofiary do podjęcia natychmiastowych działań.


---


Praktyczny przypadek ataku na Klientów mBanku:

Treść fałszywego e-maila:




Wygląd fałszywej strony mBanku, na jaką przekierowywał link zawarty w
wiadomości:




Po podaniu loginu i hasła, atakujący wyłudzają kolejne dane dostępowe:


---


Prawdopodobnie te dane miały posłużyć do próby "odzyskania" hasła poprzez
infolinię. Włamywacz gromadzi informacje, które mogą zostać użyte jako pytania
weryfikacyjne przez konsultantów mLinii, aby sprawdzić, czy rozmawiają z
autentycznym klientem potrzebującym pomocy związanej z hasłem.



Skąd atakujący „phisherzy” pozyskali e-maile klientów?

Prawdopodobnie atak został skierowany wyłącznie do rzeczywistych klientów
mBanku, a te adresy wydają się być używane jedynie do rejestracji na oficjalnym
forum mBanku – po analizie tego przypadku powstało kilka hipotez takich jak:

   • Błąd w skrypcie forum mBanku - Atakujący mogli wykorzystać błąd w
      skrypcie forum, który pozwalał na pozyskiwanie adresów e-mail
      użytkowników.
   • Włamanie do serwisu internetowego forum mBanku - Atakujący mogli
      dokonać włamania do forum mBanku, uzyskując dostęp do bazy danych i
      kradnąc adresy e-mail.


---


   • Wcześniejszy atak phishingowy na użytkowników forum - Jeśli atak
      phishingowy był skierowany do ograniczonej grupy użytkowników,
      atakujący mogli pozyskać adresy e-mail wcześniej, np. poprzez manipulację
      podczas wcześniejszego ataku phishingowego.
   • Nieuczciwy pracownik - Adresy e-mail mogły zostać pozyskane poprzez
      przekupienie pracownika, np. firmy obsługującej marketing dla mBanku.



Okazało się, że hipoteza numer 1 jest prawdziwa. Adresy mailowe można było
pozyskać bezpośrednio z profilu użytkownika. Te informacje były ujawnione w
kodzie źródłowym strony HTML, choć zastosowano pewne zabezpieczenia w
postaci atrybutu "hidden".




Atak wyłudzający dane poprzez kliknięcie w link do fałszywej strony banku niesie
ze sobą poważne zagrożenia. Wprowadzenie poufnych informacji na takiej
stronie może prowadzić do kradzieży danych logowania, numerów kart
kredytowych oraz innych poufnych danych finansowych, stawiając ofiarę w
sytuacji ryzyka utraty środków oraz naruszenia prywatności.



Praktyczny przypadek ataku nr 2 poprzez e-mail który wykryłem osobiście:

Jakiś czas temu napotkałem się na niepokojące sytuacje związane z
bezpieczeństwem, które chciałbym przedstawić w ramach projektu. Po
dokonaniu sprzedaży na Allegro, zauważyłem uporczywy spam oraz otrzymałem


---


podejrzany SMS z podziękowaniami za korzystanie z usług InPost, który był
wysłany zaledwie kilka minut (ok 4 minuty) po nadaniu paczki w paczkomacie.




Po dokładnej analizie linku zawartego w SMS-ie za pomocą usługi VirusTotal,
pojawiły się alerty wskazujące na potencjalne niebezpieczeństwo.




Dodatkowo, otrzymałem maila, który jednoznacznie wydaje się być próbą
phishingu. Te wydarzenia skłaniają mnie do zastanowienia się nad możliwością
nowego wycieku danych związanych z Allegro lub InPost. To poważne zagrożenie
dla bezpieczeństwa, a otrzymanie spamu po transakcji, podejrzanego SMS-a oraz


---


oczywistego maila phishingowego może sugerować próby wyłudzenia danych –
niestety nie otrzymałem odpowiedzi po zgłoszeniu incydentu do służb security.




Jak wyglądają inne przykłady fałszywych maili phishingowych? Poniżej kilka
przykładów:


---


E-maile zawierają linki do fałszywych stron internetowych, na których ofiary są
proszone o wprowadzenie swoich danych logowania lub informacji finansowych.
Przykłady fałszywych e-maili od banków często zawierają linki do stron
zatwierdzonych    certyfikatami      SSL,   co   dodaje   im   pozorny   charakter
bezpieczeństwa.



Co zrobić aby nie stać się ofiarą?


---


Aby skutecznie chronić się przed email phishing, należy dokładnie sprawdzać
adresy nadawcy, unikać klikania w podejrzane linki czy załączniki, a dodatkowo
korzystać z oprogramowania antyphishingowego, które może skanować i
identyfikować potencjalne zagrożenia. Ponadto, należy być świadomym i
ostrożnym w przypadku wiadomości wymagających natychmiastowego działania
lub ujawnienia poufnych informacji.



d) Fałszywe komunikaty od instytucji

   •   Pozorowana oficjalność: Przestępcy podszywają się pod instytucje, takie
       jak administracja publiczna, urzędy podatkowe czy firmy ubezpieczeniowe.
       Tworzą wiadomości o ważnym charakterze, sugerujące konieczność
       natychmiastowej reakcji w postaci potwierdzenia danych lub pobrania
       załączników.




   •   Załączniki zawierające złośliwe oprogramowanie: Ataki tego rodzaju
       często zawierają załączniki, które po otwarciu instalują na komputerze


---


      ofiary złośliwe oprogramowanie. Może to być keylogger, trojan czy
      ransomware, mające na celu kradzież danych lub szkodzenie systemowi.




e) Fałszywe komunikaty od serwisów społecznościowych

  •   Manipulacja    emocjonalna:     Przestępcy   wykorzystując   dane      o
      użytkownikach z serwisów społecznościowych, próbują stworzyć
      wiadomości spersonalizowane i wiarygodne. Mogą one sugerować
      naruszenie konta, ostrzegać przed próbami nieautoryzowanego dostępu
      czy informować o nowych zabezpieczeniach.

      Poniżej tzw. Smishing (Phishing przez SMS)


---


Smishing, czyli phishing za pomocą wiadomości SMS, to kolejny rodzaj ataku,
który zyskuje na popularności. Przestępcy wysyłają fałszywe wiadomości
tekstowe, podszywając się w tym konkretnym przypadku pod dziecko proszące
mamę o pomoc.

   •   Linki do fałszywych stron logowania: W treści e-maili zawarte są linki do
       fałszywych stron logowania serwisów społecznościowych. Ofiary, myśląc,
       że reagują na rzekome zagrożenie, podają swoje dane uwierzytelniające,
       co pozwala przestępcy przejąć kontrolę nad kontem.




Ataki phishingowe na platformach społecznościowych stają się coraz bardziej
wyrafinowane. Przestępcy wykorzystują popularne media społecznościowe do
szerzenia złośliwych treści, fałszywych profili i linków prowadzących do
zainfekowanych stron.


---


f) Konsekwencje dla ofiar i instytucji wynikające z ataków phishingowych:

   •   Utrata danych: W wyniku ataków tego typu, ofiary mogą ujawnić swoje
       poufne dane, co prowadzi do utraty kontroli nad swoimi danymi
       osobowymi oraz finansowymi.

   •   Straty finansowe: Jeśli przestępcy uzyskają dostęp do informacji
       finansowych, ofiary mogą być narażone na kradzież środków z ich kont
       bankowych, co prowadzi do realnych strat finansowych.

   •   Uszczerbki na reputacji: Atak na renomowaną firmę może prowadzić do
       poważnych uszczerbków na reputacji. Klienci, dowiedziawszy się o
       incydencie, mogą stracić zaufanie do przedsiębiorstwa, co wpływa
       negatywnie na jego pozycję rynkową.

   •   Wyciek poufnych informacji: Atak może prowadzić do wycieku poufnych
       informacji, takich jak dane osobowe klientów lub dokumenty instytucji, co
       stanowi naruszenie prywatności i bezpieczeństwa.

   •   Zakłócenie działań instytucji: Jeśli atak prowadzi do zainfekowania
       systemów instytucji, może to zakłócić normalne funkcjonowanie
       operacyjne, co ma bezpośredni wpływ na klientów oraz spowodować
       utratę zaufania.

   •   Potencjalne kary prawne: W przypadku wycieku danych, instytucja może
       być narażona na potężne kary prawne, zwłaszcza jeśli naruszenie
       prywatności klientów będzie podlegało przepisom o ochronie danych.



g) Środki Ochronne przed atakami phishingowymi


---


   • Narzędzia Anty-Phishingowe
W ramach analizy narzędzi anty-phishingowych, skupimy się na przeglądzie
programów, które są projektowane do identyfikacji i blokowania ataków
phishingowych.

  1. Microsoft Defender for Office 365: Narzędzie to oferuje zaawansowaną
     ochronę przed phishingiem w środowisku poczty elektronicznej.
     Wykorzystuje sztuczną inteligencję do analizy treści wiadomości,
     identyfikacji podejrzanych załączników oraz blokowania szkodliwych
     linków.




  2. Proofpoint   Email   Protection:   To   kompleksowe narzędzie anty-
     phishingowe, które analizuje treści wiadomości, wykrywa oszukańcze linki,
     chroni przed zaawansowanymi atakami typu BEC (Business Email
     Compromise) oraz zapewnia filtrowanie antyspamowe.




  3. Cisco Email Security: Cisco Email Security to rozwiązanie oparte na
     chmurze, które skutecznie chroni przed atakami phishingowymi.


---


      Wykorzystuje zaawansowane technologie analizy behawioralnej, aby
      identyfikować i blokować podejrzane wiadomości.




   4. Symantec Email Security: Symantec oferuje rozbudowane narzędzie anty-
      phishingowe, które skanuje wiadomości w czasie rzeczywistym,
      wykorzystując zaawansowane algorytmy do rozpoznawania zagrożeń oraz
      analizy zachowań.




   • Szkolenia dla Użytkowników
Szkolenia dla użytkowników są kluczowym elementem ochrony przed
phishingiem.

Poniżej przykłady interaktywnych szkoleń online, takich jak:

   1. KnowBe4: to platforma oferująca interaktywne szkolenia online z zakresu
      świadomości      phishingowej.    Zapewnia      różnorodne   scenariusze
      szkoleniowe, testy praktyczne oraz raporty z postępów uczestników.


---


2. PhishER:    dostępny    w    ramach      platformy   KnowBe4,     umożliwia
  przeprowadzanie symulacji ataków phishingowych na pracownikach.
  Pomaga w identyfikacji osób, które wymagają dodatkowego szkolenia i
  wsparcia.




3. Cofense PhishMe: narzędzie oferuje interaktywne szkolenia online,
  symulacje phishingowe oraz analizę wyników, co pozwala organizacjom na
  skuteczne podnoszenie poziomu świadomości pracowników na temat
  zagrożeń phishingowych.




4. Sophos     Phish   Threat:   platforma     szkoleniowa,   która   umożliwia
  organizacjom tworzenie spersonalizowanych kampanii szkoleniowych.
  Oferuje symulacje ataków phishingowych, a także raporty i analizy
  wyników szkoleń.


---


h) Wykresy przykładów ataków phishingowych

Najpowszechniejsze rodzaje oszustw:




Najpopularniejsze strony na których przeprowadzane były ataki phishingowe i jak
zmieniała się ich ilość w przeciągu roku (2020/2021):




   • Infografiki Szkoleniowe
Oto przykłady infografik szkoleniowych dotyczących zagrożeń phishingowych,
które mogą być skutecznym narzędziem edukacyjnym dla pracowników,
zwiększając ich świadomość i umiejętność rozpoznawania potencjalnych
zagrożeń:


---


3.3 Ransomware - Analiza, zabezpieczenia i strategie ochronne

Charakterystyka Oprogramowania ransomware

Czym tak właściwie jest ransomware:


---


Ransomware to złośliwe oprogramowanie, które infekuje systemy komputerowe,
szyfruje dane użytkownika, a następnie żąda okupu w zamian za ich
odblokowanie. Ten rodzaj ataku stanowi poważne zagrożenie dla prywatności,
firm oraz instytucji.




a) Typy i funkcje ransomware:

Ransomware obejmuje różne typy, takie jak crypto-ransomware, który szyfruje
pliki, oraz locker ransomware, który blokuje dostęp do systemu. Funkcje
obejmują także ataki na inne systemy, jak chmury czy urządzenia mobilne.



b) Analiza znanych ataków ransomware:

Przeanalizujemy kilka znanych ataków ransomware, takich jak WannaCry,
NotPetya czy Ryuk.

    • Atak WannaCry:
WannaCry, znany również jako WanaCrypt0r 2.0, WCry czy WannaCry, to złośliwe
oprogramowanie ransomware, które zaatakowało sieci korzystające z protokołu
SMBv1, umożliwiającego komunikację między komputerami a drukarkami oraz
innymi urządzeniami w sieci. Wersja, która pojawiła się w 2017 roku,
wykorzystała lukę w zabezpieczeniach oznaczoną jako MS17-010. Microsoft
wydał poprawkę zabezpieczeń w marcu 2017 roku, ale użytkownicy, którzy jej nie
zainstalowali, stali się łatwym celem dla hakerów stojących za robakiem
WannaCry.


---


Podczas ogromnej epidemii ransomware w maju 2017 roku, WannaCry
najczęściej atakował kraje takie jak Rosja, Chiny, Ukraina, Tajwan, Indie i Brazylia.
Cele ataku obejmowały zarówno użytkowników indywidualnych, jak i instytucje
rządowe, szpitale, uczelnie, firmy kolejowe, przedsiębiorstwa techniczne oraz
dostawców usług telekomunikacyjnych w ponad 150 krajach. Wśród ofiar
znalazły się m.in. publiczny brytyjski system służby zdrowia NHS, Deutsche Bahn,
hiszpańska firma Telefónica, FedEx, Hitachi i Renault.




Eksperci zauważyli, że WannaCry korzysta z dwóch metod ataku znalezionych w
kodzie, który wyciekł z agencji NSA (ETERNALBLUE i DOUBLEPULSAR). Istnieją
także dowody sugerujące związki z północnokoreańską grupą Lazarus.

W przypadku infekcji WannaCry, pliki na zainfekowanym komputerze są
szyfrowane, a użytkownik otrzymuje komunikat z żądaniem okupu w walucie
bitcoin, początkowo równowartości 300 USD, a po upływie 3 dni kwota ta zostaje
podwojona.

Rozpoznanie WannaCry przed atakiem jest trudne, ponieważ infekcja nie
wymaga interakcji użytkownika. Oprogramowanie antywirusowe może pomóc w
usuwaniu WannaCry, ale odszyfrowanie plików jest zazwyczaj niemożliwe.
Ochrona przed WannaCry obejmuje regularne aktualizacje oprogramowania,
korzystanie z oprogramowania antywirusowego, oraz konfigurację zapory


---


sieciowej. Wskazane jest również regularne tworzenie kopii zapasowych danych,
które mogą pomóc w przywracaniu systemu po ataku.




                     Całość procesu działania WannaCry:




   • Atak NotPetya


---


NotPetya, zaatakował w czerwcu 2017 roku, pierwotnie uderzył w Ukrainę, ale
szybko rozprzestrzenił się globalnie, zyskując rozgłos jako oprogramowanie
ransomware. Chociaż na początku wydawało się, że celem jest żądanie okupu,
późniejsze analizy ujawniły, że głównym celem było zaszkodzenie i zakłócenie
działalności firm i instytucji. NotPetya używał zaawansowanych narzędzi,
sugerujących, że mógł być elementem kampanii cyberwojennej.




Atak ten skoncentrował się na sektorach logistycznym, finansowym i
energetycznym, powodując zakłócenia w funkcjonowaniu wielu firm. Oprócz
zaszyfrowania danych, oprogramowanie to niszczyło sektory startowe
komputerów, co znacznie utrudniało przywracanie systemów.

NotPetya wykorzystał dwie główne metody rozprzestrzeniania się. Po pierwsze,
wewnątrz danej sieci, korzystając z narzędzi sieciowych Windows, a po drugie,
globalnie, poprzez rozsyłanie zainfekowanych maili za pomocą techniki
phishingu. Początkowym źródłem ataku było narzędzie M.E.Doc, popularne
wśród ukraińskich instytucji, które zostało skompromitowane. Atakujący zdobyli
dostęp do serwerów M.E.Doc i wprowadzili zainfekowaną aktualizację, która
została automatycznie zainstalowana na wielu komputerach.

W przeciwieństwie do niektórych innych zagrożeń, NotPetya nie szyfrował
natychmiast danych na zainfekowanym komputerze. Zamiast tego szukał


---


sposobów na zainfekowanie innych urządzeń w sieci. To sprawiało, że nawet
domowe wersje Windowsa były pod pewnym względem bezpieczne, ale
korporacyjne wersje, zwłaszcza te podpięte pod domenę Active Directory, były
bardziej narażone.

Aby   się    chronić   przed   NotPetya,   zaleca   się   regularne    aktualizacje
oprogramowania, szczególnie systemu operacyjnego. Ponadto, warto stosować
oprogramowanie antywirusowe oraz utrzymywać kopie zapasowe danych, aby
ułatwić     przywracanie   systemu   po    ewentualnym     ataku.     Dla   bardziej
zaawansowanych użytkowników, istnieje możliwość utworzenia pliku "perfc" w
folderze C:\Windows, ustawionego jako "tylko do odczytu", co może dodatkowo
ograniczyć ryzyko zainfekowania. Jednakże, zawsze istnieje ryzyko, że atakujący
dostosują się do tego rodzaju zabezpieczeń.



   • Atak Ryuk
Ryuk, uważany za zaawansowaną odmianę ransomware, zadebiutował w 2018
roku, cechując się precyzyjnymi atakami skierowanymi głównie przeciwko
korporacjom i instytucjom. Operując w tandemie z innymi złośliwymi
oprogramowaniami, takimi jak Emotet czy TrickBot, Ryuk zdobywa dostęp do
systemów, a następnie przeprowadza zorganizowane i ukierunkowane ataki. W
przeciwieństwie do niektórych programów ransomware, Ryuk nie tylko żąda
okupu, ale również dąży do zaszkodzenia i zakłócenia działalności firm.

Grupa hakerska przypisująca się nazwie WIZARD SPIDER stoi za atakami, a ich
portfolio obejmuje włamania do systemów rządowych, akademickich, służby
zdrowia, fabryk i organizacji technologicznych. Operatorzy Ryuka są znani z żądań
okupu sięgających nawet 12,5 miliona USD, a do końca 2020 roku
prawdopodobnie zgromadzili sumę wynoszącą 150 milionów USD.


---


Atak Ryuka, który w 2019 roku wstrząsnął światem cyberbezpieczeństwa,
zazwyczaj zaczyna się od infekcji innymi malware'ami, takimi jak TrickBot. W
chwili ataku operatorzy wyłączają 180 usług i 40 procesów, które mogłyby
uniemożliwić Ryukowi wykonanie zadania lub są mu potrzebne do
przeprowadzenia ataku. Następnie Ryuk przystępuje do szyfrowania plików,
używając silnych algorytmów, takich jak AES-256, następnie symetryczne klucze
szyfrowania szyfruje asymetrycznym algorytmem RSA-4096.

AES-256 - oznacza Advanced Encryption Standard z kluczem 256-bitowym. Jest
to jeden z najbardziej zaawansowanych i powszechnie stosowanych algorytmów
szyfrowania symetrycznego na świecie. Jest bardzo silny i trudny do złamania.



RSA-4096 to algorytm kryptograficzny oparty na matematyce liczby pierwsze,
który należy do rodziny algorytmów klucza publicznego. Algorytm ten jest często
wykorzystywany do szyfrowania i podpisywania cyfrowego, a liczba 4096 odnosi


---


się do długości klucza używanego przez ten konkretny algorytm RSA. W
przypadku RSA, klucz publiczny i prywatny składają się z par liczb. Długość klucza
(tak jak 4096-bitowy) określa ilość bitów użytych do wygenerowania tych liczb.
Klucz publiczny jest udostępniany publicznie, podczas gdy klucz prywatny jest
trzymany poufnie. Algorytm RSA działa na zasadzie trudności faktoryzacji dużych
liczb na czynniki pierwsze.




Znamiennym dla ataków Ryuka jest fakt, że hakerzy często pozostawiają losowe
zapiski     w       postaci      plików      typu       RyukReadMe.txt        czy
UNIQUE_ID_DO_NOT_REMOVE.txt, co stanowi rodzaj wizytówki ich działań.




Ryuk może pomagać w infekowaniu systemów przez oferowanie usługi
pobierania danych (DaaS). DaaS to usługa oferowana przez jednego hakera


---


innemu. Kiedy haker stworzy ransomware, ale nie wie, jak go rozdystrybuować,
inni hakerzy, posiadający odpowiednie umiejętności, mogą mu w tym pomóc.

Nieuważni użytkownicy często padają ofiarą ataków phishingowych, które
wykorzystują wstępną infekcję. AdvIntel donosi, że aż 91% ataków rozpoczyna się
od phishingowej wiadomości e-mail. Dlatego niesłychanie ważne jest
przeszkolenie użytkowników w zakresie rozpoznawania takich wiadomości.
Szkolenie radykalnie obniża ryzyko infekcji.

Ryuk to jeden z najpospolitszych i najlepiej znanych programów typu
ransomware jako usługa (RaaS), jeśli chodzi o zakres infekcji. W modelu RaaS
twórca programu ransomware oferuje go innym hakerom, którzy odpalają mu
ustalony procent z zysków po udanej akcji. RaaS to forma modelu
oprogramowania jako usługi (SaaS).

Kiedy użytkownik kliknie phishingową wiadomość e-mail, Ryuk pobiera
dodatkowe elementy malware (zwane dropperami). Mogą to być Trickbot,
Zloader, BazarBackdoor i wiele innych. Te programy mogą bezpośrednio
zainstalować Ryuka.

Ponadto mogą zainstalować inny rodzaj malware, na przykład Cobalt Strike
Beacon do komunikacji z centrum dowodzenia (C2). Ryuk jest pobierany po
zakończeniu instalacji malware. Ponadto ten wirus wykorzystuje różne exploity,
jak   na   przykład    lukę    w    zabezpieczeniach        serwerów   Windows   o
nazwie ZeroLogon.

Poniżej ścieżka ifekcji Ryukiem (tzw. attack kill chain).


---


Co świadczy o infekcji Ryukiem?

Skutki infekcji ransomware mogą być dramatyczne, dlatego należy za dołożyć
wszelkich starań, aby jej zapobiec. Nie zawsze jest to możliwe, więc specjaliści
powinni nieustannie monitorować system pod kątem wczesnych objawów ataku
i błyskawicznie podejmować działania, aby zapobiec większym stratom.

Ponieważ Ryuk potrafi zainfekować system na wiele sposobów, jego wykrywanie
jest skomplikowane. Jest wiele wskaźników infekcji (IOC) informujących
administratorów sieci i systemów zabezpieczeń, że zaczyna się infekcja Ryukiem.

Często spotykanym wektorem dla Ryuka jest dropper o nazwie BazarLoader.
Dropper, albo DaaS, to malware, który pobiera do systemu inne złośliwe


---


oprogramowanie. Oto niektóre wskaźniki IOC charakterystyczne dla droppera
BazarLoader:

   •   W rejestrze systemu Windows pojawia się zaplanowane zadanie o nazwie
       „StartAd-Ad” z pozycjami automatycznego uruchamiania

   •   Pojawiają się pliki wykonywalne z podwójnym rozszerzeniem, np.
       Report.DOC.exe



Innym często używanym wektorem ataków Ryuka, jest TrickBot. O jego obecności
świadczy pojawienie się pliku wykonywalnego o składającej się z dwunastu
losowych znaków nazwie. Plik utworzony przez TrickBot, np. mnfjdieks.exe,
będzie znajdował się w jednym z następujących folderów:

   •   C:\Windows\

   •   C:\Windows\SysWOW64

   •   C:\Users\[Nazwa użytkownika]\AppData\Roaming



Podstawowym      środkiem    ochrony     przed   Ryukiem     jest   odpowiednie
monitorowanie systemu pod kątem wczesnych sygnałów ataku oraz stosowanie
procedur reagowania na incydenty. Warto także inwestować w szkolenia
pracowników i regularnie aktualizować procedury bezpieczeństwa. Jako element
prewencyjny można również tworzyć kopie zapasowe danych offline, co ułatwia
szybszą reakcję na ataki i minimalizuje straty. Odkrywanie i neutralizacja ataków
Ryuka to zadanie wymagające profesjonalnego podejścia i ścisłej współpracy
zespołów ds. cyberbezpieczeństwa.


---


   • Skutki dla ofiar
Analiza skutków ataków ransomware pokazuje, że ofiary doświadczają znacznych
strat finansowych, utraty danych, a także zakłócenia normalnej działalności.
Firmy i instytucje, które padły ofiarą takich ataków, muszą również borykać się z
utratą zaufania klientów i koniecznością długotrwałego procesu odbudowy
reputacji.

Skutki obejmują także zakłócenia w dostawach usług, szczególnie w przypadku
sektorów krytycznych, takich jak służba zdrowia czy infrastruktura krytyczna.
Często konieczne jest długotrwałe śledzenie i analiza, aby ocenić pełen zakres
szkód oraz przywrócić normalne funkcjonowanie.

Wnioski z tych ataków wpływają na rozwój bardziej zaawansowanych strategii
ochronnych, ponieważ przestępcy stale doskonalą swoje metody, a środowisko
cybernetyczne staje się coraz bardziej wymagające.



c) Zabezpieczanie przed atakami ransomware

   • Strategie prewencyjne: ransomware może być skutecznie zablokowane
       poprzez skoncentrowane działania prewencyjne. Regularne tworzenie
       kopii   zapasowych    danych    jest   kluczowe,   umożliwiając   szybkie
       przywrócenie systemu w przypadku ataku. Aktualizacje systemów oraz
       korzystanie z oprogramowania antywirusowego i firewalla stanowią
       dodatkowe warstwy obrony.
Dobrą praktyką jest wdrożenie planu automatycznego tworzenia codziennych
kopii zapasowych oraz zapewnienie, że wszystkie systemy są regularnie
aktualizowane, może znacznie zmniejszyć ryzyko utraty danych.

   • Szkolenia dla użytkowników: Edukacja użytkowników to kluczowy
       element prewencji. Szkolenia dotyczące rozpoznawania zagrożeń,


---


      bezpiecznego korzystania z e-maili i unikania podejrzanych linków mogą
      zmniejszyć ryzyko przypadkowego zainfekowania systemu.
Firmy oraz instytucje powinny organizować regularne szkolenia online, które
obejmują testy na rozpoznawanie potencjalnych zagrożeń w e-mailach, może to
zwiększyć świadomość i umiejętności pracowników.

   • Monitoring i analiza działalności systemu: Systemy monitorujące oraz
      IDS/IPS odgrywają kluczową rolę w wykrywaniu i reagowaniu na
      potencjalne zagrożenia ransomware. Analiza anomalii w systemie
      umożliwia szybką identyfikację nieprawidłowości. Ustawienie alertów
      monitorujących niezwykłe wzorce aktywności na sieci, co pozwala na
      szybką reakcję w przypadku podejrzanego zachowania systemu.
   • Segmentacja      sieci:   Segmentacja    sieci   to   skuteczna   strategia
      zabezpieczająca przed rozprzestrzenianiem się ransomware. Izolacja
      kluczowych obszarów systemu minimalizuje ryzyko, że atak obejmie całą
      infrastrukturę. Stworzenie osobnych segmentów sieci dla kluczowych
      sektorów firmy, takich jak finanse czy zarządzanie danymi, aby ograniczyć
      potencjalne szkody w przypadku ataku.
   • Odzyskiwanie     danych:    Planowane     i   regularne   tworzenie   kopii
      zapasowych danych stanowi podstawę skutecznych strategii odzyskiwania
      danych po ataku ransomware. Dobrą praktyką jest codzienne
      automatyczne tworzenie kopii zapasowych danych w odizolowanym
      środowisku, aby uniknąć ich zainfekowania w przypadku ataku.
   • Przywracanie systemu: Skuteczne przywracanie systemu po ataku
      ransomware wymaga oceny szkód, identyfikacji źródła ataku i eliminacji
      zagrożenia. Zalecane jest wypracowanie procedur przywracania systemu
      z wykorzystaniem zaktualizowanych kopii zapasowych, z uwzględnieniem
      identyfikacji podatności, które zostały wykorzystane przez atakujących.


---


d) Kontynuacja działalności w sytuacji ataku ransomware

   • Plan awaryjny: Plan awaryjny obejmuje procedury działania, identyfikację
      kluczowych zasobów, komunikację z interesariuszami oraz skuteczne
      przywracanie    funkcjonalności   systemu.    Należy   określić   zespoły
      odpowiedzialne za przywracanie systemu, zarządzanie komunikacją
      wewnętrzną i z interesariuszami oraz regularne przeprowadzanie ćwiczeń
      awaryjnych.
   • Współpraca z instytucjami ochrony: Współpraca z instytucjami
      zajmującymi się cyberbezpieczeństwem oraz organami ścigania jest
      kluczowa w przypadku ataku ransomware. Wspólna analiza i reakcja na
      incydent przyspieszają proces ochrony danych. W razie potrzebu należy
      nawiązać współpracę z lokalnymi agencjami ds. cyberbezpieczeństwa, aby
      uzyskać wsparcie i niezbędne informacje.


Wnioski:
W procesie analizy ransomware, kluczowym wnioskiem jest uświadomienie
sobie, że ataki te są nieuchronne, dlatego należy być zawsze przygotowanym.
Zidentyfikowano, że strategie prewencyjne, takie jak regularne tworzenie kopii
zapasowych, edukacja użytkowników i monitoring systemu, odgrywają kluczową
rolę w ograniczaniu ryzyka.



e) Zalecenia na przyszłość

Aby zwiększyć odporność systemów na ataki ransomware, zaleca się:

   • Ciągłe szkolenia i świadomość: Regularne szkolenia dla pracowników w
      zakresie   najnowszych   zagrożeń    oraz    promowanie     świadomości
      cyberbezpieczeństwa wśród personelu.


---


   • Automatyczne         kopie      zapasowe:   Utrzymywanie     regularnych,
      automatycznych kopii zapasowych danych w odizolowanym środowisku, a
      także regularne testowanie procedur ich przywracania.
   • Monitoring proaktywny: Wdrażanie systemów monitorujących z
      funkcjami analizy anomalii, umożliwiających szybką identyfikację
      nieprawidłowości.
   • Segmentacja sieci: Stosowanie segmentacji sieci w celu izolacji kluczowych
      obszarów systemu i ograniczenia potencjalnych szkód.
   • Plan awaryjny i ćwiczenia: Opracowanie i regularna aktualizacja planu
      awaryjnego, a także przeprowadzanie ćwiczeń symulacyjnych, aby
      zminimalizować czas reakcji.
   • Współpraca zewnętrzna: Nawiązywanie współpracy z instytucjami
      zajmującymi się cyberbezpieczeństwem oraz organami ścigania, aby
      skoordynować reakcję na incydent.
Poprzez skoncentrowanie się na tych aspektach, organizacje mogą wzmocnić
swoją odporność na ataki ransomware, minimalizując potencjalne straty i
skracając czas reakcji w przypadku incydentu.



3.4 Social Engineering

a) Rola socjotechniki w atakach

Socjotechnika odgrywa kluczową rolę w atakach na bezpieczeństwo systemów,
wykorzystując ludzkie zachowania i interakcje. Ataki oparte na socjotechnice
często polegają na manipulacji pracowników, aby uzyskać nieautoryzowany
dostęp do informacji czy systemów. W tym kontekście socjotechnika wpływa na
bezpieczeństwo systemów, ukierunkowując się na słabości ludzkiego elementu,
który stanowi często najłatwiejszy cel dla cyberprzestępców.


---


b) Analiza technik socjotechnicznych

Przegląd różnorodnych technik socjotechnicznych używanych w atakach
obejmuje m.in.:

  • Phishing społecznościowy:
Phishing społecznościowy to technika socjotechniczna, która wykorzystuje
zaufane relacje między ludźmi w celu oszustwa i zdobycia poufnych informacji.
W tej metodzie atakujący udaje się zaufaną osobę lub instytucję, aby zmylić
potencjalne ofiary. Przykłady obejmują fałszywe e-maile, komunikaty
społecznościowe czy strony internetowe, które wyglądają autentycznie, a ich
celem jest wyłudzenie poufnych danych, takich jak hasła czy dane karty
kredytowej. Atakujący często posługują się psychologią społeczną, wykorzystując
techniki manipulacyjne, aby przekonać ofiary do udzielenia swoich poufnych
informacji.


---


  • Inżynieria społeczna przez telefon:
Inżynieria społeczna przez telefon to próby manipulacji i oszustwa
przeprowadzane za pomocą rozmów telefonicznych w celu zdobycia poufnych
danych. Atakujący mogą udawać przedstawicieli instytucji finansowych, firm
technologicznych czy urzędów, aby przekonać ofiary do ujawnienia swoich
danych osobowych, numerów kont bankowych czy kodów PIN. Ta technika
socjotechniczna opiera się na zdolności przekonywania i manipulacji werbalnej,
a atakujący często używają taktyk straszenia lub podszywania się za osoby
autentyczne w celu zwiększenia skuteczności ataku.




  • Ataki bezpośrednie w miejscu pracy:
Ataki Bezpośrednie w miejscu pracy to fizyczne próby uzyskania dostępu do
budynków lub komputerów poprzez podszywanie się za pracowników lub osoby
zaufane. Atakujący mogą próbować przełamać fizyczne zabezpieczenia, takie jak
systemy kontroli dostępu, lub wykorzystać brak świadomości pracowników w
celu swobodnego przemieszczania się po obiekcie. To może obejmować
podszywanie się pod dostawców usług, pracowników sprzątających czy innych
osób, które są w stanie uzyskać fizyczny dostęp do miejsca pracy. Ataki
bezpośrednie w miejscu pracy wymagają precyzyjnego planowania oraz
zdolności do manipulacji ludźmi i sytuacją.


---


c) Psychologiczne aspekty social engineeringu

Analiza   psychologicznych    mechanizmów       wykorzystywanych    w    atakach
socjotechnicznych obejmuje:

  • Zaufanie społeczne:
Zaufanie społeczne to kluczowy element psychologiczny wykorzystywany w
atakach socjotechnicznych. Atakujący starają się budować fałszywe zaufanie,
korzystając z informacji lub relacji między ludźmi. Przykładowo, mogą
wykorzystać publicznie dostępne informacje na temat organizacji lub relacji
społecznych, aby stworzyć wiarygodny kontekst dla swoich działań.
Wykorzystanie elementu zaufania sprawia, że ofiara jest bardziej skłonna udzielić
informacji lub podjąć inne działania, uważając, że interakcja ma legitymację.


---


  • Manipulacja emocjonalna:
Manipulacja emocjonalna to kolejny istotny element w psychologicznych
aspektach social engineeringu. Atakujący wykorzystują emocje, takie jak strach,
ciekawość lub chęć pomocy, w celu uzyskania pożądanej reakcji od ofiary.
Przykładowo, atakujący mogą wywołać strach przed utratą danych,
zainfekowaniem komputera czy innymi negatywnymi konsekwencjami, aby
zmusić ofiarę do podjęcia pośpiesznych działań, takich jak ujawnienie poufnych
informacji. Manipulacja emocjonalna polega na skierowaniu uwagi ofiary na
określony stan emocjonalny, który sprzyja realizacji celów atakującego.




  • Zagrożenia i nagrody:
Tworzenie sytuacji, w której ofiara czuje się zagrożona lub obiecuje nagrodę,
stanowi kolejny psychologiczny mechanizm wykorzystywany w atakach
socjotechnicznych. Atakujący mogą grozić utratą dostępu do konta,
sfałszowanym oskarżeniem lub innymi konsekwencjami, aby zmusić ofiarę do
współpracy. Z drugiej strony, obiecanie nagrody, takiej jak wygrana w konkursie
czy dostęp do ekskluzywnych informacji, może skłonić ofiarę do udzielenia
niebezpiecznych informacji. Ten rodzaj psychologicznej manipulacji opiera się na
działaniu ludzkiego instynktu unikania zagrożeń i dążenia do nagród.


---


3.5 Bezpieczeństwo aplikacji internetowych

a) Zagrożenia Związane z Aplikacjami Internetowymi

Przegląd popularnych ataków na aplikacje internetowe, w tym:

  • SQL Injection:
SQL Injection to powszechne zagrożenie związane z aplikacjami internetowymi,
które polega na wstrzykiwaniu złośliwego kodu SQL w celu manipulacji bazą
danych. Atakujący wykorzystują luki w mechanizmach obsługi danych
wejściowych, takich jak formularze, aby wprowadzić złośliwy kod SQL. Gdy
aplikacja nie sprawdza poprawnie i dostatecznie danych wprowadzanych przez
użytkownika, atakujący może modyfikować zapytania SQL i uzyskiwać dostęp do
poufnych danych, takich jak hasła czy dane użytkowników. SQL Injection może
prowadzić do naruszenia integralności danych oraz dostępu do informacji, które
nie powinny być udostępnione.


---


SQL injection w praktyce:
Aplikacje, które nie są należycie zabezpieczone, narażone są na różnorodne
ataki, w tym na manipulacje formularzami, co może prowadzić do poważnych
zagrożeń bezpieczeństwa. Jednym z powszechnie stosowanych ataków na słabo
zabezpieczone aplikacje jest wykorzystanie wbudowanych formularzy do
wydobywania poufnych danych, takich jak loginy i hasła użytkowników.

Proces tego typu ataku jest stosunkowo prosty. Haker wykorzystuje formularz
logowania, jednak zamiast wprowadzać swoje dane, wpisuje frazy, które w
połączeniu z zapytaniem SQL zawsze zwrócą wynik TRUE. Przykładowo, zamiast
standardowych danych logowania, haker wpisuje frazę:




Wynikowe zapytanie SQL generowane przez aplikację przyjmuje wtedy postać:



W tym przypadku wykorzystuje się fakt, że w języku SQL fraza OR “”=”” zawsze
zwraca wartość TRUE. W efekcie przesłane zapytanie skutkuje wyświetleniem
wszystkich loginów i haseł zapisanych w bazie danych.


---


Warto zauważyć, że odpowiednio zabezpieczona aplikacja nie będzie podatna
na tego rodzaju manipulacje. Niemniej jednak, tego typu metody są skuteczne
w przypadku amatorskich usług, które nie zostały odpowiednio zabezpieczone
przed atakami SQL Injection (SQLi).

W skrajnych przypadkach, szczególnie w sytuacji bardzo słabo zabezpieczonych
formularzy, istnieje nawet możliwość zalogowania się do aplikacji bez
podawania prawidłowego loginu i hasła. Jak to możliwe?

Najprostszy formularz logowania może generować zapytanie SQL do bazy
danych w formie:




Zamiast standardowych danych logowania, manipulując formularzem, można
spowodować, że generowane zapytanie zawsze zwróci wartość TRUE. Na
przykład, zamiast wprowadzać prawdziwe dane logowania, wpisuje się:




W tym przypadku argument „1 = 1” jest zawsze prawdziwy, a znaki specjalne
służą do skonstruowania komentarza w języku SQL, ignorując w ten sposób
hasło. Takie zapytanie zwróci wartość TRUE, umożliwiając nawet
uwierzytelnienie użytkownika.

Innym popularnym przykładem ataku SQL Injection jest użycie polecenia
UNION, które pozwala na scalanie wyników kilku zapytań SELECT. Poprawnie
wykorzystane może skutkować wzbogaceniem głównego zapytania SQL o
dodatkowe informacje. W rezultacie atakujący może uzyskać poufne dane, takie
jak loginy, hasła, numery PESEL czy maile użytkowników. Ochrona przed tego


---


typu atakami wymaga skrupulatnego zabezpieczania formularzy oraz
stosowania środków ochronnych przed atakami SQL Injection.



  • Cross-Site Scripting (XSS):
Cross-Site Scripting (XSS) to atak, w którym atakujący wstrzykuje złośliwy skrypt
w stronę internetową, który jest następnie wykonany przez przeglądarkę ofiary.
Atakujący często wykorzystują luki w mechanizmach obsługi danych wejściowych
lub bezpośrednio w treści strony, aby osadzić złośliwe skrypty. Skrypty te mogą
być używane do kradzieży sesji użytkownika, przechwytywania informacji
przesyłanych między przeglądarką a serwerem, a także przekierowywania
użytkowników na fałszywe strony internetowe. XSS jest                szczególnie
niebezpieczny, ponieważ atakujący może zdalnie kontrolować przeglądarkę
ofiary, co umożliwia różne formy manipulacji i szpiegostwa.


---


Praktyczny przykład:




Zielonej ofierze podsyłany jest tutaj link z przykazaniem parametru do aplikacji.
Parametr search zawiera wstrzyknięcie javascriptu tagiem <script>. Zobaczmy
co dzieje się dalej:




Całość można prześledzić na realnej aplikacji, dostępnej tutaj (czy nie
ostrzegałem przed klikaniem „w ciemno”? ;-)


---


Wyżej widzieliśmy bardzo prosty przykład uruchomienia javascriptu poprzez tag
<script>. W jaki sposób wykonać javascript jedynie poprzez odpowiednie
manipulacje parametrami do tagu? Na przykład tak:

<img src=tralalala onerror=alert(/xss/)>

(Przykład zaczerpnięty od sekurak: https://sekurak.pl/czym-jest-xss/)



  • Cross-Site Request Forgery (CSRF):
Cross-Site Request Forgery (CSRF) to atak, który wykorzystuje zaufanie
użytkownika do wykonania niechcianych działań na stronie, na której użytkownik
jest zalogowany. Atakujący wysyła żądanie HTTP w imieniu ofiary, wykorzystując
sesję uwierzytelniającą użytkownika. Jeśli użytkownik jest zalogowany na danej
stronie, to żądanie może być traktowane jako autentyczne, co pozwala
atakującemu na manipulację ustawieniami, zmianę hasła czy nawet dokonanie
transakcji finansowej. CSRF jest szczególnie niebezpieczny w kontekście aplikacji
internetowych, które nie odpowiednio zabezpieczają przesyłanych żądań i sesji
użytkowników.


---


b) Narzędzia wykorzystywane w atakach na aplikacje internetowe

  • Burp Suite:
Burp Suite to kompleksowe narzędzie do testowania bezpieczeństwa aplikacji
internetowych, które jest powszechnie wykorzystywane przez profesjonalistów
ds. bezpieczeństwa oraz hakerów etycznych. Posiada szereg funkcji,
umożliwiających wykrywanie luk w zabezpieczeniach i przeprowadzanie
różnorodnych ataków. Burp Suite może być używane do przechwytywania,
analizy i modyfikacji ruchu HTTP, a także do automatycznego skanowania aplikacji
w poszukiwaniu słabości, takich jak SQL Injection czy Cross-Site Scripting.
Narzędzie to wspomaga także testowanie wydajności aplikacji, co czyni je
wszechstronnym instrumentem w rękach testerów bezpieczeństwa.




  • OWASP ZAP (Zed Attack Proxy):
OWASP ZAP (Zed Attack Proxy) to bezpieczne narzędzie do testowania aplikacji
internetowych, które jest dostępne jako wolne oprogramowanie o otwartym
kodzie źródłowym. Stworzone przez Open Web Application Security Project
(OWASP), ZAP umożliwia identyfikację i naprawę błędów bezpieczeństwa w
aplikacjach internetowych. Narzędzie to oferuje funkcje, takie jak automatyczne


---


skanowanie podatności, przechwytywanie i analiza ruchu HTTP, wstrzykiwanie
złośliwych danych, a także wsparcie dla wielu różnych technologii internetowych.
OWASP ZAP jest rozwijane przez społeczność i jest powszechnie stosowane w
celu weryfikacji bezpieczeństwa aplikacji.




  • Zabezpieczanie aplikacji internetowych
Chociaż "Zabezpieczanie Aplikacji Internetowych" nie jest konkretnym
narzędziem, to jest to kluczowy element w kontekście narzędzi używanych w
obronie przed atakami. Proces ten obejmuje szereg działań mających na celu
minimalizację podatności aplikacji na ataki. Włącza to wdrażanie najlepszych
praktyk programistycznych, takich jak bezpieczne zarządzanie sesją, walidacja
danych wejściowych, stosowanie odpowiednich mechanizmów kontroli dostępu,
a także regularne testowanie bezpieczeństwa. Narzędzia związane z
zabezpieczaniem aplikacji internetowych mogą obejmować frameworki
bezpieczeństwa, takie jak Spring Security czy Django Security, a także praktyki
DevSecOps, integrujące bezpieczeństwo w procesy deweloperskie.


---


c) Praktyczne środki zabezpieczające obejmują:

  • Regularne aktualizacje:
Regularne aktualizacje stanowią kluczowy element praktycznych środków
zabezpieczających. Polegają one na stałym uaktualnianiu oprogramowania,
systemów operacyjnych, bibliotek oraz innych komponentów aplikacyjnych w
celu zamknięcia potencjalnych luk bezpieczeństwa. Producent oprogramowania
regularnie udostępnia poprawki bezpieczeństwa, które eliminują znane
podatności. Brak aktualizacji oprogramowania może prowadzić do wykorzystania
znanego    exploitu   przez   atakujących.   Praktyka   ta   obejmuje   również
monitorowanie informacji o bezpieczeństwie dostarczanych przez dostawców
oprogramowania oraz szybką reakcję na pojawiające się zagrożenia




  • Firewalle aplikacyjne:
Wykorzystanie firewalli aplikacyjnych jest kolejnym skutecznym środkiem
zabezpieczającym. Firewalle te monitorują i kontrolują ruch w sieci aplikacyjnej,
chroniąc przed nieautoryzowanym dostępem i atakami. Firewall aplikacyjny
analizuje warstwę aplikacji protokołu komunikacyjnego, umożliwiając precyzyjną
kontrolę nad ruchem sieciowym. W przeciwieństwie do tradycyjnych firewalli,
które operują na poziomie warstwy sieciowej, firewall aplikacyjny jest w stanie
zrozumieć kontekst aplikacji, co pozwala na bardziej zaawansowaną filtrację


---


ruchu. Skonfigurowane reguły w firewallu aplikacyjnym mogą chronić przed
atakami, takimi jak SQL Injection czy Cross-Site Scripting.




  • Kontrola dostępu:
Kontrola dostępu jest kluczowym środkiem zabezpieczającym, mającym na celu
ograniczenie dostępu do zasobów aplikacji tylko dla upoważnionych
użytkowników. Wdrożenie skutecznej kontroli dostępu obejmuje identyfikację i
uwierzytelnianie    użytkowników,     zarządzanie     ich     uprawnieniami   oraz
monitorowanie ich działań. Mechanizmy takie jak autentykacja dwuskładnikowa,
silniki polityk dostępu (RBAC, ABAC) oraz audyt dostępu pomagają w skutecznej
kontroli dostępu do danych i funkcji aplikacji. Poprawna implementacja kontroli
dostępu jest kluczowa dla uniknięcia sytuacji, w których nieupoważnieni
użytkownicy uzyskują dostęp do poufnych informacji czy funkcji systemu.


---


3.6 Bezpieczna wymiana informacji - rola kryptografii

a) Wprowadzenie do kluczowych koncepcji kryptograficznych obejmuje:

   1. Szyfrowanie symetryczne i asymetryczne:

  • Szyfrowanie stanowi podstawową technikę kryptograficzną, mającą na celu
     zabezpieczenie danych poprzez ich konwersję w taki sposób, aby były one
     nieczytelne dla osób nieuprawnionych. W ramach kryptografii wyróżnia się
     dwa główne rodzaje szyfrowania - symetryczne i asymetryczne.



  • Szyfrowanie Symetryczne: Jest to rodzaj szyfrowania, w którym do zarówno
     szyfrowania, jak i deszyfrowania danych używany jest ten sam klucz. Oba
     procesy wymagają posiadania tego samego tajnego klucza. Szyfrowanie
     symetryczne jest efektywne pod względem wydajności, jednak wymaga
     bezpiecznego udostępnienia klucza między stronom komunikującymi się.



  • Szyfrowanie    Asymetryczne:     W   przeciwnym      razie   nazywane   jest
     szyfrowaniem klucza publicznego i prywatnego. W tym przypadku używane
     są dwa klucze - jeden publiczny do szyfrowania danych i drugi prywatny do
     ich deszyfrowania. Klucz publiczny jest dostępny publicznie, co pozwala na
     bezpieczne przesyłanie danych, podczas gdy klucz prywatny jest trzymany
     w    tajemnicy.   Szyfrowanie    asymetryczne      eliminuje   konieczność
     bezpiecznego udostępniania klucza, ale jest bardziej złożone obliczeniowo.



   2. Klucze Kryptograficzne:

   • Klucze kryptograficzne odgrywają kluczową rolę w procesie szyfrowania i
     deszyfrowania danych. Są to sekwencje bitów, które determinują procesy


---


        kryptograficzne. W kontekście szyfrowania symetrycznego, obie strony
        komunikujące się muszą używać tego samego klucza. Natomiast w
        przypadku szyfrowania asymetrycznego, para kluczy, składająca się z
        klucza publicznego i prywatnego, jest wykorzystywana. Klucz publiczny
        jest dostępny publicznie, a klucz prywatny jest trzymany w tajemnicy.
        Bezpieczeństwo systemu kryptograficznego często zależy od
        bezpiecznego przechowywania i przekazywania kluczy.

b) Zastosowanie kryptografii w bezpiecznej wymianie informacji

Analiza roli kryptografii w zabezpieczaniu danych i komunikacji obejmuje:

      • SSL/TLS w komunikacji sieciowej:
Protokoły SSL (Secure Sockets Layer) i TLS (Transport Layer Security) są
wykorzystywane do zabezpieczania komunikacji internetowej. Zapewniają one
poufność, integralność i uwierzytelnianie danych przesyłanych między klientem
a serwerem. SSL/TLS używają technik szyfrowania, takich jak szyfrowanie
asymetryczne do wymiany kluczy sesji oraz szyfrowanie symetryczne do
szyfrowania rzeczywistej komunikacji.

      • Wprowadzenie do bezpiecznych kanałów komunikacyjnych:
Bezpieczne kanały komunikacyjne są kluczowym elementem w wymianie
poufnych informacji. To zabezpiecza przekazywane dane przed przechwyceniem
lub     modyfikacją   przez   potencjalnych   atakujących.   Bezpieczne     kanały
komunikacyjne opierają się na protokołach kryptograficznych, takich jak SSL/TLS,
aby zapewnić poufność, integralność i autentyczność transmisji danych.

Wnioski płynące z analizy kluczowych zagrożeń i środków ochronnych ukazują, że
skuteczne      zarządzanie    bezpieczeństwem    informatycznym     to      proces
wieloaspektowy. Wrażliwość na ludzki czynnik stała się jednym z głównych
obszarów uwagi, a świadomość pracowników uznawana jest za kluczową w
zapobieganiu atakom. Jednakże, aby kompleksowo zabezpieczyć organizację,


---


niezbędne jest wdrożenie wielowarstwowych środków ochronnych. Ochrona
przed zagrożeniami nie powinna opierać się wyłącznie na jednym rodzaju
zabezpieczeń, lecz raczej na strategicznym połączeniu różnych środków w celu
zminimalizowania ryzyka.

Podkreślenie     kluczowych   aspektów   podsumowuje,   że   bezpieczeństwo
informatyczne nie jest statycznym obszarem, ale wymaga ciągłego doskonalenia
procedur i technologii. Organizacje powinny być gotowe na dynamiczne zmiany
w krajobrazie zagrożeń cybernetycznych i elastycznie dostosowywać swoje
strategie bezpieczeństwa. Współpraca zewnętrzna, zwłaszcza z instytucjami
zajmującymi się cyberbezpieczeństwem, stanowi kluczową część skutecznej
reakcji na zmieniające się zagrożenia. Dzięki współpracy, organizacje mogą
wymieniać informacje, uczestniczyć w analizach sytuacyjnych i skorzystać z
doświadczeń innych podmiotów, co wzmocni ich zdolność do skutecznej obrony
przed atakami.



Podsumowując, kompleksowe podejście do bezpieczeństwa informatycznego, z
naciskiem na ludzki czynnik, wielowarstwową ochronę, ciągłe doskonalenie i
współpracę zewnętrzną, jest kluczowe dla skutecznej obrony przed
współczesnymi zagrożeniami cybernetycznymi. Organizacje, które zrozumieją i
wdrożą te kluczowe elementy, będą lepiej przygotowane do zapobiegania
atakom i reagowania na zmienne wyzwania w dziedzinie bezpieczeństwa
informatycznego.


---


3.7 Social Engineering w praktyce:
a) Phishing:
- Definicja: Phishing to rodzaj ataku, w którym atakujący podszywa się pod
zaufane źródło, takie jak bank, firma, czy też serwis społecznościowy, w celu
zdobycia poufnych informacji, takich jak hasła, numery kart kredytowych itp.
- Przykłady: Fałszywe e-maile od banku wymagające potwierdzenia danych,
fałszywe strony logowania na serwisach społecznościowych, wiadomości SMS
podające się za instytucje finansowe.


b) Pretekstowanie:
- Definicja: Pretekstowanie polega na tworzeniu fałszywych historii lub sytuacji
w celu oszukania ofiary i nakłonienia jej do podjęcia określonych działań, takich
jak ujawnienie poufnych informacji.
- Przykłady: Osoba podająca się za pracownika pomocy technicznej firmy i
prosząca o aktualizację hasła, fałszywy inspektor, który żąda dostępu do
pomieszczeń biurowych.


c) Baiting:
- Definicja: Baiting polega na oferowaniu czegoś atrakcyjnego w celu
nakłonienia ofiary do wykonania określonych działań, zwykle związanych z
instalacją złośliwego oprogramowania lub ujawnieniem poufnych informacji.
- Przykłady: Fałszywe oferty darmowych filmów, muzyki lub programów, które
wymagają instalacji złośliwego oprogramowania, fałszywe dyski USB
pozostawione w miejscach publicznych, które zawierają złośliwe
oprogramowanie.
d) Tailgating:
- Definicja: Tailgating to technika polegająca na wykorzystaniu braku
świadomości lub uprzejmości pracowników w celu uzyskania fizycznego dostępu
do budynku lub pomieszczenia.


---


- Przykłady: Osoba podszywająca się za pracownika i prosi o przepuszczenie jej
przez bramki wejściowe, atakujący korzystający z otwartych drzwi, aby wejść do
biura razem z pracownikiem.


e) Dumpster Diving:
- Definicja: Dumpster diving polega na przeszukiwaniu śmieci w poszukiwaniu
dokumentów, nośników danych lub innych materiałów zawierających poufne
informacje, które mogą być wykorzystane do ataku.
- Przykłady: Znalezienie wyrzuconych dokumentów z wrażliwymi danymi, takimi
jak faktury, notatki z hasłami, kopie dokumentów tożsamości itp.


|. Techniki Wykorzystywane w Social Engineering:xxxxx


a) Ustalenie Celu:
- Definicja: Atakujący zbiera informacje o swojej ofierze, takie jak nazwisko,
stanowisko, hobby, zainteresowania, co pozwala im dostosować swoje ataki do
konkretnej osoby.
- Metody: Przeglądanie profili na mediach społecznościowych, analiza
informacji dostępnych publicznie, wykorzystanie danych z wycieków danych.


b) Wiarygodność:
- Definicja: Atakujący wykorzystuje zaufane źródła, takie jak nazwy firm, loga,
adresy e-mail, aby sprawić, że atak wydaje się autentyczny i godny zaufania.
- Metody: Tworzenie fałszywych stron internetowych, fałszywych e-maili z
zaufanych adresów, wykorzystanie adresów URL podobnych do oryginalnych.


c) Manipulacja Emocjonalna:
- Definicja: Atakujący wykorzystuje emocje ofiary, takie jak strach, ciekawość,
chciwość, aby skłonić ją do podejmowania działań zgodnych z ich intencjami.


---


- Metody: Tworzenie sytuacji kryzysowych, np. grożenie zamknięciem konta
bankowego, obietnice nagród lub korzyści.


d) Społeczne Zasady Wpływu:
- Definicja: Atakujący wykorzystuje zasady wpływu społecznego, takie jak
autorytet, społeczna wartość, brak czasu na decyzję, aby manipulować
zachowaniem ofiary.
- Metody: Poddawanie presji czasowej, podawanie się za autorytety lub osoby z
wysokim statusie, wykorzystywanie społecznej presji.


||. Obrona Przed Social Engineering:xxxxxx


a) Świadomość Użytkowników:
- Definicja: Edukacja pracowników na temat technik social engineering oraz
przestrzeganie polityk bezpieczeństwa organizacji.
- Metody: Szkolenia dotyczące rozpoznawania ataków, testy phishingowe,
podnoszenie świadomości na temat zagrożeń.


b) Monitorowanie Działalności Sieciowej:
- Definicja: Używanie narzędzi monitorujących ruch sieciowy i zachowanie
użytkowników w celu wczesnego wykrycia podejrzanej aktywności.
- Metody: Analiza logów zdarzeń, monitorowanie aktywności użytkowników,
wdrażanie systemów detekcji intruzów.


c) Wspieranie Polityk Bezpieczeństwa:
- Definicja: Wdrażanie silnych polityk bezpieczeństwa, takich jak wieloetapowa
autoryzacja, polityka hasła, ograniczenia dostępu do wrażliwych danych itp.
- Metody: Wymuszenie regularnej zmiany haseł, ograniczenie dostępu do
krytycznych zasobów, kontrola dostępu.


---


d) Zdrowy Rozsądek:
- Definicja: Zachęcanie użytkowników do podejmowania podejrzanych
działaniach, jak np. weryfikacja źródła e-maila lub wiadomości przed kliknięciem
w linki lub załączniki.
- Metody: Edukacja na temat zachowań bezpiecznych w sieci, promowanie
podejrzliwości wobec nieznanych lub niespodziewanych komunikatów.


|||. Przykłady Skutecznych Ataków Social Engineering:


a) Phishing na Wysokim Poziomie:
- Opis: Atakujący podszywa się pod wysokiego rangą pracownika firmy i wysyła
e-maile do pracowników z prośbą o przekazanie poufnych informacji.
- Skutki: Ujawnienie wrażliwych danych, dostęp do systemów firmy, potencjalne
straty finansowe.


b) Fałszywe Akcje Charytatywne:
- Opis: Atakujący wykorzystuje sytuacje kryzysowe, takie jak katastrofy
naturalne, do zbierania pieniędzy na fałszywe cele charytatywne.
- Skutki: Oszustwo finansowe, wyłudzenie pieniędzy od osób dobrej woli,
pogorszenie wizerunku organizacji charytatywnej.


c) Złamanie Bezpieczeństwa Fizycznego:
- Opis: Atakujący wykorzystuje brak kontroli dostępu do budynków lub
pomieszczeń, aby uzyskać fizyczny dostęp do komputerów i infrastruktury
sieciowej.
- Skutki: Kradzież danych, szpiegostwo przemysłowe, sabotowanie
infrastruktury organizacji.


---


   4. Wirusy przejmujące kontrolę systemu


4.1 Trojany
Trojany to rodzaj złośliwego oprogramowania, często udającego legalny
program. Użytkownicy zostają oszukani i pobiorą złośliwy kod, co z kolei daje
atakującemu dostęp do systemu. Aplikacje typu „oprogramowanie jako usługa”
(SaaS) oparte na chmurze są szczególnie atrakcyjne, ponieważ profesjonaliści w
przedsiębiorstwach są przyzwyczajeni do rutynowego klikania łączy
prowadzących do tych usług w ciągu dnia roboczego. Firma Netskope ustaliła,
że drugim najczęstszym typem ataków są trojany, ponieważ pracownicy
pobierali średnio 11 trojanów miesięcznie na 10 000 użytkowników, co oznacza,
że w typowej organizacji tej wielkości użytkownicy pobieraliby średnio 132
trojany rocznie.
Trojany (Trojan Horses), znane również jako trojany, to złośliwe
oprogramowanie, które podszywa się pod pozornie bezpieczne lub użyteczne
aplikacje, aby uzyskać dostęp do systemu komputerowego lub urządzenia
mobilnego. Nazwa "trojan" pochodzi od mitologicznego konia trojańskiego,
który był prezentem dla Troi, ale w rzeczywistości ukrywał w sobie żołnierzy,
którzy zaatakowali miasto. Podobnie jak w mitologii, trojany wyglądają na coś
niewinnego lub pożytecznego, ale w rzeczywistości są szkodliwe i mogą
powodować znaczne szkody.


Charakterystyka i działanie trojanów:
Trojany często przychodzą w formie pozornie bezpiecznych lub pożytecznych
aplikacji, takich jak darmowe gry, narzędzia optymalizacji systemu, czy nawet
narzędzia antywirusowe. Mogą być również ukryte w załącznikach e-maili lub
linkach do pobierania plików.


Zachowanie:
Po zainstalowaniu, trojan może wykonywać różne złośliwe działania, w
zależności od rodzaju. Może to obejmować kradzież danych, instalowanie
dodatkowego złośliwego oprogramowania, zdalne sterowanie komputerem,
szpiegowanie aktywności użytkownika, przekierowywanie przeglądarki, lub
nawet przeprowadzanie ataków DDoS (Distributed Denial of Service).


---


Zdolność Ukrycia:
Trojany często próbują ukryć swoje działania przed użytkownikiem i systemem
operacyjnym, aby trudniej było je wykryć. Mogą ukrywać swoje pliki, procesy,
oraz zmieniać swoje cechy, aby uniknąć wykrycia przez programy antywirusowe.


Uwierzytelnienie:
Często trojany wykorzystują techniki socjotechniczne, takie jak phishing, aby
nakłonić użytkownika do samodzielnego uruchomienia złośliwego pliku lub
pobrania zainfekowanej aplikacji, co sprawia, że atak jest bardziej skuteczny.


4.2 Rodzaje trojanów:


Trojany dostępu zdalnego (RATs):
Pozwalają atakującemu na zdalne kontrolowanie komputera ofiary. Zwykle
wykorzystywane do kradzieży danych, szpiegowania aktywności użytkownika
lub przeprowadzania ataków z botnetu.


Trojany bankowe:
Zaprojektowane do kradzieży danych logowania i innych informacji finansowych
użytkowników, zwykle poprzez keylogging (rejestrację klawiszy), phishing lub
przechwytywanie sesji.


Trojany backdoor:
Otwierają "tylnie drzwi" w systemie komputerowym, umożliwiając atakującemu
zdalny dostęp i kontrolę nad systemem.


---


Trojany ransomware:
Szyfrują pliki na zainfekowanym komputerze i żądają okupu za ich
odszyfrowanie. Bardzo niebezpieczne, ponieważ mogą poważnie zakłócić
działalność użytkownika lub organizacji.
Trojany wyszukiwarek:
Modyfikują ustawienia przeglądarki internetowej, aby przekierowywać
użytkownika na fałszywe strony lub wyświetlać niepożądane reklamy.


4.3 Ochrona przed trojanami
Aktualizacje oprogramowania:
Regularne aktualizacje oprogramowania pomagają w usuwaniu luk
bezpieczeństwa, które mogą być wykorzystane przez trojany do infekcji
systemu.


Oprogramowanie antywirusowe:
Skuteczne programy antywirusowe mogą wykrywać i usuwać trojany z
zainfekowanego systemu, zapewniając dodatkową warstwę ochrony.


Ostrożność przy korzystaniu z Internetu:
Unikanie klikania w podejrzane linki, pobierania plików z niezaufanych źródeł
oraz otwierania załączników e-mailowych od nieznanych nadawców.


Zapora sieciowa:
Wykorzystanie zapory sieciowej może pomóc w blokowaniu prób połączenia się
trojanów z zewnętrznymi serwerami kontrolnymi.


---


Regularne skany systemu:
Wykonywanie regularnych skanów systemu przy użyciu oprogramowania
antywirusowego lub anty-malware może pomóc w wczesnym wykrywaniu i
usuwaniu trojanów z komputera.
Trojany są jednym z najbardziej niebezpiecznych rodzajów złośliwego
oprogramowania ze względu na ich zdolność do ukrywania się i wykonywania
różnych złośliwych działań. Wiedza o nich i stosowanie odpowiednich praktyk
bezpieczeństwa są kluczowe dla zapobieżenia infekcji i ochrony komputerów
oraz danych użytkowników.


4.4 Black Basta
Ataki typu Trojan ciągle występują. Poniższe kilka przykładów ukazuje, że nawet
bardzo duże firmy mogą paść ofiarami Trojanów.
W ostatnich latach zaobserwowano gwałtowny wzrost liczby ataków
ransomware, z grupą Black Basta na czele jako jednym z głównych aktorów tego
niebezpiecznego trendu. Powstanie i rozwój Black Basta są reprezentatywne dla
ewolucji strategii i technik stosowanych przez nowoczesne grupy
cyberprzestępcze.
Black Basta zadebiutowała na scenie w lutym 2022 roku, jednak badacze
uważają, że jej członkowie mieli wcześniejsze doświadczenie w innych grupach,
takich jak Conti i REvil, co sugeruje kontynuację i adaptację istniejących modeli
biznesowych przestępczych.
Jedną z kluczowych cech grupy Black Basta jest jej szybki wzrost oraz
podejmowanie współpracy z innymi operacjami cyberprzestępczymi, takimi jak
QBot, co przyczynia się do zwiększenia skuteczności i zasięgu ataków.
Partnerstwo z QBotem umożliwia grupie Black Basta wykorzystanie szerokiej
gamy funkcji i narzędzi do przeprowadzania ataków oraz szybkiego
rozprzestrzeniania się oprogramowania ransomware.
Techniki stosowane przez Black Basta są zgodne z najlepszymi praktykami
innych grup ransomware, takich jak podwójne szyfrowanie, wyłączanie
programów antywirusowych i wykorzystanie PowerShell do wdrożenia
złośliwego oprogramowania. Jednakże, co stanowi wyzwanie dla firm i
instytucji, Black Basta ciągle ewoluuje i dostosowuje swoje strategie, co
utrudnia przewidywanie i zapobieganie atakom.


---


Grupa nie tylko atakuje pojedyncze maszyny, ale także masowo szyfruje serwery
firmowe, w tym te działające na platformie VMware ESXi, co zwiększa skalę i
skutki ataków. Ich żądania okupu są wysokie, a brak skutecznej obrony może
prowadzić do znacznych strat finansowych i reputacyjnych dla ofiar.
Jednakże, pomimo szybkiego wzrostu i agresywnych działań, wiele pozostaje
jeszcze nieznane na temat grupy Black Basta, włączając w to ich motywacje,
skład i strukturę organizacyjną. Niemniej jednak, stały rozwój i ekspansja grupy
wskazują na pilną potrzebę podjęcia skutecznych działań zaradczych oraz
współpracy międzysektorowej w celu zwalczania rosnącego zagrożenia ze strony
grup ransomware.
Jednym z większych celów ataków grupy była globalna korporacja ABB, której
struktury zostały zainfekowane w maju 2023 roku. Według informacji
uzyskanych przez BleepingComputer, atak ransomware dotknął firmowe
Windows Active Directory i miał wpływ na setki urządzeń.
W odpowiedzi na atak, ABB zamknęła połączenia VPN ze swoimi klientami w
celu zapobieżenia rozprzestrzenianiu się ransomware na inne sieci. Według
doniesień, ransomware zakłóciło działalność firmy, powodując opóźnienia w
projektach i wpływając na działanie fabryk.
Od momentu swojego powstania, cyberprzestępcy z Black Basta byli
odpowiedzialni za szereg ataków, w tym na American Dental Association,
Sobeys, Knauf i Yellow Pages Canada. Ostatnio grupa zaatakowała firmę Capita,
największą brytyjską spółkę outsourcingową i zaczęła ujawniać skradzione dane.


4.5 Krypta 7 (Vault 7)
Vault 7 to seria dokumentów, które portal WikiLeaks zaczął publikować 7 marca
2017 roku, szczegółowo opisując działania i możliwości Centralnej Agencji
Wywiadowczej Stanów Zjednoczonych (CIA) w zakresie inwigilacji elektronicznej
i cyberwojny.
Pliki, pochodzące z lat 2013-2016, zawierają szczegółowe informacje na temat
możliwości oprogramowania agencji, takich jak zdolność do kompromitowania
samochodów, inteligentnych telewizorów, przeglądarek internetowych, w tym
Google Chrome, Microsoft Edge, Mozilla Firefox i Opera, systemów
operacyjnych większości smartfonów, w tym Apple iOS i Google Android, oraz


---


komputerowych systemów operacyjnych, w tym Microsoft Windows, macOS i
Linux.
Wewnętrzny audyt CIA zidentyfikował 91 narzędzi złośliwego oprogramowania z
ponad 500 narzędzi używanych w 2016 r., które zostały naruszone przez
wydanie. Narzędzia zostały opracowane przez Oddział Wsparcia Operacyjnego
CIA.
Ujawnienie Vault 7 doprowadziło CIA do przedefiniowania WikiLeaks jako
"niepaństwowej wrogiej służby wywiadowczej". W lipcu 2022 r. były inżynier
oprogramowania CIA Joshua Schulte został skazany za wyciek dokumentów do
WikiLeaks, a w lutym 2023 r. skazany na 40 lat więzienia




Joshua Schulte – główny podejrzany oskarżony o udostępnienie tajnych
informacji do serwisu WikiLeaks.


Historia
Według doniesień medialnych w lutym 2017 r. WikiLeaks zaczęło drażnić się z
wydaniem "Vault 7" serią tajemniczych wiadomości na Twitterze. Później w
lutym WikiLeaks opublikowało tajne dokumenty opisujące, w jaki sposób CIA
monitorowała wybory prezydenckie we Francji w 2012 r. W komunikacie


---


prasowym dotyczącym wycieku stwierdzono, że został on opublikowany "jako
kontekst dla nadchodzącej serii CIA „Vault 7”
W marcu 2017 roku amerykańscy urzędnicy wywiadu i organów ścigania
powiedzieli międzynarodowej agencji Reuters, że byli świadomi naruszenia
bezpieczeństwa CIA, które doprowadziło do wycieku Vault 7 od końca 2016
roku. Dwóch urzędników stwierdziło, że koncentrują się na "wykonawcach" jako
możliwym źródle przecieków.


4.6 Część 1 - "Rok Zero"
Pierwsza partia dokumentów o nazwie "Year Zero" została opublikowana przez
WikiLeaks w dniu 7 marca 2017 r. i składała się z 7818 stron internetowych z
943 załącznikami, rzekomo pochodzących z Center for Cyber Intelligence, które
zawierały więcej stron niż były wykonawca NSA i przeciek Edwarda Snowdena.
WikiLeaks opublikował Year Zero online w zamkniętym archiwum wcześniej w
tym samym tygodniu, ujawniając hasło 7 marca. Hasło odnosiło się do cytatu z
prezydenta Kennedy'ego, który chciał "rozbić CIA na tysiąc kawałków i rozrzucić
je na wietrze".
WikiLeaks nie podało źródła, ale stwierdziło, że pliki "krążyły wśród byłych
hakerów i wykonawców rządu USA w nieautoryzowany sposób, z których jeden
dostarczył WikiLeaks fragmenty archiwum". "Według WikiLeaks, źródło "pragnie
zainicjować publiczną debatę na temat bezpieczeństwa, tworzenia,
wykorzystywania, rozprzestrzeniania i demokratycznej kontroli broni
cybernetycznej", ponieważ narzędzia te podnoszą kwestie, które "pilnie
wymagają publicznej debaty, w tym, czy możliwości hakerskie CIA przekraczają
jej uprawnienia i problem publicznego nadzoru nad agencją".
Łącznie udostępniono 24 części, ujawniające coraz więcej metod oraz
dowodów, że CIA szpiegowało ludzi bez ich zezwolenia


4.7 Najpopularniejsze rodzaje Trojanów / wirusów


-ZEUS
Jednym z najpopularniejszych „Trojanów” jest oprogramowanie to kryptonimie
Zeus.


---


Służy on do kradzieży danych oraz informacji bankowych poprzez rejestrację
naciśnięć klawiszy i przechwytywanie formularzy.
Został on zidentyfikowany w połowie 2007 roku, kiedy został wykorzystany do
kradzieży danych z USDOT (United States Department of Transportation)


W 2009 roku, firma Prevx przekazała, że Zeus stał za ponad 75 tysiącami
włamań na konta FTP na stronach typu Amazon, Cisco, Oracle, NASA czy
BusinessWeek.
W październiku 2010 roku amerykańskie FBI ogłosiło, że hakerom w Europie
Wschodniej udało się zainfekować komputery na całym świecie za pomocą
Zeusa.
Wirus był rozprzestrzeniany w wiadomościach e-mail, a gdy osoby skierowane
do firm i gmin otworzyły tę wiadomość, trojan instalował się na komputerze
ofiary, potajemnie przechwytując hasła, numery kont i inne dane używane do
logowania się do bankowości internetowej konta.
Hakerzy wykorzystali następnie te informacje do przejęcia kont bankowych ofiar
i dokonania jednorazowo nieautoryzowanych przelewów na kwotę tysięcy
dolarów, często kierując środki na inne konta kontrolowane przez sieć mułów
pieniężnych, za co płacili prowizję.
Wiele amerykańskich mułów zostało rekrutowanych z zagranicy. Założyli konta
bankowe, posługując się fałszywymi dokumentami i fałszywymi nazwiskami.
Gdy pieniądze znalazły się na rachunkach, muły albo przesyłały je z powrotem
do swoich szefów w Europie Wschodniej, albo wypłacały je w gotówce i
przemycały z kraju.


-SpyEye
SpyEye to szkodliwy program atakujący użytkowników przeglądarek Google
Chrome, Opera, Firefox i Internet Explorer w systemach operacyjnych Microsoft
Windows.
To złośliwe oprogramowanie wykorzystuje rejestrowanie naciśnięć klawiszy i
przechwytywanie formularzy w celu kradzieży danych uwierzytelniających
użytkownika w celu złośliwego wykorzystania.


---


SpyEye umożliwia hakerom kradzież pieniędzy z internetowych kont bankowych
i inicjowanie transakcji nawet wtedy, gdy właściwi użytkownicy są zalogowani
na swoim koncie bankowym.
Oprogramowanie ma możliwość wstawiania nowych pól i modyfikowania
istniejących, gdy przeglądarka zaatakowanego użytkownika wyświetla stronę
internetową, co pozwala na monitorowanie zapytań o podanie nazwy
użytkownika, hasła lub numeru karty, dostarczając w ten sposób hakerom
informacje, które umożliwiają im kradzież pieniędzy bez wiedzy użytkownika.
Może również zapisać fałszywe saldo użytkownika (z ukrytymi fałszywymi
transakcjami), dzięki czemu przy następnym logowaniu użytkownika fałszywe
transakcje i saldo rzeczywiste nie zostaną wyświetlone w przeglądarce
użytkownika (chociaż bank nadal widzi fałszywe transakcje).


SpyEye pochodzi z Rosji oraz od 2009 roku jest sprzedawany na podziemnych
forach za ponad 500 dolarów, na których SpyEye reklamuje takie funkcje, jak:
   ● rejestratory naciśnięć klawiszy
   ● moduły kart kredytowych z automatycznym uzupełnianiem,
   ● kopie zapasowe wiadomości e-mail
   ● pliki konfiguracyjne (zaszyfrowane)
   ● Zabójca Zeusa
   ● dostęp poprzez http (niezabezpieczone SSL’em)
   ● grabbery POP3
   ● grabbery FTP


Największymi ofiarami SpyEye byli docelowi użytkownicy i instytucje w Stanach
Zjednoczonych, Wielkiej Brytanii, Meksyku, Kanadzie i Indiach.


-RedLine
Malware RedLine jest trojanem wykorzystującym samorozpakowujące się
archiwum RAR, które zawiera złośliwe pliki i skrypty. Po uruchomieniu może
kraść dane z przeglądarek, portfeli kryptowalut i klientów FTP/SSH/VPN, a także
wykonywać polecenia w cmd.exe oraz otwierać linki za pomocą domyślnej
przeglądarki.


---


Dodatkowo zawiera program do kopania kryptowalut i narzędzia do
samodystrybucji, np. poprzez publikowanie filmów z złośliwymi linkami na
zhakowanych kanałach YouTube. RedLine jest dostępny na forach hakerskich za
stosunkowo niewielką cenę. Ważne jest zachowanie ostrożności wobec
podejrzanych linków na YouTube, szczególnie dla dzieci.


-Remcos
Remcos RAT jest jednym z najbardziej rozpowszechnionych zagrożeń w polskiej
sieci w ostatnich latach. Co ciekawe, jest również stosunkowo łatwe do
wykrycia, ponieważ używa identycznego wektora ataku – podszywa się pod
autentyczną korespondencję z istniejącą firmą.
Dlatego też głównymi celami przestępców, którzy prowadzą kampanie
wykorzystujące trojana Remcos, są firmy. Zwłaszcza małe lub średnie
przedsiębiorstwa, ponieważ w większych organizacjach procedury
postępowania z dokumentami przesyłanymi mailem są często bardziej
zaawansowane (lub przynajmniej tak można by przypuszczać).
Sztuczka polegająca na wykorzystaniu Remcosa opiera się na tym, że atakujący
włączają się w rzeczywisty przepływ korespondencji e-mailowej. Jak to
możliwe? Otóż atakujący najpierw włamują się do innej firmy, która
współpracuje z docelową ofiarą.
W takiej sytuacji jest naprawdę łatwo, nawet z impetem, kliknąć w
załącznik.Ciężko będzie nawet taką sytuację uznać za nierozważną, tym bardziej,
że język polski jest bez zarzutu. Podejrzewamy, że atakujący po włamaniu do
sieci firmy, której nazwa zaczyna się na „Ke”, również przyjrzał się formie
wypowiedzi mailowych Pana Wiesława.


Co się dzieje po kliknięciu?
W załączniku maila znajduje się dokument: Zapytanie ofertowe.doc
Plik wykorzystuje podatność CVE-2017-11882 w Edytorze Równań (Microsoft
Office Equation Editor), aby pobrać i uruchomić złośliwy kod z adresu
hxxp://fresh1.ironoreprod[.]top/_errorpages/chungzx.exe


---


Pobrany payload z plikiem wykonywalnym zawiera Remcos RAT – komercyjne
złośliwe oprogramowanie, sprzedawane w modelu Malware-as-a-Service,
dedykowane do kradzieży haseł i danych dostępowych, podsłuchiwania
aktywności użytkownika oraz przejęcia zdalnej kontroli nad zainfekowanym
urządzeniem. Przykładem może być funkcja:
take_screenshot_title: Username;password;proforma;invoice;notepad
która powoduje wykonanie zrzutu ekranu w momencie wykrycia
zaprogramowanych słów kluczowych.


-Melissa
Wirus Melissa to złośliwe oprogramowanie stworzone przez Davida L. Smitha w
1999 roku. Rozprzestrzeniał się poprzez zainfekowane dokumenty Worda
przesyłane za pośrednictwem poczty elektronicznej.
Po otwarciu zainfekowanego załącznika, wirus wysyłał kopie samego siebie do
pierwszych 50 adresów e-mail z książki adresowej ofiary. Szybko rozprzestrzenił
się na tysiące komputerów na całym świecie, powodując duże problemy z
wydajnością sieci i systemów informatycznych.
Firmy musiały często wyłączać swoje systemy e-mailowe, aby powstrzymać
infekcję. Smith został aresztowany przez FBI i skazany na 20 miesięcy więzienia
oraz nałożono na niego grzywnę.
Wirus Melissa jest nadal uważany za jednego z najbardziej wpływowych i
szkodliwych w historii, zwracając uwagę na potrzebę większej świadomości i
ostrożności w zakresie bezpieczeństwa cybernetycznego.


-MEMZ.EXE
MEMZ (wymawiane: memes / mims) to złośliwy wirus komputerowy w postaci
konia trojańskiego stworzonego dla systemu Microsoft Windows.
Nazwa wirusa odnosi się do jego przeznaczenia jako wirusa humorystycznego,
którego zadaniem jest replikowanie skutków wczesnych wirusów
komputerowych.
MEMZ został pierwotnie stworzony przez „Leurak” dla serii Viewer-Made
Malware YouTubera danooct1.Został on później zaprezentowany przez Joela


---


Johanssona, alias Vargskelethor, członka grupy zajmującej się streamowaniem
Vinesauce w jego serii Windows Destruction, który zademonstrował trojana w
działaniu przeciwko maszynie wirtualnej z systemem Windows 10 - po
otrzymaniu kopii od danooct1.
Zasady działania
Uruchamiamy pobrany plik MEMZ.exe




https://www.youtube.com/watch?v=9Deg7VrpHbM




Po wybraniu opcji Yes, wirus aktywuje się na naszych systemie. Wirus co prawda
nie jest szkodliwy jeśli chodzi o dane poufne, jednakże uniemożliwi nam
ponowne bootowanie komputera. Wirus ma być śmiesznym
oprogramowaniem, które ma przypominać swoim zachowaniem wirusy z latach
05-15. (pop-upy, automatyczne wyświetlanie różnych stron internetowych,


---


automatyczne odtwarzanie dźwięków systemu Windows, zmiana tapety co kilka
sekund, zmiana kursora, odwrócenie obrazu do góry nogami, losowe usuwanie
ikon na pulpicie. Po zaledwie kilku minutach, pulpit wygląda następująco:




4.8 WATYKAŃCZYK
Teraz przykład z rodzimego podwórka, wirus ten swego czasu był najczęściej
uruchamianym „przewodnikiem” w mojej szkole na lekcjach informatyki.
(Krążyła legenda, że ten program aktywował „cheaty” w Minecraft’cie, a
pierwszoklasiści bardzo szybko łapali się na tego typu rzeczy )
Wszystko zaczynało się o uruchomienia jednego, niewinnego programu:



Na „dzień dobry” witał nas komunikat:


---


Po kliknięciu OK, (lub X) w tle zaczynała grać mocno przesterowana wersja barki
oraz co kilka sekund wyskakiwały różne komunikaty związane z polskim
Papieżem (niezbyt przychylne).


---


Uruchamiały się również linki do filmów z YouTube:




Po ponownym uruchomieniu komputera, witał nas komunikat przedstawiony na
pierwszym zdjęciu.
Watykańczyk, pomimo swojego agresywnego zachowania (oraz obrażania na
wszelakie sposoby) nie jest programem wykradających dane osobowe, jednakże
zużywa mnóstwo zasobów, uniemożliwiając jakąkolwiek pracę. Dochodzi do
tego jeszcze nieustannie rozbrzmiewająca barka w tle. Konieczna była
reinstalacja systemu, ale wszelkie zachowane zdjęcia, filmy oraz dokumenty
pozostawały nienaruszone. Ot to tylko program do wywoływania zakłopotania
nauczycieli na lekcjach informatyki
Zero-day exploit
Termin „dzień zerowy” pierwotnie odnosił się do liczby dni od upublicznienia
nowego oprogramowania, zatem „oprogramowanie dnia zerowego” uzyskiwano
w wyniku włamania się do komputera programisty przed jego udostępnieniem.
Ostatecznie termin ten został zastosowany do luk w zabezpieczeniach, które
umożliwiły to włamanie, oraz do liczby dni, przez które dostawca musiał je
naprawić.Dostawcy, którzy odkryją tę lukę, mogą stworzyć łaty lub zalecić
obejścia jej ograniczenia – chociaż użytkownicy muszą wdrożyć to rozwiązanie,
aby wyeliminować lukę w swoich systemach. Ataki dnia zerowego stanowią
poważne zagrożenie.
Niedawno, firma AMD, produkująca sprzęt komputerowy, padła ofiarą luki
zabezpieczeń w układach procesorów z serii Ryzen 3000. Luka otrzymała


---


kryptonim Zenbleed. AMD musiało bardzo szybko wydać łatkę, która miała
zapobiec nieautoryzowanemu dostępowi nieproszonych użytkownikom. Wpływ
wprowadzonych poprawek nie został oficjalnie ogłoszony, jednakże po
wprowadzeniu jej, procesor z automatu zużywa więcej zasobów.
Po zębach dostało się również największej konkurencji. Exploit Downfall
spowodował w Intelu konieczność wprowadzenia poprawek do procesów
produkowanych od 2016 (Skylake) do 2019 (Rocket Lake/Tiger Lake). Niestety,
tak jak i w przypadku AMD, procesory znacznie zwolniły po wprowadzeniu
poprawek. Exploit pozwalał wykraść 128 i 256 bitowe klucze szyfrujące AES.




Porównanie wydajności i7-1165G7 bez (0xa6) oraz z poprawką (0xac)


---


4.9 Podsumowanie i wnioski
Referat omawiał trzy kluczowe zagadnienia: Vault 7, trojany oraz
nieautoryzowany dostęp do komputera i danych. Vault 7 to zbiór tajnych
dokumentów ujawnionych przez WikiLeaks, które dotyczą narzędzi i technik
wywiadowczych używanych przez CIA. W referacie omówiono różne aspekty
tych narzędzi oraz ich potencjalne konsekwencje dla prywatności i
bezpieczeństwa użytkowników.
Trojany są rodzajem złośliwego oprogramowania, które podszywa się pod
legalne pliki lub programy, aby uzyskać dostęp do systemu komputerowego.
Omówiono różne metody propagacji trojanów oraz sposoby ich działania,
włączając w to kradzież danych, szpiegostwo czy też zniszczenie systemu.
Nieautoryzowany dostęp do komputera i danych to problem, który dotyka
zarówno jednostek prywatnych, jak i organizacje. Omówiono różne sposoby, w
jakie atakujący mogą uzyskać nielegalny dostęp do danych oraz skutki takich
działań, w tym kradzież tożsamości, utratę poufnych informacji czy też szkody
finansowe.


Wnioski:
1. Wzrost cyberzagrożeń wymaga podjęcia skutecznych środków ochrony
danych i systemów komputerowych. Niezwykle istotne jest stosowanie
zaktualizowanego oprogramowania zabezpieczającego oraz świadomość
użytkowników w zakresie praktyk bezpieczeństwa online.
2. Konieczne jest regularne szkolenie personelu w zakresie identyfikacji
potencjalnych zagrożeń oraz odpowiednich procedur reagowania w przypadku
ataku.
3. Organizacje i jednostki powinny stosować polityki bezpieczeństwa danych, w
tym zasady dostępu i zarządzania hasłami, aby minimalizować ryzyko
nieautoryzowanego dostępu.
4. Współpraca międzynarodowa oraz wymiana informacji na temat zagrożeń
cybernetycznych są kluczowe dla skutecznej ochrony danych i zapobiegania
atakom.


---


5. Ciągłe badania nad nowymi rodzajami zagrożeń są niezbędne, aby
dostosowywać strategie obronne do zmieniającego się krajobrazu
cyberbezpieczeństwa.


Bibliografia:
   •   HTTPS :// WWW .KEEPERSECURITY .COM / PL_PL/ THREATS / MAN-IN-THE -MIDDLE -ATTACKS -MITM .HTML


   •   HTTPS :// WWW .KALILINUX .IN/2022/01/ WIFITE .HTML


   •   HTTPS :// WWW .DOBREPROGRAMY .PL/ ATAKI -NA -WI -FI -ZABEZPIECZMY -SIE -OFENSYWNIE -METODAMI-


       HAKEROW ,6628341837260417 A


   •   HTTPS :// SEKURAK .PL/ CZYM -JEST -SQL-INJECTION /


   •   HTTPS :// SEKURAK .PL/ CZYM -JEST -XSS /


   •   HTTPS :// WWW .AKAMAI .COM /US / EN/ PRODUCTS / SECURITY / DDOS -PROTECTION .JSP



   •   HTTPS :// NANO.KOMPUTRONIK .PL/ N/ CO-TO -JEST -ATAK -DDOS /


   •   HTTPS :// KWESTIABEZPIECZENSTWA .PL/ ATAK -DDOS /


   •   HTTPS :// DHOSTING .PL/ POMOC/ BAZA -WIEDZY / RODZAJE -ATAKOW-DDOS /


   •   HTTPS :// BORINGOWL .IO/ BLOG/ATAK -DDOS


   •   HTTPS :// WWW .OVHCLOUD .COM/ PL/ SECURITY / ANTI -DDOS /


   •   HTTPS :// EXATEL .PL/ USLUGI / CYBERBEZPIECZENSTWO /ANTY -DDOS -TAMA /


   •   HTTPS :// WWW .NASK .PL/PL/ AKTUALNOSCI / OFERTA / OFERTA -


       TELEKOMUNIKACYJN / BEZPIECZENSTWO /2662,DD OS-ATTACK -PROTECTION .HTML


   •   HTTPS :// WWW .ORANGE .PL/ DUZE -FIRMY / DDOS -PROTECTION


   •   HTTPS :// WWW .US -CERT .GOV / NCAS / TIPS /ST04-015


   •   HTTPS :// HARVARDNSJ .ORG /2017/02/ THE - DYN-DDOS - ATTACK /


   •   HTTPS :// WWW .CLOUDFLARE .COM / LEARNING / DDOS / FAMOUS -DDOS -ATTACKS /


   •   HTTPS :// BITDEFENDER .PL/ABC-CYBERBEZPIECZENSTWA -D-JAK -ATAK -DOS /


   •   HTTPS :// PL.WIKIPEDIA .ORG /WIKI /DDO S


   •   HTTPS :// WWW .MDPI .COM /2224-2708/12/4/51


   •   HTTPS :// ARXIV .ORG / FTP /ARXIV/ PAPERS /2208/2208.14205. PDF


---


•   HTTPS :// WWW .HINDAWI .COM/ JOURNALS /SCN /2021/5710028/


•   HTTPS :// WWW .MDPI .COM /2079-9292/10/4/406


•   HTTPS :// ARXIV .ORG / ABS /2103.10113


•   HTTPS :// IEEEXPLORE . IEEE .ORG / DOCUMENT /9259808


•   HTTPS :// WWW .SPRINGER .COM /GP /BOOK /9783319339524


•   HTTPS :// LINK .SPRINGER .COM / ARTICLE /10.1007/ S 11277-020-07228-6


•   HTTPS :// WWW .SCIENCEDIRECT .COM / SCIENCE /ARTICLE / PII/S2405959520300530


•   HTTPS :// WWW .SCIENCEDIRECT .COM / SCIENCE /ARTICLE / PII/S0167739X20331600


•   HTTPS :// WWW .SCIENCEDIRECT .COM / SCIENCE /ARTICLE / PII/S1389128620304830


•   HTTPS :// WWW .SCIENCEDIRECT .COM / SCIENCE /ARTICLE / PII/S240595951730258X


•   https://www.sciencedirect.com/science/article/pii/S240595951830118X

•   HTTPS :// WWW .GOV . PL/ WEB /BAZA -WIEDZY / CZYM -JEST -PHISHING-I -JAK -NIE -DAC-SIE -NABRAC -NA -PODEJRZANE -
    WIDOMOSCI -E -MAIL-ORAZ -SMS -Y


•   HTTPS :// WWW .EY .COM / PL_PL/CONSULTING / PHISHING -CO-TO-JEST


•   HTTPS :// KWESTIABEZPIECZENSTWA .PL/ PHISHING /


•   HTTPS :// PL.MALWAREBYTES .COM / PHISHING /


•   HTTPS :// NIEBEZPIECZNIK .PL/ POST / UWAGA -KLIENCI -MBANKU -UDZIELAJACY -SIE -NA -OFICJALNYM -FORUM -
    MBANKU /


•   HTTPS :// MEDIA .KASPERSKYDAILY .COM / WP -CONTENT / UPLOADS /SITES /95/2019/06/05124136/ TOP 4-
    DANGEROUS -ATTACHMENTS -2019-FEATURED -A.JPG


•   HTTPS :// PLBLOG .KASPERSKY .COM / PHISHING -PSYCHOLOGY /10278/


•   HTTPS :// POLICJA .PL/ POL/ AKTUALNOSCI /212455,T OP -5-NAJCZESTSZYCH -TECHNIK -PHISHINGOWYCH .HTML


•   HTTPS :// WWW .SIRT.PL/ CONTENT / IMAGES /2023/06/ SMS .JPG


•   HTTPS :// ELK .POLICJA .GOV .PL/ O05/ AKTUALNOSCI /107321,H EJ - MAMO-TO-MOJ -NOWY -NUMER -ZAPISZ -GO-
    UWAZAJ-NA -TAKIE -WIADOMOSCI .HTML


•   HTTPS :// PANWYBIERAK .PL/ BLOG/ INWESTUJESZ -PRZEZ -INTERNET -UWAZAJ-TO-POPULARNA -FORMA-OSZUSTWA /


•   HTTPS :// BEZPIECZNYMIESIAC .PL/ BM / BAZA -WIEDZY /654,P HISHING .HTML


•   HTTPS :// WWW .AVAST .COM / PL-PL/ C-WANNACRY


•   HTTPS :// CERT .PL/ POSTS /2017/05/ WANNACRY -RANSOMWARE /


•   HTTPS :// PL.WIKIPEDIA .ORG /WIKI /ATAK _N OTPETYA


---


•   HTTPS :// CYBERDEFENCE 24.PL/ CYBERBEZPIECZENSTWO / CYBERATAK -NOTPETYA -JEST -POROZUMIENIE -MIEDZY -
    POSZKODOWANA -FIRMA -A -UBEZPIECZYCIELEM


•   HTTPS :// WWW .GOV . PL/ WEB / RCB / RANSOMWARE -W -NOWEJ -ODSLONIE


•   HTTPS :// NEXT .GAZETA .PL/ NEXT /7,151243,22020254, JAK -DZIALA -WIRUS -PETYA -NOTPETYA -I -DLACZEGO -
    ATAKUJE -KOMPUTERY . HTML


•   HTTPS :// WWW .TRENDMICRO .COM / PL_PL/ WHAT-IS / RANSOMWARE / RYUK -RANSOMWARE . HTML


•   HTTPS :// WWW .2-SPYWARE .COM/ REMOVE -RYUK -RANSOMWARE .HTML


•   HTTPS :// NEWS .SOPHOS .COM /EN-US /2020/10/14/ INSIDE -A -NEW -RYUK -RANSOMWARE -ATTACK /


•   HTTPS :// WWW .MALWAREBYTES .COM / RYUK -RANSOMWARE


•   HTTPS :// WWW .CRYPTO -IT.NET/ PL/ SYMETRYCZNE / AES .HTML


•   HTTPS :// WWW .COMPUTERWORLD .PL/ NEWS /AES-128-VS -AES-256- CZYM -ROZNIA -SIE -ZNANE -STANDARDY -
    SZYFROWANIA ,445242. HTML


•   HTTPS :// WWW .VIDA . PL/ RANSOMWARE -RYUK -NISZCZYCIELSKIE -OPROGRAMOWANIE -SZYFRUJACE -DANE /


•   HTTPS :// CYBERDEFENCE 24.PL/ SOCIAL-MEDIA / CYBERMAGAZYN -SOCJOTECHNIKA -CZYLI -KROTKO -O-TYM -JAK -
    CYBERPRZESTEPCY -WYKORZYSTUJA -NASZE -SLABOSCI


•   HTTPS :// EMAILLABS .IO/ CYBERLABS -4-SOCJOTECHNIKA -CZYLI -HACKOWANIE -LUDZKICH -UMYSLOW /


•   HTTPS :// ATFIDE .PL/ CYBERBEZPIECZENSTWO -ATAKI -HAKERSKIE -Z-UZYCIEM -SOCJOTECHNIKI /


•   HTTPS :// WWW .SPYSHOP .PL/ BLOG / SQL-INJECTION -CZYM -JEST -I -JAK -ZAGRAZA -TWOJEJ -STRONIE -INTERNETOWEJ /


•   HTTPS :// WEBSITESECURITYSTORE .COM / BLOG /GUIDE -SQL -INJECTION -ATTACK -WHAT -IS -IT-HOW -TO -PREVENT -IT/


•   HTTPS :// WWW .SPYSHOP .PL/ BLOG / SQL-INJECTION -CZYM -JEST -I -JAK -ZAGRAZA -TWOJEJ -STRONIE -INTERNETOWEJ /


•   HTTPS :// WWW .POLITYKABEZPIECZENSTWA .PL/ PL/ A /SOCIAL -ENGINEERING -JAK -CHRONIC-SWOJA -FIRME -PRZED -
    MANIPULACJA -LUDZKA


•   HTTPS :// WWW .POLITYKABEZPIECZENSTWA .PL/ PL/ A /SPEAR -PHISHING -NA -PRACOWNIKOW -POLSKICH -INSTYTUCJI -
    PUBLICZNYCH


•   HTTPS :// NORDVPN .COM /PL/ BLOG / SOCJOTECHNIKA -CO-TO/


•   HTTPS :// HAKER .EDU . PL/2016/05/15/ SQL-INJECTION -W -PRAKTYCE -WEP -18/


•   HTTPS :// HAKER .EDU . PL/2016/05/20/ SQLMAP -JSQL-W -KALI -LINUX -WEP -20/


•   HTTPS :// KRYSTIANBROZEK .PL/ ATAK -SQL-INJECTION /


•   HTTPS :// PL.WIKIPEDIA .ORG /WIKI /C ROSS -SITE _SCRIPTING


•   HTTPS :// SEKURAK .PL/ CZYM -JEST -XSS /


•   HTTPS :// OWASP .ORG /WWW -COMMUNITY / ATTACKS / XSS /


---


•   HTTPS :// OWASP .ORG /WWW -COMMUNITY / ATTACKS / CSRF


•   HTTPS :// SEKURAK .PL/ CZYM -JEST -PODATNOSC -CSRF -CROSS -SITE -REQUEST -FORGERY /


•   HTTPS :// PORTSWIGGER .NET/ WEB -SECURITY/ CSRF


•   HTTPS :// SEKURAK .PL/ MASTERING -BURP -SUITE -CZ-1-POZNAJ -SEKRETY -TOPOWEGO -NARZEDZIA -DLA -
    PENTESTEROW -WEB -APLIKACJI /


•   HTTPS :// SZKOLASECURITY .PL/ NARZEDZIA -PENTESTERA -BURP -SUITE -WPROWADZENIE /


•   HTTPS :// FANKAKODOWANIA .PL/NARZEDZIA -PENTESTERA -JAK -SKONFIGUROWAC-BURP -SUITE /


•   HTTPS :// EN.WIKIPEDIA .ORG /WIKI /B URP _SUITE


•   HTTPS :// DEVOPEDIA . ORG / OWASP -ZAP


•   HTTPS :// SEKURAK .PL/ WPROWADZENIE -DO-NARZEDZIA -ZED -ATTACK -PROXY -ZAP /


•   HTTPS :// WWW .DROPTICA .PL/ BLOG / OWASP -ZAP -OPIS -NARZEDZIA -GLOWNE -FUNKCJONALNOSCI -I -PRZYDATNE -
    ZRODLA -WIEDZY /


•   HTTPS :// SSL24.PL/ BAZA -WIEDZY/ INFORMACJE -OGOLNE /583,5-SPOSOBOW -NA -OCHRONE -PRZED -ATAKAMI -SQL-
    INJECTION


•   HTTPS :// POWERDMARC .COM /PL/ SQL-INJECTION -PREVENTION /


•   HTTPS :// IQHOST .PL/ BLOG/ JAK -ZABEZPIECZYC -SWOJA -STRONE -INTERNETOWA -PRZED -ATAKAMI -SQL-INJECTION /


•   HTTPS :// ACADEMY .BINANCE .COM / PL/ARTICLES / SYMMETRIC -VS - ASYMMETRIC -ENCRYPTION


•   HTTPS :// CYBERWIEDZA .PL/KRYPTOGRAFIA -KLUCZA -SYMETRYCZNEGO /


•   HTTPS :// WWW .SLAWOP .NET/ BLOG / SZYFROWANIESYMETRYCZNEANIESYMETRYCZNE


•   HTTPS :// WWW .UNICARD .PL/ NEWS /89/56/C O -TO -JEST -KRYPTOGRAFIA -DEFINICJA -I -KLUCZOWE -
    FUNKCJONALNOSCI


•   HTTP :// II .UWB .EDU .PL/ RYBNIK /BDI SI/BD I SI%20W5. PDF


•   HTTPS :// WWW .LH.PL/ POMOC/ TLS /


•   HTTPS :// INSTYTUTCYBER .PL/ARTYKULY / JAK -DZIALA -TLS -I -SSL/


•   HTTPS :// HARBINGERS .IO/ DEFINICJE / TLS


•   HTTPS :// ITBIZNES .PL/BEZPIECZENSTWO / ABB -RANSOMWARE -BLACK -BASTA /


•   HTTPS :// KAPITANHACK .PL/2022/06/27/ NIESKATEGORYZOWANE / UWAGA -NA -RANSOMWARE -OD-BLACK -BASTA/


•   HTTPS :// EN.WIKIPEDIA .ORG /WIKI /SPY EYE


•   HTTPS :// EN.WIKIPEDIA .ORG /WIKI /Z EUS _( MALWARE )


•   HTTPS :// WWW .YOUTUBE .COM/WATCH?V =F 8LN Z6G E_20 - M EMZ .EXE | WINDOWS TROJAN DEMONSTRATION


---


•   HTTPS :// EN.WIKIPEDIA .ORG /WIKI /MEMZ


•   HTTPS :// EN.WIKIPEDIA .ORG /WIKI /M ELISSA _( COMPUTER _VIRUS)


•   HTTPS :// PL.WIKIPEDIA .ORG /WIKI /Z ERO-DAY _EXPLOIT


•   HTTPS :// WWW .COMPUTERWORLD .PL/ NEWS /LUKA -Z ENBLEED -W -AMD-POZWALA -HAKEROM -WYKRADAC-DANE -
    Z-PROCESOROW -R YZEN ,446175. HTML


•   HTTPS :// WWW .BENCHMARK .PL/AKTUALNOSCI / LUKA -BEZPIECZENSTWA -DOWNFALL-W -PROCESORACH -INTEL-
    POPRAWKA -OBNIZA .HTML


•   HTTPS :// EN.WIKIPEDIA .ORG /WIKI /JOSHUA _SCHULTE


•   HTTPS :// EN.WIKIPEDIA .ORG /WIKI /VAULT_7


•   HTTPS :// EN.WIKIPEDIA .ORG /WIKI /WIKI LEAKS


•   HTTPS :// CERT .ORANGE .PL/ AKTUALNOSCI / REMCOS -POWRACA -ANALIZA -TECHNICZNA /


•   https://kapitanhack.pl/2022/10/17/nieskategoryzowane/malware-samorozprzestrzeniajacy-sie-
    na-youtube/




    SKŁAD OSÓB ZAANGAŻOWANYCH W REALIZACJI PROJEKTU :

                 - KRZYSZTOF PIETRUCHA (PUNKT 1)
                  - ANDRZEJ KOZŁOWSKI (PUNKT 3)
                    - KACPER MAJCHER (PUNKT 2)
                 - MICHAŁ WŁODARCZYK (PUNKT 4)


---


