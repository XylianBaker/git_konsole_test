# Git auf der Konsole

**Author**: Jan Franz Kammellander

**Login**: jkammellander

**Jahrgang**: 3BHIT

**Erstellt am**: 12.01.2021



[TOC]



## Ordner des Repositorys erstellen

![Ordner erstellen](1.png)

Mit dem Befehl `mkdir` wird ein Ordner namens `gitJkammellander` erstellt, welcher der Ordner für mein Git Repository wird.

![](2.png)

Mit dem Befehl `cd` navigiere ich in den Ordner.

## Git Repository erstellen

![git Init](3.png)

Mit dem Befehl `git init` wird ein lokales Git Repository zur Versionierung erstellt.

## Text erstellen

![](4.png)

Mit dem Befehl `touch` erstelle ich eine README.md datei und bearbeite es mit dem Texteditor **Nano**.

![](5.png)

Danach ersteltle ich eine Textdatei namens **Kammellander.txt** und sfügte dieser den Text "*Kammellander1*" hinzu.

## Status Überprüfen

![status](6.png)

Mit dem Befehl `git status` kann ich den Status meines Staging Bereiches überprüfen und es ist zu erkennen, dass noch keine Version oder Elemente im Staging-Bereich vorhanden isn.

## Datei zum Staging Bereich hinzufügen

![add staging](7.png)

Mit dem Befehl `git add` wird eine Datei dem Stagin-Bereich hinzugefügt. In meinem Fall habe ich die Datei **README.md** und **Kammellander.txt** diesem hinzugefügt. Anshcließend habe ich mit `git status` überprüft, ob die Dateien im Staging-Bereich vorhanden sind; sie sind vorhanden.

![](8-1610407685640.png)

Danach habe ich mit dem Befehl `git diff --staged` überprüft, ob bereits vorhandene Elemente überschrieben wurden und welche Zeile veränderten wurde; es wurde nichts verändert, nur etwas Neues hinzugefügt. 



Anschließend habe ich mit dem Befehl `git commit` meine erste Version bereitgestellt. Die Flag `-m` benötige, sodass ich danach mit Anführungszeichen `"NEW: First Commit"` meine Commit-Nachricht hinzuschreiben konnte, ohne dass ich diese in einem Textdeditor vorher schreiben und speichern muss.

## Ziffer der Datei ändern

![](9.png)

Nun habe ich die Datei **Kammellander.txt** geändert indem ich eine **1** mit einer **2** ausgetauscht habe. Danach habe ich mit `git status` überprüft, ob die Datei modifiziert wurde; sie wurde.

## Erneut zum Stagin Bereich hinzufügen

![git add](10.png)

Nun füge ich meine veränderte Datei **Kammellander.txt** dem Staging-Bereich hinzu.

![diff & status](11.png)

Als nächstes überprüfe ich mit dem Befehl `diff`, ob die Ziffe richtig modifiziert wurde; sie wurde. Anschließend habe ich noch den Staging-Bereich überprüft, ob die Datei modifiziert wure; sie wurde verändert.

## Log-Eintrag

![log](12.png)

Mit dem Befehl `git log` schaue ich nach, ob meine erste Version vorhanden ist. Wie es im Bild zu sehen ist, wurde die Version von mir bereitgestellt und zwar am Montag dem 11 Jänner.

## Jahrgang.info

![Info-Datei](13.png)

Nun erstelle ich eine Datei Namens **3BHIT.info**, welche meine Klasse alst Text ("*3BHIT*") enthält. Anschließend habe ich mit `status` überprüft, ob die Datei nicht von git getracked wird und aus der Version ausgeschlossen ist.

## Ausschließen der Versionierung

![.gitignore](14.png)

Dass zukünftig und im hier und jetzt alle Datein welche auf "**.info**" enden von meinen und den Versionen anderer Contributer ist, erstelle ich ein sogenanntes **.gitignore-file**. Dieses beinhaltet Dateien, Ordner und Dateiendungen, welche aus den Versionen vorenthalten beliben soll und von git ignoriert werden sollen. Deswegen habe ich der Datei folgendes hinzugefügt: "**.info*".

![](15.png)

Zuguterletzt habe ich mit `status` überprüft, ob das **.gitignore-file** von git erkannt wurde und alle Dateien mit der Endung "*.info*" von Git ignoriert werden.

## Änderungen dem Repository Hinzufügen

![add gitignore](16.png)

Nun wird das **.gitignore-file** dem Staging-Bereich hinzugefügt.

![](17.png)

Anschließend wird eine neue Version von mir erstellt und mit `log` überprüfe, ob meine neue Version vorhanden ist.

## Unterordner erstellen

![](18.png)

Ich habe einen Unterordner mit dem Befehl `mkdir` namens Jan erstellt und überprüft, ob dieser von git erkannt wurde.

### Unterordner dem Repository hinzufügen

Der Ordner kann dem Respoitry Übertrage werden. Er wird allerdings von Git nicht erkannt und muss manuell dem Staging-Bereichhinzugefügt werden. Allerdings macht es nur Sinn, wenn der Ordner ein **Subfolder** ist und keine großen unrelevanten Dateien enthält

![ls](19.png)

## Dem Unterordner Dateien hinzufügen

![Jan.txt](20.png)

Nun habe ich dem Unterordner **Jan** die Datei **Jan.txt**, welche meinen Vornamen ("*Jan*") beinhaltet.

### Datei verschieben

![](21.png)

Mit dem Befehl `mv` kann ich eine Datei eines Pfades in einen anderen Pfad verschieben. Anschließend wurde die Datei **Kammellander.txt** erneut modifiziert und zwar wurde die Ziffer **2** nun mit der Zahl **3** ersetzt wurde.

![status folder](22.png)

Zuletzt habe ich mit `status` überprüft, ob alle Änderungen übernomen und erkannt wurden.

## Dateien im Unterordner in Git stagen

![Files add](23.png)

Mit dem Befehl `git add .` wurden alle Dateien, die nicht ignoriert werden, im Ordner in welchem ich mich befinde, dem Staging-Bereich hinzugefügt. Zuletzt überprüfe ich mit `status` meine Veränderungen.

## Neue Version

![new Version](24.png)

Nun wird eine dritte Version erstelltm, in welche ein Unterornder, mit dessen Dateien, hinzugefügt wurde.

![log subfolder](25.png)

Zuletzt habe ich mit `log` alle meine Versionen überprüft.

## Das lokale repository als remote-repository hinzufügen

![remote](26.png)

Mit dem Befehl `git remote add origin` wird das lokale Repository mit einem Remote Repository verbunden. Der Befehl `branch -M master` erstellt ein branch für das Remote Repository.

![push](27.png)

Zuletzt wird mit `git push U- origin master` alle Commits auf das remote Repository auf den Branch Master gepushed.

## Github repository

-> [My Github repo](https://github.com/XylianBaker/git_konsole_test.git)