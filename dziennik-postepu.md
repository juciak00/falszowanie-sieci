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
