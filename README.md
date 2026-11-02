# MOL — rekonstrukcja magazynu 3D (nowy projekt)

## Źródło i zasady
Źródło: jedyna strona dokumentu **PLAN MAGAYNU LOKALIZACJE.pdf** udostępnionego przez właściciela MOL. Implementacja została rozpoczęta od nowa; poprzednie HTML V2.x usunięto z aktualnej gałęzi (historia Git pozostaje).

**Kluczowe ograniczenie:** PDF nie zawiera wymiarów budowlanych, dlatego skala 3D i wysokość regałów są poglądowe. Nie należy przedstawiać modelu jako wiernej inwentaryzacji metrycznej. Również przejścia między rzędami nie są zatwierdzone jako graf tras ES.

## Audyt źródła — fragment po fragmencie
1. **Górna granica / zaplecze:** BIURO MOL, SALA KONFERENCYJNA, BIURA — CEO, MKTPL, E-COM, MARKETING, wewnętrzne przegrody; winda.
2. **Przyjęcia:** dwa pola „Stanowiska działu przyjęcia” w górnej prawej części.
3. **Pakowanie:** dziewięć osobnych stanowisk, ułożonych **3 × 3** (potwierdzenie właściciela procesu, pierwszeństwo nad nieczytelnym zrzutem PDF).
4. **Wózki kurierskie:** wydzielone żółte pole w górnej części środka.
5. **Lewy górny blok:** regały 01–10 w parach, pięć oznaczeń w szeregu, ścieżki kierunkowe.
6. **Pionowy blok 11:** numery 11-01-XX do 11-06-XX.
7. **Prawy górny i środkowy blok:** numery 12–36 z indeksami lokalizacji; strefy 1 i 2; drogi wzdłuż bloków.
8. **Blok 41:** indywidualne lokalizacje 41-01-01…41-07-04.
9. **Rząd 37:** oznaczenia 37-01-01…37-01-05 przy dolnej krawędzi socjalnej.
10. **Część socjalna:** duży wydzielony ciemny prostokąt.
11. **Lewa dolna część:** regały 50–64 (w tym 57 z sześcioma oznaczeniami, pozostałe głównie siedem).
12. **Operacyjne żółte strefy:** ZWROTY oraz MATERIAŁY - PUSTE KARTONY.
13. **Dół:** lokalizacje R1–R7 i końcowe oznaczenia strefy 4.
14. **Ściany:** zewnętrzny uskokowy obrys magazynu, górne przegrody pomieszczeń i strefy socjalnej.
15. **Tabela lokalizacji na PDF:**
   - Strefa 1: półkowe 650, paletowe 17
   - Strefa 2: półkowe 1428, paletowe 13
   - Strefa 3: półkowe 0, paletowe 95
   - Strefa 4: półkowe 59, paletowe 7
   - Suma: półkowe 2137, paletowe 132, wszystkie 2269.

## Zakres implementacji
- Three.js, jeden plik HTML; interaktywny obrót, zoom, widok z góry; regały, ściany, strefy, etykiety.
- Wyszukiwanie lokalizacji i wskazywanie regałów.
- Prosta linia po kolejnych punktach służy wyłącznie jako **wizualizacja kolejności pobrań**, nie jako zatwierdzona trasa po przejściach. Celowo nie odtwarzamy błędnej, wymyślonej trasy z poprzednich wersji.
- Bez żadnych integracji z n8n, WMS, BL, SR, Moniti ani innymi systemami.

## Otwarte kwestie dokładności
- Nie wszystkie grafiki, strzałki i szczegóły wewnętrzne z PDF są osobnymi obiektami 3D. Obecnie odwzorowano główne **rodzaje** elementów, a nie gwarantowane 100% elementów rysunkowych.
- Wymagane jest porównanie renderu w przeglądarce z PDF nałożonym jako podkład oraz weryfikacja wszystkich indeksów lokalizacji i rzeczywistych przejść.
- Do zatwierdzenia: dokładne pomiary, położenie przejść, rozstrzygnięcie oznaczeń nieczytelnych na PDF. Nie wolno uznawać mapy za 1:1 bez tych działań.

## Uruchomienie
GitHub Pages: https://atybus-create.github.io/mol-warehouse-3d/

Repozytorium jest publiczne. Nie umieszczać tutaj kluczy, danych klientów ani tajemnic systemowych.
