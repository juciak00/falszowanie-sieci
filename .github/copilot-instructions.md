# Instrukcje projektu (always-on)

Ten plik zawiera stałe zasady pracy Copilota dla tego repozytorium.

## Temat i zakres
- Główny temat projektu: **12. Atak na OSPF - Fałszowanie tras (OSPF Route Injection)**.
- Wszystkie propozycje, konfiguracje, scenariusze testów i dokumentacja mają być zgodne z tym tematem.

## Źródła wzorcowe
- W folderze `examples/` znajdują się przykładowe projekty.
- Traktuj materiały z `examples/` jako wzorce struktury, stylu i sposobu prezentacji wyników.
- Nie kopiuj bezrefleksyjnie; dopasuj treść do topologii i założeń tego projektu.

## Zasady aktualizacji dokumentacji
- Główny plik czystopisu: `sprawko.md`.
- Wszystkie merytoryczne wyniki końcowe i treść raportowa zapisuj w `sprawko.md`.
- Dziennik kontekstu i postępu prowadź osobno w `dziennik-postepu.md`.
- Nie usuwaj istniejących sekcji bez wyraźnej potrzeby; preferuj dopisywanie i porządkowanie.

## Obowiązkowy dziennik kontekstu i postępu
- Utrzymuj współdzielony dziennik pracy zespołowej w `dziennik-postepu.md`.
- Po każdym istotnym kroku dopisz krótką aktualizację zawierającą:
  - datę,
  - co zostało zrobione,
  - jakie pliki/artefakty powstały,
  - co jest następnym krokiem.
- Zapis powinien być krótki, konkretny i możliwy do szybkiego przeczytania przez inną osobę.

## Sposób pracy
- Pracuj etapowo zgodnie z wymaganiami z `context.txt` (atak -> zabezpieczenie -> retest).
- Priorytet: poprawność techniczna, powtarzalność kroków, czytelne dowody (komendy, logi, zrzuty, wyniki).
- Każda większa zmiana w projekcie powinna kończyć się aktualizacją `dziennik-postepu.md` i, jeśli dotyczy treści raportowej, także `sprawko.md`.