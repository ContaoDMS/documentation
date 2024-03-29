# Kategorien

**Seiteninhalt**

1. [Kategorien im ContaoDMS](#kategorien-im-contaodms)
2. [Kategorietiefe](#kategorietiefe)
3. [Kategoriebilder](#kategoriebilder)
4. [Anlegen einer neuen Kategorie](#anlegen-einer-neuen-kategorie)
5. [Kategorie-Einstellungen](#kategorie-einstellungen)
6. [Erlaubte Dateitypen](#erlaubte-dateitypen)
7. [Vererbung von erlaubten Dateitypen](#vererbung-von-erlaubten-dateitypen)
8. [Veröffentlichung von Dokumenten](#veröffentlichung-von-dokumenten)
9. [Grundsätzliche Lese und Verwaltungsrechte](#grundsätzliche-lese-und-verwaltungsrechte)
10. [Bearbeitung einer Kategorie](#bearbeitung-einer-kategorie)
11. [Mehrere Datensätze bearbeiten](#mehrere-datensätze-bearbeiten)
12. [Verschieben einer Kategorie](#verschieben-einer-kategorie)
13. [Löschen einer Kategorie](#löschen-einer-kategorie)

---

## Kategorien im ContaoDMS

* Kategorien sind die Orte, in welchen die Dokumente später aufbewahrt werden.
* Jedes Dokument wird genau einer Kategorie zugeordnet. Daher ist es wichtig, sich im Vorfeld eine sinnvolle Struktur zu überlegen.
* Eine weitere wichtige Überlegung sollte sein, welche Dokumente die einzelnen Mitglieder später zu sehen bekommen sollen.
* Grundsätzlich ist zu entscheiden ob Dokumente von:
  *  allen Nutzern der Website (auch nicht angemeldeten)
  *  nur von angemeldeten Mitgliedern
  *  oder nur von Mitgliedern spezieller Mitgliedergruppen gelesen werden dürfen.
* Es besteht also ein Zusammenspiel von **Kategorien** und **Zugriffsrechten**
* Jede Kategorie benötigt einen aussagefähigen **Namen** und eine möglichst ausführliche aber nicht zu lange **Beschreibung**
* Der Name und die Beschreibung werden später im Frontend angezeigt

**So könnte eine Kategorieübersicht im Backend aussehen:**

![Kategorieübersicht](categories_overview.png)

## Kategorietiefe

Es ist maximal ein 4-stufiger Kategorieaufbau zulässig. Das sollte eigentlich für jeden Anwendungszweck ausreichen.

<pre>
  Hauptkategorie
   --> 1. Unterkategorie
    ---> 2. Unterkategorie
     ----> 3. Unterkategorie
      -----> 4. Unterkategorie
</pre>

## Kategoriebilder

* Jeder Kategorie kann genau ein Bild zugewiesen werden (z.B. als Vorschaubild)
* Diese Bild muss in der Contao-Dateiverwaltung hochgeladen werden

## Anlegen einer neuen Kategorie

→ im Modul DMS → Kategorien

![DMS Backend Menü](backend_categories.png)

→ **Neue Kategorie** anlegen (im Beispiel wird das die Kategorie **Buchhaltung** sein)

![Kategorie einfügen](categories_new_category.png)

→ Kategorie mittels Einfügesysmbol an gewünschte Stelle einfügen. 

**Note:** Im folgenden Beispiel ist noch keine Kategorie vorhanden. Die erste Kategorie kann also nur an eine Stelle eingefügt werden.

![Kategorie auf Hauptebene anlegen](categories_insert_first_level.png)

---

Anlage einer weiteren Kategorie **"Kontakte"** auf der Hauptebene also auf gleicher Ebene wie die Kategorie **"Buchhaltung"**:

![Kategorie einfügen auf gleicher Ebene](categories_insert_same_level.png)

Die Kategorie **"Buchhaltung"** und die Kategorie **"Kontakte"** auf der Hauptebene:

![Kategorie Buchhaltung und Kontakte auf gleicher Ebene](categories_same_level.png)

---

Anlage einer Kategorie **"Steuer"** als Unterebene von **"Buchhaltung"**:

![Kategorie einfügen als Unterebene](categories_insert_second_level.png)

Kategorie **"Buchhaltung"** als Hauptebene und Kategorie **"Steuer"** als Unterebene:

![Kategorien auf zwei Ebenen](categories_two_levels.png)

---

## Kategorie-Einstellungen

### Name und Beschreibung

* **Name:** Kategoriename eintragen (*Pflichtfeld)
* **Beschreibung:** Beschreibung der Kategorie angeben (Angabe ist optional)

![Kategorie Name und Beschreibung eingeben](categories_config_name_and_description.png)


### Erlaubte Dateitypen

**Erlaubte Dateitypen:** 
* Sie können erlaubte Dateitypen für eine Kategorie manuell festlegen oder falls angelegt durch Auswahl von **Dateityp-Sets**. 
* Eine Kombination ist ebenfalls möglich.

**Manuell:** 
* Geben Sie einen Dateityp oder durch Komma getrennt mehrere Dateitypen an, für die ein Upload gestattet sind. 
* Die Liste wird beim Speichern automatisch sortiert und alle Dateitypen werden in Kleinbuchstaben konvertiert.

![Dateityp-Sets konfigurieren](categories_config_file_type_sets.png)


**Dateityp-Sets verwenden:**

 * **Erlaubte Dateityp-Sets:** Häkchen setzen für Dateitypen die in dieser Kategorie erlaubt sind. 
 * Sie können das vorherige Feld *Erlaubte Dateitypen* frei lassen, wenn Sie nur mit Sets arbeiten möchten.

![Dateityp-Sets benutzen](categories_config_file_type_sets_2.png)


### Vererbung von erlaubten Dateitypen

**Vererbung der erlaubten Dateitypen:** 
* Geben Sie an, ob die erlaubten Dateitypen auch von den Oberkategorie(n) geerbt werden sollen.

![Dateityp-Sets vererben](categories_inheritance.png)

**Beispiel**:

* Sie haben für die Hauptkategorie **"Buchhaltung"** die erlaubte Dateitypen **doc, docx und pdf** festgelegt.
* Dann erstellen sie für **"Buchhaltung"** eine neue Unterkategorie z.B. **"Steuer"**.
* Wenn sie nun für die Kategorie **"Steuer"** das Häkchen bei *Vererbung der erlaubten Dateitypen* setzen, vererbt die Hauptkategorie **"Buchhaltung"** die erlaubten Dateitypen an die Unterkategorie **"Steuer"** weiter. 
* Somit hat die Unterkategorie **"Steuer"** ebenfalls die erlaubten Dateitypen **doc, docx und pdf**
* Sie können für die Unterkategorie natürlich separat noch weitere erlaubte Dateitypen hinzufügen (entweder manuell oder über die Dateityp-Set Auswahl)


### Veröffentlichung von Dokumenten

* **Standardmäßige Veröffentlichung:** Geben Sie an, ob die in diese Kategorie hochgeladenen Dokumente standardmäßig veröffentlicht werden sollen.

## Grundsätzliche Lese und Verwaltungsrechte

### Grundsätzliches Leserecht  

Geben Sie das grundsätzliche Leserecht für Dokumente dieser Kategorie an.  

* **Leserecht für alle Mitglieder:** Alle Mitglieder haben uneingeschränktes Leserecht in dieser Kategorie. Sie müssen dazu nicht angemeldet sein.
* **Leserecht für angemeldete Mitglieder:**  Nur angemeldete Mitglieder haben uneingeschränktes Leserecht in dieser Kategorie.
* **Spezielle Leserechte für einzelne Mitgliedergruppen:** Es werden für diese Kategorie spezielle Leserechte für einzelne Mitgliedergruppen vergeben (im Bereich Zugriffsrechte).
* **Vererbung der Leserechte durch Oberkategorie(n):** Es werden für diese Kategorie die Leserechte der Oberkategorie(n) verwendet.

### Grundsätzliche Verwaltungsrechte

Geben Sie die grundsätzlichen Verwaltungsrechte für Dokumente dieser Kategorie an.  

* **Alle Verwaltungsrechte für angemeldete Mitglieder**
* **Spezielle Verwaltungsrechte für einzelne Mitgliedergruppen**
* **Vererbung der Verwaltungsrechte durch Oberkategorie(n)**


### Sonstige Einstellungen

* **Experten-Einstellungen:** Stylesheets (CSS) - Falls gewünscht kann hier eine ID und / oder Klasse(n) eintragen werden
* **Kategorie veröffentlichen:** Checkbox aktiv = Kategorie wird im Frontend angezeigt
* **Anzeigen ab** und **Anzeigen bis:** Von welchem Tag an soll die Kategorie angezeigt werden? Und bis zu welchem Tag soll die Kategorie angezeigt werden.
Lassen Sie die Felder leer um die Kategorie direkt und unbegrenzt anzuzeigen


## Bearbeitung einer Kategorie

Sie haben die Möglichkeit, einzelne Kategorien zu bearbeiten oder mehrere Kategorien auszuwählen, um gemeinsame Einstellungen vorzunehmen.

* In der Kategorieübersicht klicken Sie auf das **Stiftsymbol** der entsprechenden Kategorie um zu den Einstellungen zu gelangen. 
* **Siehe oben:** [Kategorieeinstellungen](#kategorieeinstellungen)

![Kategorie bearbeiten](categories_edit.png)


### Mehrere Datensätze bearbeiten

* Über die Funktion **Mehrere bearbeiten** können Sie mehrere Datensätze auswählen um Einstellungen vorzunehmen.

**Tip:** Die Funktion kann auch für andere Aufgaben genutzt werden (Kategorien verschieben, löschen usw.) 

![Mehrere Datensätze bearbeiten](categories_multitask.png)

Wählen Sie die zu bearbeitenden Kategorien und klicken unten auf **Bearbeiten**:

![Ausgewählte Datensätze](categories_multitask_selection.png)

Wählen Sie die zu bearbeitenden Felder aus und klicken auf **Weiter**:

![Zu bearbeitende Felder auswählen](categories_select_existing_fields.png)

Nun können Sie die Einstellungen der gewählten Kategorien vornehmen.

---

### Verschieben einer Kategorie

Kategorien lassen sich einfach über die Symbole **Verschieben** und **Einfügen** an eine andere Stelle verschieben:

![Kategorie verschieben](categories_move.png)

---

### Kategorie einfügen

![Kategorie einfügen nach verschieben](categories_insert_after_moving.png)

---

### Löschen einer Kategorie

**Note:** Das Löschen einer Kategorie ist nur dann erlaubt, wenn sich **kein** Dokument in dieser Kategorie oder in einer ihrer Unterkategorien befindet.

![Kategorie löschen](categories_delete.png)
