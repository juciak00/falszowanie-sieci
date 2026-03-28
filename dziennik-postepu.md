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
