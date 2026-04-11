# Dziennik kontekstu i postepu

## 2026-03-28

### Co zostalo zrobione
- Potwierdzono temat projektu: 12. Atak na OSPF - Falszowanie tras (OSPF Route Injection).
- Ustalono sposob pracy: atak -> zabezpieczenie -> retest, zgodnie z wymaganiami z context.txt.
- Wykonano konwersje PDF -> MD:
  - Przejmowanie kontroli nad systemem ofiary.pdf -> Przejmowanie kontroli nad systemem ofiary.md
  - SSL_i_TLS_-_omowienie_pod_katem_bezpieczenstwa.pdf -> SSL_i_TLS_-_omowienie_pod_katem_bezpieczenstwa.md
- Dodano stale instrukcje repozytorium dla Copilota.

### Pliki i artefakty
- .github/copilot-instructions.md
- sprawko.md
- Przejmowanie kontroli nad systemem ofiary.md
- SSL_i_TLS_-_omowienie_pod_katem_bezpieczenstwa.md

### Nastepny krok
- Uporzadkowac sprawko.md do finalnej struktury Etapu 2 i Etapu 3: topologia, adresacja, scenariusz ataku, scenariusz zabezpieczenia, retest, dowody i wnioski.

---

## 2026-03-28 (aktualizacja 2)

### Co zostalo zrobione
- Przygotowano nowy czystopis w sprawko.md od zera.
- Dodano strone tytulowa z autorami: Karol Ziobro, Julia Jarzab.
- Dodano spis tresci z hiperlinkami do sekcji raportu.

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Uzupelnic tresc sekcji 1-9 na podstawie rzeczywistej topologii, konfiguracji i wynikow testow.

---

## 2026-03-28 (aktualizacja 3)

### Co zostalo zrobione
- Uzupelniono sekcje "Wstep i cel projektu" w czystopisie.
- Pozostale sekcje raportu pozostawiono bez zmian, zgodnie z ustaleniem "na razie tylko wstep i cel".

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Przygotowac sekcje 2 (Topologia i srodowisko) po potwierdzeniu finalnego ukladu sieci i ról urzadzen.

---

## 2026-04-11

### Co zostalo zrobione
- Zweryfikowano stan bazowy (przed atakiem) sieci OSPF:
  - R1, R2, R3 widzą nawzajem sąsiadów OSPF w stanie FULL.
  - Brak sąsiada R-ATTACK na R2 (jest on jeszcze wył.).
  - Brak trasy do 172.16.200.0/24 na routerach legalnych.
  - Test ping PC1 → PC2 działa prawidłowo.
- Dodano screeny stanu przed atakiem do sekcji 4.2 (Stan bazowy):
  - R1_before.png
  - R2_before.png
  - R3_before.png
  - PC1_ping.png

### Pliki i artefakty
- resources/R1_before.png, resources/R2_before.png, resources/R3_before.png, resources/PC1_ping.png
- sprawko.md (aktualizacja sekcji 4.2)

### Nastepny krok
- Wykonac atak OSPF Route Injection (uruchomić OSPF na R-ATTACK).
- Zebrać screeny ze stanu ataku.
- Dodać je do sekcji 4.4 ("Oczekiwany efekt ataku").

---

## 2026-04-11 (aktualizacja 2)

### Co zostalo zrobione
- Dodano screeny stanu po zabezpieczeniu do sekcji 6.2 w sprawko.md:
  - R2_secured.png
  - R1_secured.png
  - R3_secured.png
  - PC1_ping_secured.png

### Pliki i artefakty
- resources/R2_secured.png, resources/R1_secured.png, resources/R3_secured.png, resources/PC1_ping_secured.png
- sprawko.md (aktualizacja sekcji 6.2)

### Nastepny krok
- Dokończyć weryfikację re-testu i, jeśli wynik jest zgodny, uzupełnić sekcję 7 o finalne zestawienie dowodów.

---

## 2026-04-11 (aktualizacja 3)

### Co zostalo zrobione
- Dodano obszerne podsumowanie końcowe do sekcji 8 w sprawko.md.
- Podsumowanie obejmuje pełny cykl: stan bazowy, atak, skutki route injection, zabezpieczenie MD5/passive-interface oraz wynik re-testu.

### Pliki i artefakty
- sprawko.md (aktualizacja sekcji 8)

### Nastepny krok
- Jeśli trzeba, dopracować jeszcze styl końcówki raportu lub przygotować wersję pod eksport do PDF.

---

## 2026-03-28 (aktualizacja 4)

### Co zostalo zrobione
- Rozszerzono sekcje "Wstep i cel projektu" o szerszy kontekst techniczny OSPF.
- Dodano cele szczegolowe projektu, zakres pracy laboratoryjnej i oczekiwany efekt koncowy dokumentacji.

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Przejsc do sekcji 2 i opisac finalna topologie oraz srodowisko testowe.

---

## 2026-03-28 (aktualizacja 5)

