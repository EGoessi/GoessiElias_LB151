# Projekt-Dokumentation

Goessi

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|       | 0.0.1   | ✍️ Jedes Mal, wenn Sie an dem Projekt arbeiten, fügen Sie hier eine neue Zeile ein und beschreiben in *einem* Satz, was Sie erreicht haben. |
| 23.01 | 1.1.0   | Heute habe ich mit überlegt wie ich bei der Umsetzung vorangehen möchte.                                                             |
| 13.02 | 1.2.0   | Administration programmiert, Angefangen GUI zu programmieren und Github repository aktualisiert                                               |
| 20.02 | 1.3.0   | Spiel angefangen zu programmieren                                                           |
| 27.02  | 1.4.0  |  Github repository fertiggestellt und abgegeben                                                            |


# 0 Ihr Projekt

✍️ Beschreiben Sie Ihr Projekt in einem griffigen Satz.

In diesem Projekt erstelle ich ein Glücksrad mit JSF, bei dem man die Rätselwörter erraten muss und Geld gewinnen kann, dies ist mit einer MySQL Datenbank verbunden.

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
| 1    |  Muss           |  Funktional    | Als Administrator möchte ich mich durch Benutzername und Passwort authentifizieren können, damit ich Zugriff auf die      Administrationsfunktionen habe.
| 2    |  Muss           |  Funktional    | Als Administrator möchte ich Phrasen und Rätselwörter anlegen, damit ich neue Inhalte für die Rätsel- und Wortspiele erstellen kann.
| 3    |  Muss           | Funkional       | Als Administrator möchte ich Phrasen und Rätselwörter ändern/löschen können, damit ich Inhalte aktualisieren/entfernen kann.
| 4    |  Muss           |  Funktional    | Als Administrator möchte ich Kategorien anlegen, damit ich die Inhalte der Rätsel- und Wortspiele organisieren kann.
| 5    |  Muss           |  Funktional    | Als Administrator möchte ich jedes Wort bzw. jede Frage einer Kategorie zuordnen können, damit die Spiele immer mit den relevanten Inhalten ausgestattet sind.
| 6    |  Kann           |  Funktional    | Als Administrator möchte ich einzelne Einträge der Highscore-Liste löschen können, damit ich die Highscore-Liste bereinigen kann.
| 7    |  Muss           |  Funktional    | Als Kandidat/in möchte ich einen Namen eingeben können, der auf der Highscore-Liste erscheint, damit ich mich mit anderen Spielern vergleichen kann.
| 8    |  Muss           |  Funktional    | Als Kandidat/in möchte ich meinen Kontostand sehen, damit ich weiß, wie viel Geld ich bereits gewonnen habe.
| 9    |  Muss           |  Funktional    | Als Kandidat/in möchte ich meine Lebenspunkte sehen, damit ich weiß, wie viele Leben mir noch zur Verfügung stehen.
| 10    |  Kann           |  Funktional    | Als Kandidat/in möchte ich wissen ob meine Anwort richtig oder falsch war, damit ich es nochmals versuchen kann.
| 11    |  Muss           |  Funktional    | Als Kandidat/in möchte ich, dass die Highscore-Liste nach Rang sortiert wird, der durch die Höhe des Geldbetrags bestimmt wird, damit ich weiss wer der beste Spieler ist.
| 12    |  Muss           |  Funktional    | Als Kandidat/in möchte  ich nicht zweimal dasselbe Rätselwort oder dieselbe Phrase gestellt bekommen, damit das Spiel abwechslungsreich bleibt.
| 13    |  Muss           |  Funktional    | Als Kandidat/in möchte ich jederzeit die Möglichkeit haben, entweder weiterzuspielen oder aufzuhören und meinen Gewinn in die Highscore-Liste zu übernehmen, damit ich selber entscheiden kann, wie lange ich spielen möchte.
| 14    |  Muss           |  Funktional    | Als Administrator möchte ich eine spielbare Anzahl an Wörtern und Fragen im Spiel haben, damit das Spiel ausreichend unterhaltsam ist und genügend Abwechslung bietet.
| 15    |  Muss           |  Funktional    | Als Kandidat/in möchte ich, dass die Anzahl der Spielrunden gezählt wird, damit ich meinen Fortschritt beim Spielen verfolgen kann.


✍️ Jede User Story hat eine ganzzahlige Nummer (1, 2, 3 etc. oder Zahl), eine Verbindlichkeit (Muss oder Kann?), und einen Typ (Funktional, Qualität, Rand). 

# 4.2 Testfälle

| TC-№    | Vorbereitung         | Eingabe                | Erwartete Ausgabe 
| ----    | ------------         | -------                | ----------------- 
| 1.1     | Login ist erstellt   | Benutzername und Passwort eingeben        | Admin ist eingeloggt                  
| 2.1     | Als Admin eingeloggt   | Lege neue Phrasen an        | Phrasen wurden erfolgreich in der Datenbank gespeichert  
| 3.1     | Als Admin eingeloggt | Lösche/ändere Phrasen          | Phrasen wurden in der Datenbank aktualisiert/gelöscht
| 4.1     | Als Admin eingeloggt   | Lege Kategorie an       | Kategorie wurde erfolgreich in der Datenbank gespeichert
| 5.1     | Als Admin eingeloggt | Ordne Wort einer Kategorie zu | Kategorie wurde erfolgreich in der Datenbank aktualisiert
| 6.1     | Als Admin eingeloggt   | Lösche Eintrag aus der Highscore-Liste       | Eintrag wurde erfolgreich aus der der Datenbank entfernt
| 7.1     | Spiel ist erstellt   | Gebe Namen ein         | Name wird auf der Highscore-Liste angezeigt
| 8.1     | Spiel ist erstellt   | Gewinnt / Verliert Geld      | Kontostand wird korrekt angezeigt 
| 9.1     | Spiel ist erstellt   | Frage wurde richtig/falsch beantwortet | Lebenspunkte werden korrekt angezeigt
| 10.1     | Spiel ist erstellt   | Frage wurde richtig/falsch beantwortet  | Mitteilung wird auf Bildschirm angezeigt
| 11.1     | Spiel ist erstellt   | Hat höchsten Geldbetrag | Highscore-Liste Rang zuoberst
| 11.2     | Spiel ist erstellt   | Hat tiefsten Geldbetrag | Highscore-Liste Rang zuunterst
| 12.1     | Spiel ist erstellt   | Spiele mehrere runden | Kein Rätselwort wurde zweimal gestellt
| 13.1     | Spiel ist erstellt   | Beende das Spiel und übernehme Gewinn      | Spiel wurde beendet und Gewinn wurde aus Highscore-Liste übernommen
| 14.1     | Als Admin eingeloggt  | Überprüfe ob Spiel ausreichend Anzahl an Wörter enthält | Spiel ist ausreichend unerhaltsam 
|15.1     | Spiel ist erstellt   | Spiele mehrere Runden      |  Anzahl der Spielrunden wurde korrekt gezählt 


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
