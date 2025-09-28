1. Was ist der Unterschied zwischen Working Directory, Staging Area und Repository?
	Working Directory: Der Projektordner, in dem Dateien aktiv bearbeitet werden.
	Staging Area (Index): Ein Zwischenbereich, in dem ausgewählte Änderungen für den nächsten Commit gesammelt werden.
	Repository (.git-Ordner): Die Datenbank, in der Git alle committeten Versionen (die Projekthistorie) dauerhaft speichert.
2. Woran erkennst du, ob ein Merge Fast-Forward war?
	In der Ausgabe des git merge-Befehls erscheint der Hinweis "Fast-forward". 
	Zudem wird kein neuer Merge-Commit in der git log Historie erstellt; stattdessen wird der Branch-Zeiger auf den neuesten Commit verschoben.
3. Warum kann git merge --ff-only manchmal fehlschlagen?
	Der Befehl schlägt fehl, wenn der Ziel-Branch (z. B. main) seit dem Abzweigen des Feature-Branches neue, eigene Commits erhalten hat. Da die Historien divergiert sind, wäre ein Merge-Commit erforderlich, was durch die Option --ff-only unterbunden wird.
4. Was ist der Vorteil, Änderungen zuerst auf einem Branch wie dev zu machen?
	Der Hauptvorteil liegt in der Stabilität des Haupt-Branches (z. B. main). Neue Features werden isoliert auf dem dev-Branch entwickelt. Dadurch wird die funktionierende, produktive Codebasis auf main nicht durch unfertige Entwicklungen gefährdet und bleibt stets einsatzbereit
5. Mit welchem Befehl siehst du den aktuellen Branch?
	Mit dem Befehl git branch
6. Mit welchen Befehlen machst du Änderungen sichtbar und dauerhaft (Stichworte: Staging & Commit)?
	Sichtbar machen (Staging): git add <Dateiname> oder git add .
	Dauerhaft machen (Commit): git commit -m "Commit-Nachricht"