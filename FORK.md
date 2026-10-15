# Fork-Hinweis

Dieses Repository ist ein Fork von [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) (Autor: Ayoub Ghriss, Lizenz MIT). Die Lizenz und der Urheberrechtsvermerk des Originals bleiben unverändert in `LICENSE`.

## Herkunft

| Angabe | Wert |
|---|---|
| Original | https://github.com/ayghri/i-have-adhd |
| Übernommener Stand | Commit `1ecea1993b7fce257ffbd686c070948b5e07eda6` (2026-10-11), Version 0.4.1 |
| Sicherheitsprüfung | 2026-10-15, nur gelesen: kein Netzwerkzugriff, keine Ausführung von Fremdcode, keine Verschleierung, keine versteckten Zeichen (siehe unten) |

## Änderungen gegenüber dem Original

Der Fork ist rein additiv. Keine Datei des Originals wurde geändert.

- **Neu:** `skills/adhs-modus/SKILL.md`, Version 1.0.0. Deutschsprachige Fassung der zehn Regeln, angepasst auf einen persönlichen Arbeitsstandard:
  - Der ADHS-Stil gilt nur für Chatantworten. Dokumentation, Projekt- und Produkttexte und alles für Dritte werden vollständig und ordentlich geführt.
  - Globale Anweisungen haben Vorrang: bei unklarem Briefing zuerst Rückfrage, Plan vor der Umsetzung, kurze Zusammenfassung mit offenen Punkten am Ende.
  - Schreibregeln gegen Floskeln und Füllsätze gelten für Chat und Dokumente.
- **Neu:** diese Datei.

Das Original (`skills/i-have-adhd/`, Hooks, Manifeste, Skripte) liegt unverändert daneben und wird nicht genutzt.

## Nutzung

Nur der Skill-Text wird verwendet. Es wird kein Plugin installiert und kein Hook aktiviert. Aufruf mit `/adhs-modus`, beenden mit „stop adhs-modus“ oder „normaler modus“.

## Update vom Original

Neue Versionen des Originals werden nicht automatisch übernommen. Vor jeder Übernahme wird der Diff gelesen, besonders Hooks, Skripte und Manifeste.

```
git remote add upstream https://github.com/ayghri/i-have-adhd
git fetch upstream
git diff main upstream/main
```

## Ergebnis der Sicherheitsprüfung (Stand `1ecea19`)

- `SKILL.md` besteht nur aus Text, ohne Befehle.
- Der Hook liest beim Sitzungsstart nur die Flag-Datei `~/.claude/.i-have-adhd-always` und `SKILL.md` und gibt den Text aus. Ohne Flag-Datei geschieht nichts.
- Plugin-Code für OpenCode und Pi liest nur `SKILL.md` und die Flag-Datei.
- Die Skripte unter `scripts/` dienen der Auswertung der Wirkung und starten lokale Programme nur bei manueller Ausführung.
- `logo.png` wurde als Bild nicht geprüft.
