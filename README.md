# QGIS Plugin Repository

Prywatne repozytorium wtyczek QGIS hostowane na GitHub Pages.

## Dla administratora — jak uruchomić

### 1. Utwórz repozytorium na GitHub

- Wejdź na https://github.com/new
- Nazwa: `qgis-plugin-repo`
- Ustaw jako **Private** (tylko zaproszeni mają dostęp)
- Kliknij "Create repository"

### 2. Wrzuć pliki

```bash
cd qgis-plugin-repo
git init
git add .
git commit -m "Pierwsze repozytorium wtyczek"
git branch -M main
git remote add origin https://github.com/TWOJ-USERNAME/qgis-plugin-repo.git
git push -u origin main
```

### 3. Włącz GitHub Pages

- Wejdź w Settings → Pages
- Source: **Deploy from a branch**
- Branch: **main**, folder: **/ (root)**
- Kliknij Save
- Po chwili strona będzie dostępna pod: `https://TWOJ-USERNAME.github.io/qgis-plugin-repo/`

### 4. Zaktualizuj URLe w plugins.xml

Zamień wszędzie `TWOJ-USERNAME` na swoją nazwę użytkownika GitHub.

### 5. Dodaj członków zespołu

- Settings → Collaborators → Add people
- Dodaj osoby które mają mieć dostęp

## Dla użytkowników — jak zainstalować wtyczkę

### 1. Dodaj repozytorium w QGIS

- Otwórz QGIS
- Menu: **Wtyczki** → **Zarządzaj i instaluj wtyczki...**
- Kliknij zakładkę **Ustawienia**
- Na dole w sekcji "Repozytoria wtyczek" kliknij **Dodaj...**
- Wypełnij:
  - **Nazwa:** Nasze wtyczki
  - **URL:** `https://TWOJ-USERNAME.github.io/qgis-plugin-repo/plugins.xml`
- Kliknij OK

### 2. Zainstaluj wtyczkę

- Przejdź do zakładki **Wszystkie**
- Wyszukaj "Polska Mapa OSM"
- Kliknij **Zainstaluj wtyczkę**

Od teraz QGIS będzie automatycznie sprawdzał aktualizacje z tego repozytorium.

## Jak dodać nową wtyczkę

1. Wrzuć plik `.zip` do folderu `plugins/`
2. Dodaj wpis w `plugins.xml` (skopiuj istniejący blok `<pyqgis_plugin>` i zmień dane)
3. Commit i push — GitHub Pages zaktualizuje się automatycznie

## Jak zaktualizować istniejącą wtyczkę

1. Podmień plik `.zip` w `plugins/`
2. W `plugins.xml` zmień `version` i `update_date`
3. Commit i push
