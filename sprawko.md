# Projekt: OSPF Route Injection

## Pomysł na projekt
**Atak na OSPF – Fałszowanie tras (OSPF Route Injection)**

---

## Cel projektu
Celem projektu jest pokazanie, jak atakujący może wstrzyknąć fałszywe informacje routingu do protokołu OSPF, powodując zmianę tras w sieci, a następnie wdrożenie zabezpieczenia w postaci uwierzytelniania OSPF, które blokuje taki atak.

---

## 1. Środowisko

**Symulacja:**
- Cisco Packet Tracer

**Urządzenia:**
- 3 routery
- 2 hosty PC
- 1 router atakujący

---

## 2. Topologia
PC1 ----- R1 ----- R2 ----- R3 ----- PC2
|
R-ATTACK

**Opis urządzeń:**

| Urządzenie | Rola |
|-----------|------|
| PC1 | host w sieci 1 |
| PC2 | host w sieci 2 |
| R1 | router brzegowy |
| R2 | router centralny |
| R3 | router brzegowy |
| R-ATTACK | router atakujący |

---

## 3. Adresacja

| Sieć | Adres |
|------|------|
| PC1 LAN | 192.168.1.0/24 |
| PC2 LAN | 192.168.2.0/24 |
| R1-R2 | 10.0.12.0/30 |
| R2-R3 | 10.0.23.0/30 |
| R2-Attack | 10.0.24.0/30 |

**Routery:**

| Router | IP |
|--------|----|
| R1 | 10.0.12.1 |
| R2 | 10.0.12.2 |
| R3 | 10.0.23.2 |
| Attack | 10.0.24.2 |

---

## 4. Normalna konfiguracja OSPF

```bash
router ospf 1
network 10.0.0.0 0.0.255.255 area 0
network 192.168.1.0 0.0.0.255 area 0

Test:
PC1 -> ping -> PC2
show ip route

5. Scenariusz ataku (Route Injection)

Atakujący router:

Dołącza do OSPF

Rozgłasza fałszywą sieć

5. Scenariusz ataku (Route Injection)

Atakujący router:

Dołącza do OSPF

Rozgłasza fałszywą sieć

router ospf 1
network 10.0.24.0 0.0.0.3 area 0
redistribute connected

interface loopback0
ip address 192.168.2.1 255.255.255.0

Efekt:

Routery uznają, że atakujący ma lepszą trasę do sieci PC2

Skutek ataku

Ruch przechodzi przez R-ATTACK, który może:

przechwycić ruch

zablokować ruch

zmienić routing

6. Dowody ataku

Komendy:
show ip ospf neighbor
show ip route
show ip ospf database

Do pokazania:

tablica routingu przed atakiem

tablica routingu po ataku

zmiana next-hop

7. Zabezpieczenie

OSPF MD5 Authentication

interface g0/0
ip ospf message-digest-key 1 md5 cisco123

router ospf 1
area 0 authentication message-digest

Efekt:
Router przyjmuje tylko pakiety z poprawnym hasłem

Atakujący nie może się podłączyć

8. Powtórzenie ataku

Efekt:

brak sąsiedztwa OSPF

brak fałszywych tras

Sprawdzenie:

show ip ospf neighbor
9. Wynik projektu
Etap	Efekt
przed atakiem	normalny routing
atak	fałszywa trasa OSPF
po zabezpieczeniu	router atakujący odrzucony
10. Artefakty do dokumentacji

Screenshots:

topologia

konfiguracja routerów

show ip route

show ip ospf neighbor

wynik ping

brak sąsiedztwa po zabezpieczeniu

11. Bonus (opcjonalnie)

zmiana metric / cost w ataku

pokazanie blackhole routing

analiza pakietów w Simulation Mode (Packet Tracer)

12. Gotowy opis (Etap 1)

Temat:
Atak na protokół OSPF – fałszowanie tras (OSPF Route Injection)

Środowisko:
Cisco Packet Tracer

Opis:
Projekt polega na zaprojektowaniu topologii sieci wykorzystującej protokół routingu OSPF. W pierwszej części zostanie przeprowadzony atak polegający na wstrzyknięciu fałszywych informacji routingu przez złośliwy router. Następnie zostanie wdrożone zabezpieczenie w postaci autoryzacji OSPF (MD5), które ma uniemożliwić przyłączenie się nieautoryzowanego urządzenia do domeny routingu. Na końcu atak zostanie powtórzony w celu potwierdzenia skuteczności zabezpieczenia.
