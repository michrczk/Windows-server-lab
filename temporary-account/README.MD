\# Temporary Profile w Active Directory



\## Opis

Projekt pokazuje problem profilu tymczasowego użytkownika w domenie Windows oraz jego naprawę.



\## Środowisko

\- Windows Server 2019 (Active Directory)

\- Windows 7/10 (klient)

\- VirtualBox



\## Problem

Użytkownik loguje się do domeny i otrzymuje profil tymczasowy. Zmiany nie są zapisywane.



\## Przyczyna

\- uszkodzony lub usunięty profil w C:\\Users

\- błędny wpis SID w rejestrze ProfileList



\## Rozwiązanie

\- usunięcie profilu użytkownika

\- usunięcie wpisu SID z rejestru

\- ponowne logowanie użytkownika



\## Wniosek

Problem wynika z braku poprawnego mapowania profilu użytkownika do SID.

