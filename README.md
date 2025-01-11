# ReverseNX-RT

Alternative Version von ReverseNX, die in **E**cht**z**eit zwischen Handheld- und Docked-Modus wechseln kann.

Benötigt SaltyNX 0.7.0+ und installierte Tesla-Umgebung. Links am Ende der Readme.

Kompatibel mit ReverseNX-Patches/ReverseNX-Tool 2.0.0+.

Nicht kompatibel mit veraltetem ReverseNX-Plugin.

**Verwende ReverseNX-RT nicht neben Status Monitor 0.6.0 oder älter** (Tesla kann auf Atmosphere abstürzen, wenn du NX-FPS verwendest)

Ich plane nicht, weitere Funktionen hinzuzufügen. Zukünftige Updates werden nur Fehlerbehebungen enthalten.

Das Overlay enthält mehrere Modi, von denen 2 die Hauptmodi sind, die anderen sind Fehlerbenachrichtigungen.

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/N4N5UMFN)

# Hauptmodi:
- Wenn das Spiel läuft und alles wie erwartet funktioniert:

![Gra](https://i.imgur.com/ThUbEZ6.jpg) 

Du hast hier nur zwei Optionen:
* Systemsteuerung ändern (Bezieht sich auch auf ReverseNX-Tool-Flags - z.B. wenn du das Docked-Flag für dieses Spiel in ReverseNX-Tool gesetzt hast, erzwingt es bei aktivierter Systemsteuerung den Docked-Modus)
* Modus ändern (deaktiviert, wenn Systemsteuerung aktiviert ist)

Das Spiel bleibt in der aktuellen Konfiguration, bis du das Spiel schließt.

---

# Fehlerbenachrichtigungen:
- **SaltyNX funktioniert nicht!** - SaltyNX ist abgestürzt oder nicht korrekt installiert.
- **Spiel wurde geschlossen! Overlay deaktiviert! Beende das Overlay und starte zuerst das Spiel!** - Wenn du das Overlay im letzten laufenden Spiel verwendet und das Spiel geschlossen hast, ohne das Overlay zu schließen, musst du das Overlay schließen, um es erneut zu verwenden.
- **ReverseNX-RT läuft nicht!** - Plugin wurde nicht injiziert. Es ist entweder ein 32-Bit-Spiel oder befindet sich in der SaltyNX-Ausnahmeliste.
- **Spiel unterstützt Moduswechsel nicht!** - Plugin wurde injiziert und funktioniert, aber die Funktion zum Überprüfen der Modi wurde nicht verwendet. Entweder hat das Spiel keinen (was bedeutet, dass es keinen Unterschied zwischen Handheld und Docked gibt) oder das Spiel überprüft es erst später, als du es überprüfen wolltest (z.B. verwendet das Spiel es möglicherweise erst ein paar Sekunden nach Abschluss des Bootvorgangs). Du musst das Overlay beenden und später erneut ausführen, um zu prüfen, ob der Fehler weiterhin auftritt...
- **FALSCHE MAGIC!** - Etwas ist schrecklich schief gelaufen und das Overlay liest den Wert von der falschen Speicherposition. Das sollte nicht passieren, wenn du das Overlay öffnest, nachdem der Bootvorgang des Spiels abgeschlossen ist. Es kann auch passieren, wenn du das Overlay schließt, bevor du das Spiel beendest, und es nach dem Start des nächsten Spiels öffnest, das diesmal nicht mit SaltyNX kompatibel ist.

# Fehlerbehebung:
Liste der Titel mit Kompatibilitätsproblemen mit ReverseNX-RT:

| Titel | Versionen | Warum? |
| ------------- | ------------- | ------------- |
| Robotics;Notes Elite | 1.0.1 | Defekter PopNotificationMessage()-Thread, funktioniert überhaupt nicht |

Q: Oft stürzt Atmosphere beim Schließen des Spiels mit Fehler 0x41001 ab. Warum?

A: Atmosphere 0.12.0 mit neuen Optionen für die Cheat-Engine brachte einen Fehler mit sich, der diesen Fehler in zufälligen Fällen anzeigt. Aus irgendeinem Grund lässt dieses Overlay diesen Fehler häufiger auftreten. Gehe entweder zurück zu 0.11.1 oder aktualisiere auf eine neuere Version.

# Original Links:

- https://github.com/masagrator/SaltyNX/releases
- https://github.com/WerWolv/nx-ovlloader
- https://github.com/WerWolv/Tesla-Menu
