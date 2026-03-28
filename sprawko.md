# Projekt zaliczeniowy

## 12. Atak na OSPF - Fałszowanie tras (OSPF Route Injection)

### Kierunek: Bezpieczeństwo sieci

### Autorzy
- Karol Ziobro
- Julia Jarząb

### Data
2026-03-28

---

## Spis treści

1. [Wstęp i cel projektu](#sec-1)
2. [Topologia i środowisko](#sec-2)
3. [Adresacja i role urządzeń](#sec-3)
4. [Scenariusz ataku: OSPF Route Injection](#sec-4)
5. [Wdrożone zabezpieczenia OSPF](#sec-5)
6. [Re-test po wdrożeniu zabezpieczeń](#sec-6)
7. [Dowody i wyniki testów](#sec-7)
8. [Wnioski i rekomendacje](#sec-8)
9. [Załączniki](#sec-9)

---

<a id="sec-1"></a>
## 1. Wstęp i cel projektu

Protokół OSPF (Open Shortest Path First) jest jednym z najczęściej stosowanych protokołów routingu wewnętrznego (IGP) w sieciach przedsiębiorstw. Działa dynamicznie, szybko reaguje na zmiany topologii i na podstawie metryk wybiera najkorzystniejsze trasy pomiędzy segmentami sieci. Z tego względu integralność informacji wymienianych pomiędzy sąsiadami OSPF ma kluczowe znaczenie dla stabilności i bezpieczeństwa całej infrastruktury.

W praktyce, jeżeli domena OSPF nie jest odpowiednio zabezpieczona, możliwe staje się dołączenie nieautoryzowanego urządzenia i wprowadzenie do procesu routingu fałszywych informacji o trasach. Taki scenariusz, określany jako **OSPF Route Injection**, może doprowadzić do nieprawidłowego przekierowania ruchu, utworzenia trasy typu blackhole, podsłuchu transmisji (man-in-the-middle) lub czasowej niedostępności usług. Skutki takiego ataku mogą objąć zarówno pojedynczy segment, jak i większą część sieci, zależnie od miejsca wstrzyknięcia oraz zaufania pomiędzy routerami.

Niniejszy projekt ma charakter praktyczny i laboratoryjny. Jego celem nie jest wyłącznie opis teoretyczny zagrożenia, ale przede wszystkim przeprowadzenie pełnego cyklu testowego: od poprawnie działającej sieci bazowej, przez kontrolowany atak, aż po wdrożenie zabezpieczenia i weryfikację jego skuteczności. Podejście to pozwala ocenić zarówno podatność środowiska, jak i realny efekt zastosowanych mechanizmów ochronnych.

Cele szczegółowe projektu:
1. Przygotowanie topologii testowej z wykorzystaniem routingu OSPF oraz zdefiniowanie ról urządzeń (routery legalne, hosty końcowe, węzeł atakujący).
2. Udokumentowanie stanu początkowego sieci, w tym poprawnej wymiany tras i osiągalności hostów.
3. Realizacja ataku Route Injection poprzez wprowadzenie fałszywej informacji routingu i obserwacja zmian w tablicach routingu.
4. Zebranie dowodów technicznych (komendy diagnostyczne, zrzuty konfiguracji, wyniki testów łączności) potwierdzających wpływ ataku.
5. Wdrożenie mechanizmu ochronnego w OSPF (uwierzytelnianie sąsiedztwa) oraz ponowne uruchomienie testu ataku.
6. Porównanie wyników przed i po zabezpieczeniu, wraz z oceną skuteczności i ograniczeń zastosowanej ochrony.

Zakres pracy obejmuje wyłącznie środowisko kontrolowane, przygotowane na potrzeby ćwiczenia akademickiego. Wszystkie działania są wykonywane w celu demonstracji ryzyk bezpieczeństwa i opracowania dobrych praktyk obronnych, a nie do zastosowań poza laboratorium.

Efektem końcowym projektu jest spójna dokumentacja techniczna zawierająca opis topologii, konfiguracji, przebiegu ataku, metod zabezpieczenia oraz wyników re-testu. Dokumentacja ta stanowi podstawę do sformułowania praktycznych wniosków i rekomendacji dotyczących ochrony protokołu OSPF przed fałszowaniem tras.

<a id="sec-2"></a>
## 2. Topologia i środowisko

_Sekcja do uzupełnienia._

<a id="sec-3"></a>
## 3. Adresacja i role urządzeń

_Sekcja do uzupełnienia._

<a id="sec-4"></a>
## 4. Scenariusz ataku: OSPF Route Injection

_Sekcja do uzupełnienia._

<a id="sec-5"></a>
## 5. Wdrożone zabezpieczenia OSPF

_Sekcja do uzupełnienia._

<a id="sec-6"></a>
## 6. Re-test po wdrożeniu zabezpieczeń

_Sekcja do uzupełnienia._

<a id="sec-7"></a>
## 7. Dowody i wyniki testów

_Sekcja do uzupełnienia._

<a id="sec-8"></a>
## 8. Wnioski i rekomendacje

_Sekcja do uzupełnienia._

<a id="sec-9"></a>
## 9. Załączniki

_Sekcja do uzupełnienia._
