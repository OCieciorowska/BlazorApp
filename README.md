# BlazorApp – Komponent prognozy pogody 🌤

Prosta aplikacja Blazor Web App z komponentem wyświetlającym prognozę pogody, z możliwością filtrowania i podstawową analizą liczby ciepłych dni.

##  Funkcje

- **Generowanie losowej prognozy pogody na 10 dni**
- **Filtracja dni z temperaturą powyżej 15°C**
- **Wyszukiwanie po opisie pogody (np. "Warm", "Hot")**
- **Wyświetlanie liczby ciepłych dni**
- **Tabela z datą, temperaturą w °C i °F oraz podsumowaniem**

## Opisy funkcji znajdujących się w pliku Weather.razor:
- OnInitializedAsync()

  
Asynchroniczna metoda inicjalizująca komponent.
Generuje losową prognozę pogody na 10 dni.
Oblicza liczbę ciepłych dni (temperatura > 15°C).
Zapisuje prognozy do zmiennej pomocniczej originalForecasts (do późniejszego przywracania).

- FilterWarmDays()


Filtrowanie prognoz tak, aby pozostały tylko dni cieplejsze niż 15°C.
Używane po kliknięciu przycisku „Pokaż tylko ciepłe dni”.

- RestoreForecasts()


Przywraca pełną listę prognoz pogodowych z kopii originalForecasts.

- FilterBySummary(ChangeEventArgs e)

  
Filtrowanie prognoz na podstawie wpisanego tekstu (nazwa/summary, np. "Hot").

Obsługuje dynamiczne filtrowanie podczas wpisywania. Odświeża też liczbę ciepłych dni po przefiltrowaniu.

## WeatherForecast (klasa wewnętrzna)
Model danych prognozy:

- Date – data prognozy,
- TemperatureC – temperatura w °C,
- Summary – opis pogody (np. "Warm"),
- TemperatureF – temperatura przeliczona na °F.
