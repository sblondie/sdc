---
id: cykl-zycia-strony-internetowej
title: Cykl życia serwisu internetowego (TIK). Ramowe wytyczne
sidebar_label: Cykl życia serwisu
sidebar_position: 4 
keywords: [dostepnosc cyfrowa, cykl życia]
tags: [dostepnosc cyfrowa, cykl życia]
data_zgloszenia: 6 października 2025 r.
ostatnia_aktualizacja: 19 grudzień 2025 r.
opracowanie: Dawid Górny
wersja_robocza: true
---

## 1. Cel dokumentu

Celem dokumentu jest przedstawienie minimalnych zasad, według których instytucja publiczna powinna planować, zamawiać, tworzyć, testować, utrzymywać i wycofywać serwis w sposób dostępny cyfrowo. Treść ma charakter ramowy i powinna zostać uzupełniona o procedury wewnętrzne właściwe dla danej jednostki.

## 2. Podstawy prawne i standardy

* Ustawa z dnia 4 kwietnia 2019 r. o dostępności cyfrowej stron internetowych i aplikacji mobilnych podmiotów publicznych.
* Standard WCAG 2.1 / 2.2 na poziomie AA.
* Norma EN 301 549 V3.2.1 oraz standard PDF/UA (ISO 14289).
* Standard HTML (Living Standard) – w zakresie semantycznego kodu strukturalnego.
* Standard prostego języka (Plain Language).

## 3. Role i odpowiedzialność

Poniższy wykaz ról ma charakter porządkowy. W różnych projektach lub instytucjach role te mogą być nazwane inaczej lub łączone, zależnie od struktury organizacyjnej jednostki.

### 3.1 Opis ról

* **Dostępnościowiec** – definiuje wytyczne, uczestniczy w wyborze wykonawców, zleca audyty i rozpatruje skargi dotyczące dostępności.
* **Administrator** – zarządza infrastrukturą i CMS. Odpowiada za repozytorium kodu, konfigurację techniczną oraz procesy CI/CD.
* **Projektant** – tworzy makiety i style wizualne zgodnie z zasadami projektowania uniwersalnego.
* **Programista** – implementuje semantyczny kod HTML, CSS i JS oraz stosuje atrybuty ARIA.
* **Tester** – weryfikuje zgodność rozwiązań z WCAG i ustawą za pomocą walidatorów oraz technologii asystujących.
* **Redaktor** – publikuje treści dostępne cyfrowo (nagłówki, opisy alternatywne, prosty język).
* **Wykonawca** – podmiot zewnętrzny dostarczający komponenty systemu lub przeprowadzający audyty końcowe.

### 3.2 Matryca RACI

Poniższa tabela przedstawia podział odpowiedzialności w procesie zapewniania dostępności cyfrowej. Skupia się ona na kluczowych działaniach krytycznych dla zachowania standardów WCAG i wymogów ustawowych.

**Tabela 1. Przypisanie odpowiedzialności w procesie zapewniania dostępności cyfrowej serwisu.**

| Faza cyklu życia | Dostępnościowiec | Administrator | Projektant | Programista | Tester | Redaktor | Wykonawca |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 1. Koncepcja i wymagania | A | R | C | I | | C | C |
| 2. Projektowanie | C | I | R | C | | | C |
| 3. Wykonanie i kodowanie | C | A | I | R | | | R |
| 4. Testowanie i walidacja | A | I | | R | R | I | C |
| 5. Publikacja i deklaracja | C | A | I | | C | R | I |
| 6. Utrzymanie i rozwój | A | R | | | C | R | |
| 7. Starzenie i wycofanie | A | R | | | | R | |

**Legenda oznaczeń RACI:**
* R (Realizuje / Responsible) – wykonuje zadanie.
* A (Akceptuje / Accountable) – odpowiada za zadanie i zatwierdza efekt końcowy.
* C (Konsultuje / Consulted) – doradza i opiniuje przed podjęciem decyzji.
* I (Informowany / Informed) – otrzymuje kluczowe informacje o wynikach.

## 4. Cykl życia serwisu

### Faza 1 - Koncepcja i definiowanie wymagań
* Zespół wpisuje wymagania WCAG i normę EN 301 549 do opisu zamówienia (SIWZ/OPZ).
* **Dostępnościowiec** i **Administrator** sprawdzają, czy silnik serwisu (CMS) pozwala na pełną dostępność treści.
* Kierownik projektu ustala matrycę RACI oraz planuje budżet na szkolenia i audyty.

