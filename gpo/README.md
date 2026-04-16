\# GPO: Blokada Panelu sterowania z filtrem WMI (Windows Server 2019)



\## Cel projektu

Celem projektu jest wdrożenie GPO blokującego dostęp do Panelu sterowania oraz ograniczenie jego działania tylko do komputerów z systemem Windows 10 przy użyciu filtra WMI. Komputer z Windows 7 służy jako system wykluczony z działania polityki.



\## Środowisko

\- Windows Server 2019 (kontroler domeny)

\- Active Directory Domain Services

\- Windows 10 (klient docelowy)

\- Windows 7 (klient wykluczony)



\## Konfiguracja GPO

Nazwa GPO:

GPO\_Block\_ControlPanel



Lokalizacja:

User Configuration → Administrative Templates → Control Panel



Ustawienie:

Prohibit access to Control Panel and PC settings = Enabled



\## Filtr WMI

WMI filter:

SELECT \* FROM Win32\_OperatingSystem WHERE Caption LIKE "%Windows 10%"





