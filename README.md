# 📋 Template-Anleitung

> **Für Kursteilnehmer*innen:** Diese Sektion nach dem Setup deines Projekts löschen!

## So verwenden Sie dieses Template:
Dieses Template hilft dir, dein Data Science Projekt effizient zu organisieren und zu dokumentieren. Es bietet eine gängige Struktur, um deine Arbeit zu planen, durchzuführen und zu präsentieren.

### 1. Template verwenden
Templates können in GitHub über den Button **"Use this template" -> "Create a new repository"** in der oberen rechten Ecke in ein eigenes Repository überführt werden. Nutze diese Vorlage als Inspiration und passe sie an dein Projekt an! 

### 2. Projekt klonen
Danach kannst du dein neues Repository direkt über VS Code klonen. Dazu öffnest du in VS Code die Kommando-Palette (Strg+Shift+P) bzw. (Cmd+Shift+P) auf dem Mac und gibst **"Git: Clone"** ein. Wähle dann "Clone from GitHub..." und melde dich ggf. bei GitHub an. Suche nach deinem Repository und wähle einen lokalen Ordner aus, in dem das Projekt gespeichert werden soll.

### 3. Abhängigkeiten installieren
Nachdem du das Repository geklont hast, musst du die Abhängigkeiten installieren. Öffne dazu ein neues Terminal in VS Code über die Menüleiste "Terminal"->"Neues Terminal" und führe die folgenden Befehle aus:

```bash
uv sync
```

### 4. Erweiterungen hinzufügen
Für dieses Projekt empfehlen wir die Installation der folgenden VS Code Erweiterungen:
- **Python** (Microsoft) - Bietet Unterstützung für Python-Entwicklung.
- **Jupyter** (Microsoft) - Ermöglicht das Arbeiten mit Jupyter Notebooks direkt in VS Code.
- **Even Better TOML** (tamasfe) - Verbessert die Bearbeitung von TOML-Dateien.
- **Ruff** (Astral Software) - Ein schneller Linter für Python, der dir hilft, sauberen Code zu schreiben.
- **Material Icon Theme** (PKief) - Verbessert die Dateisymbole in VS Code für eine bessere Übersicht.

Dafür kannst du den Erweiterungs-Tab in VS Code öffnen (Symbol mit den vier Quadraten auf der linken Seitenleiste) und in die Suchleiste `@recommended` eingeben. Danach sollten dir die empfohlenen Erweiterungen angezeigt werden.

### Notebooks ausführen
Im Ordner `notebooks/` findest du ein Jupyter Notebook namens `01_exploration.ipynb`, das als Ausgangspunkt für deine Datenanalyse dient. Öffne das Notebook in VS Code und wähle oben rechts dein virtuelles Environment als Kernel aus. Führe die Zellen nacheinander aus. Wenn alles geklappt hat wird das Notebook einen Datensatz von Kaggle laden und im Ordner `data/` speichern.

Von hier an kannst du mit deinem Projekt starten und die Vorlagen nach belieben anpassen.

Schaue dir für weitere Informationen zum Template die Datei [docs/project.md](./docs/project.md) an.


Für dein Projekt kannst du die folgenden Abschnitte in der `README.md` Datei anpassen, um dein Projekt zu beschreiben und zu präsentieren. Lösche anschließend diese Anleitung.

---

# Amazon Insight Engine: Globale Customer Experience Analyse 🚀

> **Data Science Case Study:** Analyse von 1,2M+ Kundenrezensionen zur Identifikation geschäftskritischer Treiber für Zufriedenheit und Umsatzoptimierung.

---

## 📌 Inhaltsverzeichnis
* [Projektübersicht](#-projektübersicht)
* [Zentrale Business-Fragen](#-zentrale-business-fragen)
* [Datensatz-Beschreibung](#-datensatz-beschreibung)
* [Projekt-Workflow](#-projekt-workflow)
* [Technologie-Stack](#-technologien)

---

## 📊 Projektübersicht

**Problemstellung:** Unternehmen verlieren signifikante Umsatzanteile durch unerkannte Muster in negativen Bewertungen. Die Herausforderung liegt in der Skalierbarkeit der Analyse über mehrsprachige Märkte hinweg.

**Ziel:** Entwicklung eines Frameworks zur Identifikation von **Risikozonen** und zur prädiktiven Vorhersage negativer Kundenerfahrungen mittels NLP und Machine Learning.

### 🛠 Technologien
* **Core:** `Pandas`, `NumPy`
* **Viz:** `Seaborn`, `Plotly`, `Matplotlib`
* **NLP:** `NLTK` / `Spacy` (Tokenisierung, N-Grams, Stopword-Removal)
* **ML:** `Scikit-learn` (Logistic Regression, Metric Evaluation)

---

## 💡 Zentrale Business-Fragen

1. **Risikozonen:** Welche Kategorien haben die höchste Negativ-Konzentration?
2. **Psychologie:** Korreliert die `review_length` mit extremen Sternebewertungen?
3. **Lokalisierung:** Wie unterscheidet sich der NPS (Net Promoter Score) zwischen Regionen (DE, US, JP)?
4. **Semantik:** Welche Begriffe sind die stärksten Prädiktoren für Churn/Unzufriedenheit?
5. **Prediction:** Wie präzise lassen sich negative Erfahrungen vorab klassifizieren?

---

## ⚙️ Projekt-Workflow

### Phase 1: Daten-Audit & Performance-Optimierung
* **Konsolidierung:** Merge von Train/Test/Validation zu einem Master-Dataset (1.2M+ Zeilen).
* **Memory Management:** Downcasting von Datentypen (`int8`, `category`) zur Reduktion des RAM-Verbrauchs um bis zu 70%.
* **Cleaning:** Behandlung von NaNs und technischen Artefakten.

### Phase 2: Explorative Datenanalyse (EDA)
* **Benchmark:** Visualisierung von Performance-Gaps zwischen Kategorien.
* **Global Sentiment:** Cross-Market Analyse der Kundenzufriedenheit.
* **Statistik:** Korrelationsmatrix zwischen Metadaten und Ratings.

### Phase 3: Feature Engineering
* Generierung von Text-Metriken (Wortanzahl, Satzstruktur).
* **Target Labeling:** Transformation der Ratings in binäre Klassen (Positiv/Negativ).

### Phase 4: NLP & Semantic Mining
* Extraktion von Schmerzpunkten mittels **N-Gram-Analyse**.
* Visuelle Identifikation von Treibern via WordClouds.

### Phase 5: Predictive Modeling & Action Plan
* Training einer Logistischen Regression.
* Ableitung von Strategien zur Steigerung der Conversion-Rate.

---

## 📂 Datensatz (Data Dictionary)
* **Quelle:** The Multilingual Amazon Reviews Corpus
* **Umfang:** 1.264.107 Rezensionen
* **Märkte:** DE, EN, FR, ES, IT, JP
* **Features:** `stars`, `review_body`, `review_title`, `product_category`, `language`


## Ergebnisse & Business Insights 📈

## Setup

Klone das Repository
```bash
# Repository klonen
git clone [DEIN-REPO-LINK]
cd [REPO-NAME]
```

Installiere [uv](https://uv.dev) (falls noch nicht installiert) und synchronisiere die Abhängigkeiten
```bash
# Dependencies installieren
uv sync
```

### Ausführung

Notebooks in dieser Reihenfolge ausführen:
1. notebooks/01_exploration.ipynb
<!--
2. notebooks/02_preprocessing.ipynb
3. notebooks/03_modeling.ipynb
4. notebooks/04_results.ipynb
-->


