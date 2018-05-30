# Fortgeschrittene Aufgaben, Tag 1

## Infrastruktur

1. Schaut, dass euer Rechner die nötigen Anforderungen erfüllt:
   - eine lokale PHP-Installation ab Version 7
   - eine lokale MySQL-Installation
   - PhpStorm
   - Chrome
2. Legt einen MySQL-User an, der die Rechte hat, Datenbanken anzulegen
   und zu löschen.
2. Klont die [Tea-Extension](https://github.com/oliverklee/tea) von GitHub.
3. Installiert die Abhängigkeiten (für TYPO3 8.7) wie in der
   [README](https://github.com/oliverklee/tea) beschrieben.
4. [Richtet euch die PHPUnit-Run-Konfigurationsvorlage ein](https://github.com/oliverklee/tea#general-phpunit-setup)
   und gebt dort die Datenbank-Zugangsdaten für den MySQL-User und die
   Datenbank ein.
5. Bekommt die Unit-Tests in PhpStorm zum Laufen.
6. Bekommt die funktionalen Tests in PhpStorm zum Laufen.
7. Räumt die temporären Dateien der Tests wieder weg.
8. Löscht automatisch generierten Test-Datenbanken.

## Tests-Suites

1. Legt eine Konfigurationsdatei mit einer Test-Suite für alle funktionalen
   Repository-Tests an.

## Funktionale Repository-Tests (und Controller-Tests)

1. Legt testgetrieben (mit Unit-Tests) ein `Testimonial`-Model im
   `Rating`-Kontext an (noch ohne TCA etc.), das folgende Felder hat:
   - `title` (`string`)
   - `text` (`string`, mit RTE)
   - `creationDate` (`DateTime`)
   - `numberOfStars` (`int`)
   - n:1-Assoziation zum `Tea`-Model
2. Legt für das Model SQL, TCA und Locallang an.
3. Legt ein Repository für das Model an und ergänzt die minimalen Unit-Tests
   dafür.
4. Legt funktionale Tests an, dass das Model aus der Datenbank gelesen und geschrieben werden kann. Das Repository soll die Storage-PID ignorieren.
   Testet auch, dass die Spalte `crdate` auf das Feld `creationDate` gemappt
   wird.
5. Testet mit funktionalen Tests auch die Assotiation zum `Tea`-Model.
6. Legt im `TeaController` eine `new`- und eine `create`-Action an und testet
   mit funktionalen Tests (zusätzlich zu den üblichen Unit-Tests), dass ein
   übergebenes Model persistiert wird. Diese Actions brauchen erst einmal noch
   keine Templates, keine Validierung, keine Einträge in der `ext_localconf`
   etc.
