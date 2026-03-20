# wG Migration Tool

**Browser-Tool zur Migration von MemberPress-Kursinhalten nach WordPress.**
Konvertiert WordPress WXR-Exporte aus MemberPress/MemberPress Courses in eine neue WXR-Datei, die direkt über den WordPress-Importer eingespielt wird.

🔗 **Live:** https://mazelwinkler-oss.github.io/wg-migration-tool/

---

## Was das Tool macht

- Liest WXR-Exporte (XML) aus WordPress/MemberPress
- Erkennt automatisch Kurse, Sektionen, Lektionen und Angebote
- Löst Term-IDs auf – mit manuellem Mapping-Fallback falls nötig
- Zeigt Vorschau: Kategorie-Baum, Lektionen, Angebote
- Validiert die Daten vor dem Export
- Generiert eine fertige WXR-Datei → direkt in WordPress importierbar

**Kein Server. Kein Build-Schritt. Einfach die HTML-Datei im Browser öffnen.**

---

## Unterstützte Post-Types

| Quellsystem | Typ |
|-------------|-----|
| MemberPress Courses | `mpcs-lesson`, `mpcs-course`, `mpcs-section` |
| LearnDash | `sfwd-lessons`, `sfwd-courses` |
| LifterLMS | `llms_membership` |
| MemberPress | `memberpressproduct` |

---

## Verwendung

### Option A – Direkt im Browser (empfohlen)
→ https://mazelwinkler-oss.github.io/wg-migration-tool/

### Option B – Lokal
1. `index.html` herunterladen
2. Im Browser öffnen (kein Server nötig)

---

## Ablauf

```
Schritt 1    →  XML-Dateien hochladen (Lektionen, Kurse, Angebote)
Schritt 1.5  →  Term-ID-Mapping (nur wenn keine <wp:term>-Definitionen im Export)
Schritt 2    →  Vorschau prüfen (Kategorie-Baum, Lektionen, Angebote)
Schritt 3    →  Validierung
Schritt 4    →  WXR herunterladen → WordPress Importer
```

**Tipp:** Beim Export aus WordPress unter „Alle Inhalte" werden Term-IDs automatisch aufgelöst.
Bei separaten Post-Type-Exporten → Schritt 1.5 (manuelles Mapping) nutzen.

---

## Entwickelt von

[webGefährte](https://webgefaehrte.de) – für die Migration des SEO Sharing-Systems.

---

## Lizenz

MIT
