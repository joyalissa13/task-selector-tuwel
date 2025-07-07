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


__________________________________________________________

# task-selector-tuwel

## General

This project is designed to allow students of the course **Ways of Thinking in Computer Science** at **TU Wien** to enter their selection of ways of thinking directly in TUWEL, save it, and export the associated dates as an `.ics` file.

The goal is to give students more flexibility in semester planning while avoiding incorrect or duplicate entries.

## Configuration

### Tuwel Configuration  
Make sure that in the Database activity in Tuwel the following settings are selected:

### Entries

The following applies:  
- Release required: No  
- Required entries before viewing all data: Number > 1 (otherwise all entries are visible to all students)  
- Maximum possible entries: 1

### Availability  
- Lock editing from: [deadline]

There are constants and functions in the code that must be adjusted annually.

### LECTURES

The constant `LECTURES` defines the lecture entries in the following format:

- `Way of Thinking`: Name of the way of thinking (e.g., "Scientific Thinking")  
- `Date`: Date of the lecture in `YYYY-MM-DD` format  
- `Panel`: Date of the associated panel discussion in `YYYY-MM-DD` format  
- `Priority`: Number between 1 and 8 (corresponding to the lecture order)

### Exercises

The constant `Exercises` defines the exercise units, divided into Monday & Wednesday.

### Tasks

Defines the different task types, e.g.:  
```js
  const TASK_TYPES = ['Workshop', 'Miniproject1', 'Miniproject2', 'Games', 'PanelDiscussion'];
``` 

These are linked with the number of allowed ways of thinking that must be selected for the respective format.

### getDateByTaskType (...)
This function contains the logic for how the due date is calculated. It must be reviewed and updated annually.