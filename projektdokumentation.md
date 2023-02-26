# Projekt-Dokumentation

Goessi

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|       | 0.0.1   | ✍️ Jedes Mal, wenn Sie an dem Projekt arbeiten, fügen Sie hier eine neue Zeile ein und beschreiben in *einem* Satz, was Sie erreicht haben. |
| 23.01 | 0.0.2   | Heute habe ich mit überlegt wie ich bei der Umsetzung vorangehen möchte.                                                             |
|       | 0.0.3   |                                                              |
|       | 0.0.4   |                                                              |
|       | 0.0.5   |                                                              |
|       | 0.0.6   |                                                              |
|       | 1.0.0   |                                                              |

# 0 Ihr Projekt

✍️ Beschreiben Sie Ihr Projekt in einem griffigen Satz.

In diesem Projekt erstelle ich ein Glücksrad bei dem man die Rätselwörter erraten muss, dies ist mit einer Datenbank verbunden.

# 1 Analyse

✍️ Beschreiben Sie, auf welchem Tier Sie die dynamischen Elemente der Anwendung unterbringen möchten:

* Tier 1 (Presentation): Anzeige des Glücksrads, Anzeige Login für Admin, Anzeige der Rätsel-Begriffe, Anzeige der Highscore-Liste, Kontostand und Lebenspunkte     anzeigen
* Tier 2 (Webserver): Namen eingeben, Glücksrad drehen, Vokale eingeben, Als Admin Benutzername und Passwort eingeben 
* Tier 3 (Application Server): Antwort richtig oder falsch, Highscore-Liste ausgeben, Phrasen und Rätselwörter bearbeiten, Kategorien erstellen
* Tier 4 (Dataserver): Speichern der Phrasen, Speichern der Kategorien, Speichern Highscore-Liste Daten, Admin Logindaten speichern

# 2 Technologie

✍️ Beschreiben Sie für dieselben Tiers, welche Programmiersprache bzw. Technologie Sie verwenden möchten.

Tier 1 (Presentation): HTML für die Struktur der Webseite, CSS für das Styling der Webseite, JavaScript für die Interaktivität und Animationen

Tier 2 (Webserver): Apache als Webserver-Software, Node.js als Laufzeitumgebung für JavaScript auf dem Server

Tier 3 (Application Server):Node.js als Laufzeitumgebung für JavaScript auf dem Server, Express.js als Framework für den Webserver

Tier 4 (Dataserver): MySQL als relationale Datenbank zur Speicherung von Spiel- und Benutzerdaten, Sequelize als Object-Relational Mapping für den Zugriff auf die Datenbank.

# 3 Datenbank

✍️ Wie steuern Sie Ihre Datenbank an? Wie ist das Interface aufgebaut? 

Die Datenbank steuere ich mit einer Datenbank-Verbindung an, über die man auf die Datenbank zugreifen kann. Dazu wird ein Treiber benötigt, welches es möglich macht mit der Datenbank zu kommunizieren.
Das Interface für den Zugriff auf die MySQL Datenbank, wird SQL verwendet, um Datenbank Abfragen zu erstellen. 
Das Interface zur Datenbank besteht aus Funktionen und Methoden, die es ermöglichen, Daten zu lesen, zu schreiben und zu aktualisieren. Diese können direkt im Code aufgerufen werden.

# 4.1 User Stories

✍️ Formulieren Sie klare Anforderungen in der Form von User Stories (*„als … möchte ich … damit …“*) und zu jeder Anforderung mindestens einen dazugehörigen Testfall (in Kapitel 4.2). 

✍️ Formulieren Sie weitere, eigene Anforderungen und Testfälle, wie Sie Ihre Applikation erweitern möchten. Geben Sie diesen statt einer Nummer einen Buchstaben (`A`, `B`, etc.)

