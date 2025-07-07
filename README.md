# task-selector-tuwel

## Allgemein

Dieses Projekt dient dazu, Studierenden der LVA **Denkweisen der Informatik** der **TU Wien** zu erlauben, ihre Denkweisen-Auswahl direkt in TUWEL einzutragen, zu speichern und die zugehörigen Termine als `.ics`-Datei zu exportieren.

Das Ziel ist, den Studierenden mehr Flexibilität bei der Semesterplanung zu geben und gleichzeitig fehlerhafte oder doppelte Eingaben zu vermeiden.

## Konfiguration

### Tuwel-Konfiguration
Achten Sie darauf, dass in der Aktivität Datenbank im Tuwel folgende Einstellungen ausgewählt sind:

### Einträge

Hier gilt:
- Freigabe erforderlich: Nein
- Erforderliche Einträge vor der Ansicht aller Daten: Zahl > 1 (denn sonst sind alle Einträge für alle Studenten ersichtlich)
- Maximale mögliche Einträge: 1

### Verfügbarkeit
- Bearbeiten sperren ab: [frist]

Im Code befinden sich Konstanten und Funktionen, die jährlich angepasst werden müssen.

### LECTURES

Die Konstante `LECTURES` definiert die Vorlesungseinträge in folgendem Format:

- `Denkweise`: Name der Denkweise (z. B. "Scientific Thinking")
- `Datum`: Datum der Vorlesung im Format `YYYY-MM-DD`
- `Panel`: Datum der zugehörigen Paneldiskussion im Format `YYYY-MM-DD`
- `Priorität`: Zahl zwischen 1 und 8 (entspricht der Vorlesungsreihenfolge)

### Exercises

Die Konstante `Exercises` definiert die Übungseinheiten, aufgeteilt in Montag & Mittwoch.

### Tasks

Definiert die unterschiedlichen Aufgabentypen, z.B.:  
```js
  const TASK_TYPES = ['Workshop', 'Miniprojekt1', 'Miniprojekt2', 'Games', 'PanelDiscussion'];
```
Diese sind verbunden mit der Anzahl der erlaubten Denkweisen, die zu dem jeweiligen Format ausgewählt werden müssen.

### getDateByTaskType (...)
Diese Funktion beinhaltet die Logik, wie das Datum der Abgabe berechnet wird. Diese ist jährlich zu überprüfen und zu aktualisieren.