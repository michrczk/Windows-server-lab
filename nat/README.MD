\# Windows Server 2019 NAT (RRAS) – Lab + Troubleshooting



\## Cel

Konfiguracja Windows Server 2019 jako routera NAT oraz diagnostyka problemów sieciowych w VirtualBox.



\## Środowisko

\- Windows Server 2019 (RRAS, NAT)

\- Windows 7 Client (Internal Network)

\- Windows 10 Client (Internal Network)

\- Sieć LAN: 192.168.1.0/24



\## Konfiguracja

\- Server LAN: 192.168.1.1/24

\- NAT (RRAS) aktywny

\- WAN: VirtualBox NAT

\- LAN interface ustawiony jako private NAT



\## Problem

Brak internetu na kliencie mimo połączenia z serwerem LAN.



Objawy:

\- ping 8.8.8.8 fail / loss

\- brak DNS

\- ping do 192.168.1.1 działa



\## Przyczyna

Błędna brama domyślna na kliencie:

\- 192.168.0.1 (błędna)

\- 192.168.1.1 (poprawna)

Błędna konfiguracja translatora adresów sieciowych



\## Rozwiązanie

\- korekta gateway na kliencie

\- zmiana prywatnego interfejsu na publiczny

\- ipconfig /release /renew

\- test łączności (ping, DNS)



\## Wynik

Przywrócono pełną łączność internetową przez NAT.



\## Wniosek

Nieprawidłowa brama domyślna blokuje ruch do NAT mimo poprawnej konfiguracji serwera.