### Faza 2 - Projektowanie
* **Projektant** tworzy makiety serwisu zgodnie z zasadami projektowania uniwersalnego.
* **Dostępnościowiec** lub **Wykonawca** ocenia makiety pod kątem WCAG przed rozpoczęciem prac programistycznych.
* **Projektant** przygotowuje wytyczne dla programistów dotyczące nawigacji klawiaturą i etykiet pól.

### Faza 3 - Wykonanie (kodowanie i integracja CMS)
* **Programista** buduje semantyczny kod HTML, a **Administrator** wdraża automatyczne testy dostępności w procesie CI/CD.
* **Redaktor** wprowadza do systemu treści testowe w celu sprawdzenia poprawności szablonów.
* **Administrator** sprawdza, czy system CMS nie generuje błędnego kodu podczas publikacji treści.

### Faza 4 - Testowanie i walidacja
* **Tester** wykonuje audyt techniczny kodu oraz testuje serwis za pomocą technologii asystujących.
* Zespół opcjonalnie przeprowadza testy użyteczności z udziałem osób z niepełnosprawnościami.
* **Programista** naprawia zgłoszone błędy, a **Tester** potwierdza ich skuteczne usunięcie.

### Faza 5 - Publikacja i deklaracja
* **Administrator** przenosi gotowy serwis na serwer produkcyjny.
* **Dostępnościowiec** przygotowuje i zamieszcza w serwisie Deklarację Dostępności.
* **Administrator** lub **Wykonawca** uruchamia system stałego monitoringu automatycznego.

### Faza 6 - Utrzymanie i rozwój
* **Redaktor** dba o to, aby każda nowa treść oraz każdy załącznik (PDF/UA) spełniały zasady dostępności.
* **Tester** sprawdza każdą nową funkcjonalność pod kątem regresji dostępności.
* **Dostępnościowiec** aktualizuje Deklarację Dostępności po każdej zmianie oraz po corocznym przeglądzie (do 31 marca).

### Faza 7 - Starzenie się i wycofanie
* **Administrator** przygotowuje dostępną wersję archiwalną serwisu (np. statyczny HTML lub plik PDF/UA).
* **Dostępnościowiec** informuje o wycofaniu serwisu w raportach dostępności i zapewnia odpowiednie przekierowania.

## 5. Szkolenia i kompetencje

* Projektanci i Programiści: Szkolenia techniczne z WCAG 2.1/2.2 i semantyki kodu.
* Testerzy: Warsztaty z audytowania i obsługi czytników ekranu (NVDA, Jaws).
* Dostępnościowcy: Zarządzanie dostępnością w organizacji i interpretacja norm prawnych.
* Redaktorzy i Administratorzy CMS: Tworzenie dostępnych treści i zasady prostego języka.

## 6. Monitorowanie dostępności

Monitoring automatyczny jest konfigurowany przez **Administratora**. Raporty są okresowo analizowane przez **Dostępnościowca**, który inicjuje działania naprawcze w przypadku wykrycia błędów w publikowanych treściach lub kodzie.

## 7. Planowane dokumenty pomocnicze

* Lista kontrolna Dostępnościowca dla każdej fazy.
* Wzór klauzuli dostępności do umów z Wykonawcą.
* Procedura zgłaszania barier i reagowania na regresję dostępności.

## 8. Słownik pojęć

* **ARIA** – atrybuty dla technologii asystujących (np. czytników ekranu).
* **CI/CD** – zautomatyzowane procesy budowania i testowania zmian w serwisie.
* **CMS** – system zarządzania treścią serwisu.
* **Deklaracja Dostępności** – dokument opisujący stan dostępności i dane kontaktowe.
* **HTML** – język znaczników używany do tworzenia struktury stron; semantyczny HTML jest kluczowy dla dostępności.
* **Projektowanie uniwersalne** – projektowanie produktów użytecznych dla każdego bez potrzeby adaptacji.
* **Regresja** – ponowne pojawienie się błędów po wprowadzeniu zmian w systemie.
* **Semantyczny HTML** – kod używający znaczników zgodnie z ich funkcją.
* **Serwis** – strona internetowa podmiotu publicznego, BIP lub aplikacja webowa realizująca zadania publiczne.
* **PDF/UA** – standard tworzenia dostępnych plików PDF (ISO 14289).
