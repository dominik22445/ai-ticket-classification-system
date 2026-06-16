# AI Ticket Classification System

## Opis projektu

System wykorzystujący sztuczną inteligencję do automatycznej analizy i klasyfikacji wiadomości klientów oraz kierowania ich do odpowiednich procesów biznesowych.

Projekt wykorzystuje model OpenAI do rozpoznawania rodzaju zgłoszenia, zapisuje wyniki w Google Sheets oraz uruchamia odpowiednie działania w zależności od kategorii wiadomości.

---

## Problem biznesowy

Ręczna analiza każdej wiadomości klienta jest czasochłonna i utrudnia szybkie reagowanie na ważne zgłoszenia.

Projekt automatyzuje proces klasyfikacji wiadomości oraz kieruje je do odpowiednich ścieżek obsługi, dzięki czemu możliwe jest szybsze przetwarzanie zgłoszeń i lepsze zarządzanie priorytetami.

---

## Technologie

* Make
* OpenAI API
* Gmail
* Google Sheets
* JSON

---

## Architektura rozwiązania

Klient → Gmail → OpenAI API → JSON → Router

### Kategorie zgłoszeń

* Reklamacja
* Klient wysokowartościowy
* Nowa wycena
* Pytanie ogólne
* Zmiana rezerwacji

### Dalszy przepływ

Router → Google Sheets → Powiadomienie e-mail → Odpowiedni proces obsługi

---

## Funkcje

* automatyczna analiza treści wiadomości,
* klasyfikacja zgłoszeń do odpowiednich kategorii,
* wykorzystanie AI do podejmowania decyzji biznesowych,
* automatyczny routing wiadomości,
* zapis zgłoszeń w Google Sheets,
* automatyczne powiadamianie odpowiednich osób,
* obsługa wielu ścieżek procesowych,
* ograniczenie ręcznej pracy związanej z segregacją zgłoszeń.

---

## Przykładowe kategorie

### Reklamacja

Wiadomości dotyczące problemów z usługą lub zgłoszeń reklamacyjnych.

### Wysokowartościowy lead

Zapytania od klientów o dużym potencjale biznesowym wymagające szybkiej reakcji.

### Nowa wycena

Wiadomości zawierające prośbę o przygotowanie oferty lub wyceny.

### Pytanie ogólne

Standardowe pytania dotyczące usług lub działania firmy.

### Zmiana rezerwacji

Prośby o zmianę wcześniej ustalonych terminów lub parametrów usługi.

---

## Przykładowy wynik klasyfikacji

```json
{
  "kategoria": "NOWA_WYCENA",
  "priorytet": "ŚREDNI"
}
```

---

## Ograniczenia projektu

* klasyfikacja zależy od jakości wiadomości klienta,
* błędnie sformułowane wiadomości mogą zostać przypisane do niewłaściwej kategorii,
* skuteczność działania zależy od jakości promptu i zdefiniowanych kategorii,
* projekt nie analizuje załączników.

---

## Czego nauczyłem się podczas realizacji projektu

* projektowania procesów biznesowych wspieranych przez AI,
* wykorzystania OpenAI API do klasyfikacji danych,
* pracy z formatem JSON,
* tworzenia zaawansowanych workflow w Make,
* budowy systemów routingowych opartych o AI,
* integracji Gmail, OpenAI i Google Sheets,
* automatyzacji procesów obsługi klienta.