| US-№ | Verbindlichkeit | Typ            | Beschreibung                       |
| ---- | --------------- | ----           | ---------------------------------- 
| 1    |  Muss           |  Funktional    | Als Administrator möchte ich mich authentifizieren können, damit ich Phrasen, Rätselwörter und Kategorien bearbeiten kann
| 2    |  Muss           |  Funktional    | Als Administrator möchte ich mich authentifizieren können, damit ich Einträge aus der Highscore-Liste löschen kann 
| 3    |  Muss           |  Funktional    | Als Kandidat/in möchte ich mich einen Namen eingeben können, damit ich auf der Highscore-Liste erscheine
| 4    |  Muss           |  Funktional    | Als Kandidat/in möchte ich wissen ob meine Anwort richtig oder falsch war, damit ich es nochmals versuchen kann
| 5    |  Kann           |  Funktional    | Als Kandidat/in möchte ich jederzeit aufhören oder weiterspielen können, damit ich selber entscheiden kann
| 6    |  Muss           |  Funktional    | Als Kandidat/in möchte ich jederzeit den Kontostand und die Lebenspunkte sehen, damit ich den Überblick habe


✍️ Jede User Story hat eine ganzzahlige Nummer (1, 2, 3 etc. oder Zahl), eine Verbindlichkeit (Muss oder Kann?), und einen Typ (Funktional, Qualität, Rand). 

# 4.2 Testfälle

| TC-№    | Vorbereitung         | Eingabe                | Erwartete Ausgabe 
| ----    | ------------         | -------                | ----------------- 
| 1.1     | Login ist erstellt   | einloggen Admin        | Admin ist eingeloggt                  
| 1.2     | Login ist erstellt   | einloggen Admin        | Admin ist eingeloggt  
| 1.3     | Spiel ist erstellt   | Name eingeben          | Name wird gespeichert 
| 1.4     | Spiel ist erstellt   | Anwort eingeben        | Anwort ist richtig/falsch
| 1.5.1   | Spiel ist erstellt   | Spiel abbrechen        | Spiel wird abgebrochen
| 1.5.2   | Spiel ist erstellt   | Spiel weiterspielen    | Spiel geht weiter
| 1.6.1   | Spiel ist erstellt   | Kontostand nimmt zu/ab | Kontostand wird angezeigt
| 1.6.2   | Spiel ist erstellt   | Anwort war falsch      | Lebenspunkte werden angezeigt

✍️ Die Nummer hat das Format `N.m`, wobei `N` die Nummer der User Story ist, die der Testfall abdeckt, und `m` von `1` an nach oben gezählt. Beispiel: Der dritte Testfall, der die zweite User Story abdeckt, hat also die Nummer `2.3`.

# 5 Prototyp

✍️ Erstellen Sie Prototypen für das GUI (Admin-Interface und Quiz-Seite).

![image](https://user-images.githubusercontent.com/54137474/214005657-5e14c98d-a477-438f-acb5-a9102feeaec1.png)

![image](https://user-images.githubusercontent.com/54137474/214008835-bbff3b0e-679e-426b-a150-59c787739580.png)

![image](https://user-images.githubusercontent.com/54137474/214008029-a17f8eb9-285c-4bdb-9ebb-2d4593f3f813.png)


# 6 Implementation

✍️ Halten Sie fest, wann Sie welche User Story bearbeitet haben

| User Story | Datum | Beschreibung |
| ---------- | ----- | ------------ |
| ...        |       |              |

# 7 Projektdokumentation

| US-№ | Erledigt? | Entsprechende Code-Dateien oder Erklärung |
| ---- | --------- | ----------------------------------------- |
| 1    | ja / nein |                                           |
| ...  |           |                                           |

# 8 Testprotokoll

✍️ Fügen Sie hier den Link zu dem Video ein, welches den Testdurchlauf dokumentiert.

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |       |          |        |
| ...  |       |          |        |

✍️ Vergessen Sie nicht, ein Fazit hinzuzufügen, welches das Test-Ergebnis einordnet.

# 9 `README.md`

✍️ Beschreiben Sie ausführlich in einer README.md, wie Ihre Applikation gestartet und ausgeführt wird. Legen Sie eine geeignete Möglichkeit (Skript, Export, …) bei, Ihre Datenbank wiederherzustellen.

# 10 Allgemeines

- [ ] Ich habe die Rechtschreibung überprüft
- [ ] Ich habe überprüft, dass die Nummerierung von Testfällen und User Stories übereinstimmen
- [ ] Ich habe alle mit ✍️ markierten Teile ersetzt
