# Specyfikacja przypadków użycia

## Dodawanie zleceń od strony dyspozytora

### Cel:

Dodanie zlecenia i wyszukanie kierowcy do danego zlecenia

### Główny aktor:

Dyspozytor

### Warunek początkowy:

Dyspozytor znajduje się na stronie głównej swojej aplikacji

### Zdarzenie początkowe (wyzwalacz):

Dyspozytor wciska przycisk "Dodaj zlecenie"

### Główny scenariusz sukcesu:

1. Otwiera się panel dodawania zlecenia
2. Dyspozytor uzupełnia pole zawierające punkt startowy zlecenia
3. Dyspozytor uzupełnia pole zawierające punkt docelowy zlecenia
4. Dyspozytor wciska przycisk "Dodaj zlecenie" w panelu dodawania zlecenia
5. System wyszukuje najbliższego dostępnego kierowcę, który mógłby przyjąć dodane zlecenie
6. Kierowca otrzymuje powiadomienie o przychodzącym zleceniu do akceptacji
7. Automatyczne przekierowanie dyspozytora z powrotem na stronę główną aplikacji

### Scenariusze alternatywne:

2.1  Dyspozytor wciska przycisk "Anuluj" w panelu dodawania zlecenia
* Przekierowanie z powrotem na stronę główną aplikacji i ewentualne wyczyszczenie wpisanych szczegółów zlecenia

## Akceptacja zleceń od strony kierowcy

### Cel:

Akceptacja zlecenia przez kierowcę w celu jego realizacji

### Główny aktor:

Kierowca

### Warunek początkowy:

Kierowca ma w aplikacji status "dostępny"

### Zdarzenie początkowe (wyzwalacz):

System dopasowuje danego kierowcę do zlecenia

### Główny scenariusz sukcesu:

1. Kierowca otrzymuje powiadomienie z aplikacji o przychodzącym zleceniu
2. Kierowca klika w przychodzące powiadomienie
3. Otwiera się okno ze szczegółami zlecenia
4. Kierowca klika "Zaakceptuj"
5. Status kierowcy zmienia się na "zajęty"
6. System automatycznie ustawia nawigację kierowcy w aplikacji do miejsca startowego kursu
7. Po dojechaniu na miejsce, kierowca wciska przycisk "Rozpocznij kurs"
8. System automatycznie ustawia nawigację kierowcy w aplikacji do miejsca docelowego kursu
9. Po dojechaniu na miejsce, kierowca wciska przycisk "Zakończ zlecenie"
10. Otwiera się okno podsumowania kursu
11. Kierowca wciska "Ok"
12. Status kierowcy zmienia się na "dostępny"
13. Automatyczne przekierowanie kierowcy na stronę główną aplikacji

### Scenariusze alternatywne:

4.1 Kierowca klika "Odrzuć"
* System wyszukuje innego najbliższego dostępnego kierowcę do zlecenia
* Przekierowanie kierowcy na stronę główną aplikacji

9.1 Kierowca wciska przycisk "Anuluj zlecenie"
* System wysyła informację do dyspozytora o anulowanym zleceniu
* Status kierowcy zmienia się na "dostępny"
* Przekierowanie kierowcy na stronę główną aplikacji
