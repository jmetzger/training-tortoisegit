# Überblick über Arbeitsweise 

## Szenario 1: Arbeiten an einem Feature 

  * Wann immer ich etwas umsetzte, erstelle ich zunächste ein feature
  * Arbeitszeit an Feature möglichst klein halten (wenn feature zu gross, dann in kleinere mini-features aufbrechen) 

### Schritt 1: Am Tag 0 

  1. Im master (ich muss mich im master befinden) den aktuellen Stand herstellen (tortoise -> pull -> master)
  2. In einen neuen Branch reinswitchen (tortoisegit -> switch/checkout -> create branch) Empfehlung Prefix feature/ z.B. feature/anpassung-instrument oder auch ticket-id
  3. An dem Projekt arbeiten (d.h. add + commit von neuen und geänderten files), gerne viele commits pro tag
  4. einmal täglich Stand auf server pushen (für Krankheitsfall) - push des feature-branches

### Schritt 2: Danach täglich (wenn ich länger an dem Feature arbeite)

  1. morgen: aktuellen stand holen: tortoisegit -> pull vom master [remote branch : master)  (ich bin nachwievor im Feature)
  2. an dem projekt arbeiten (s. Schritt 1)
  3. abends wieder stand auf server push (für Krankheitsfall) push des feature - branches

 ### Schritt 3: Juppie Yeah, ich bin fertig mit feature 

  1. Nochmal zur Sicherheit Änderungen vom master pullen (ich bin nachwievor im feature)
     (d.h. im feature -> tortoisegit -> pull (remote branch: master)
     Evtl. hier Konflikte auflösen
  2. Pushen des feature-branches auf den Server
  3. Merge request erstellen (Achtung: Source ist der feature - branch, target is der master branch --> d.h. Änderung sollen in den master übernommen werden)

### Schritt 4a: mergen (kein Konflikt vorhanden) in gitlab 

  * Bevorzugt online mergen 
  * Im merge request ist ersichtlich, dass ich mergen kann (grüner Mergebutton erscheint)

  1. Gitlab: Merge button klicken (es wird gemerged)
  1. Aufräumen (Tortoisegit)
     1. In master wechseln (tortoisegit -> switchto -> master)
     1. Pull im master von master (remote branch bleibt master)
     1. tortoisegit -> show log -> lokalen branch löschen
    
### Oder: Schritt 4b: mergen (konflikt vorhanden) in gitlab 

  * Bevorzugt online mergen 
  * Im merge request ist ersichtlich, dass ich NICHT mergen kann (rotes Schild, kein grüner Button vorhanden)

  1. tortoisegit im feature-branch -> tortoisegit -> pull -> von master !! (Achtung: remote branch in master) ändern im Select 
  1. tortoisegit: Es wird ein Konflikt angezeigt und der Resolve button (ganz links). Diesen drücken
  1. tortoisegit: Kleines Fenster öffnet sich mit Liste der Files mit Konflikt in rot
  1. tortoisegit: File anklicken(doppelt)
  1. tortoisgit: mergetool öffnet sich
  1. tortoisegit mergetool: Konflikte lösen, danach grünen Haken drücken und Fenster schliesen
  1. tortoisegit: kleines Fenster schliessen
  1. tortoisegit: commit -> feature/xyz  (Achtung kommentare rausnehmen und commit klicken)
  1. tortoisegit: push -> feature/xyz - branch
  1. Online: merge request neu laden (F5) oder einfach nochmal im Menü links merge request anklicken
  1. Online: im merge request - mergen (sollte jetzt auf grün stehen)
  1. Aufräumen (Tortoisegit)
     1. In master wechseln (tortoisegit -> switchto -> master)
     1. Pull im master von master (remote branch bleibt master)
     1. tortoisegit -> show log -> lokalen branch löschen 



 