### Co zostalo zrobione
- Dalsze rozszerzenie sekcji "Wstep i cel projektu" o teorie OSPF.
- Dodano opis: LSDB, algorytm SPF (Dijkstry), rodzaj wplywu LSA, stany sasiedztwa OSPF oraz ryzyka przy braku granic zaufania.
- Uzupelniono czesc metodologiczna o kryteria potwierdzania skutecznego route injection (routing, sasiedztwo, LSDB, testy lacznosci).

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Uzupelnic sekcje 2: topologia, urzadzenia, role i zalozenia srodowiska laboratoryjnego.

---

## 2026-03-28 (aktualizacja 6)

### Co zostalo zrobione
- Uzgodniono wariant realizacji: GNS3/EVE-NG + FRRouting (routery Linux) na dwoch komputerach.
- Rozpisano szczegolowo punkt 2 w czystopisie, w tym: uzasadnienie wyboru, model topologii, podzial rol miedzy komputerami, komponenty, wymagania sprzetowe/programowe, zalozenia operacyjne i ograniczenia.

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Uzupelnic sekcje 3 (Adresacja i role urzadzen) zgodnie z topologia i wybranym wariantem laboratoryjnym.

---

## 2026-03-28 (aktualizacja 7)

### Co zostalo zrobione
- Dodano diagramy Mermaid do sekcji 2 w czystopisie.
- Wstawiono trzy wizualizacje: podzial rol na dwa komputery, topologie logiczna OSPF oraz przeplyw etapow eksperymentu.

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Uzupelnic sekcje 3 (adresacja i mapa interfejsow) w formie tabeli technicznej.

---

## 2026-03-28 (aktualizacja 8)

### Co zostalo zrobione
- Rozszerzono punkt 2 do wiekszej objetosci i szczegolowosci (porownywalnej z przykladami).
- Dodano podsekcje: architektura FRRouting, plan uruchomienia i walidacji, kryteria jakosci i powtarzalnosci, scenariusze bledow srodowiskowych.

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Uzupelnic sekcje 3 o konkretna tabele adresacji i przypisanie interfejsow do R1, R2, R3, R-ATTACK, PC1 i PC2.

---

## 2026-03-28 (aktualizacja 9)

### Co zostalo zrobione
- Uzupelniono sekcje 3 (Adresacja i role urzadzen) w czystopisie.
- Dodano: tabele podsieci, mape interfejsow routerow, konfiguracje hostow, role urzadzen, parametry OSPF powiazane z adresacja oraz diagram Mermaid adresacji.

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Uzupelnic sekcje 4: scenariusz ataku OSPF Route Injection krok po kroku (stan bazowy, wykonanie, obserwacje, kryteria sukcesu).

---

## 2026-03-28 (aktualizacja 10)

### Co zostalo zrobione
- Uzupelniono sekcje 4 (Scenariusz ataku: OSPF Route Injection).
- Dodano: warunki wejsciowe, kroki realizacji ataku, szkielet konfiguracji FRR, oczekiwane artefakty, kryteria sukcesu/niepowodzenia oraz diagram Mermaid (sequence diagram).

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Uzupelnic sekcje 5 (Wdrozone zabezpieczenia OSPF) i opisac konfiguracje ochronna przed route injection.

---

## 2026-04-10

### Co zostalo zrobione
- Zmieniono wariant realizacji projektu z GNS3/EVE-NG + FRR na uproszczony scenariusz w Cisco Packet Tracer.
- Przepisano sekcje techniczne w sprawko.md pod Packet Tracer i Cisco IOS: topologia, adresacja, scenariusz ataku, zabezpieczenie i re-test.
- Uzupelniono dotychczas puste sekcje 5-9 (zabezpieczenia, re-test, wyniki, wnioski, zalaczniki).

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Przygotowac plik .pkt zgodny z opisem oraz uzupelnic raport o rzeczywiste zrzuty komend z Packet Tracer.

---

## 2026-04-10 (aktualizacja 2)

### Co zostalo zrobione
- Dodano do sprawko.md gotowe konfiguracje IOS 1:1 do wklejenia dla R1, R2, R3 i R-ATTACK (wariant przed zabezpieczeniem).
- Dodano uzupelnienie konfiguracji ochronnej na R1 i R3 (MD5), aby komplet zabezpieczenia byl od razu wykonywalny.
- Dodano krotka checklistę testow krok po kroku (stan bazowy -> atak -> ochrona -> re-test).

### Pliki i artefakty
- sprawko.md

### Nastepny krok
- Wykonac scenariusz w Packet Tracer i uzupelnic sekcje 7 o realne zrzuty polecen oraz wyniki ping/tracert.

---

## 2026-04-10 (aktualizacja 3)

### Co zostalo zrobione
- Dodano do sekcji 2 w sprawko.md osadzony obraz finalnej topologii z Packet Tracer.
- Wykorzystano plik resources/topology.png jako ilustracje gotowego ukladu urzadzen i polaczen.

### Pliki i artefakty
- sprawko.md
- resources/topology.png

### Nastepny krok
- Uzupełnic sekcje 7 o kolejne dowody z etapu OSPF (sasiedztwo i trasy podczas ataku oraz po zabezpieczeniu).
