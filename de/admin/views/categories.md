<a name="top"></a>
# Kategorien

Hier erhalten Sie Informationen über die Ansicht für Kategorien.

### Inhalt
1. [Anlegen einer neuen Kategorie](#categories_1)
2. [Kategorieeinstellungen](#categories_2)  
  	2.1 [Name und Beschreibung](#categories_2_1)  
	2.2 [Erlaubte Dateitypen](#categories_2_2)    
	2.3 [Vererbung von erlaubten Dateitypen](#categories_2_3)  
	2.4 [Veröffentlichung von Dokumenten](#categories_2_4)    
	2.5 [Grundsätzliche Lese-, und Verwaltungsrechte](#categories_2_5)      
	2.6 [Sonstige Einstellungen](#categories_2_6)    
3. [Bearbeitung einer Kategorie](#categories_3)  
	3.1 [Mehrere Datensätze bearbeiten](#categories_3_1)  
4. [Verschieben einer Kategorie](#categories_4)
5. [Löschen einer Kategorie](#categories_5)


----------

<a name="categories_1"></a>
## 1. Anlegen einer neuen Kategorie

Im Modul DMS → Kategorien

![Screenshot Backend Menü](../screenshot_backend_menu.png)

→ "Neue Kategorie“ anlegen

![Screenshot Neue Kategorie anlegen](screenshot_categories_new_category.png)


→ Kategorie mittels Einfügesysmbol an gewünschte Stelle einfügen:

**Folgende Abb.:** Anlage der allerersten Kategorie
![Screenshot Kategorie einfügen](screenshot_categories_insert_first.png)

**Folgende Abb.:** Anlage einer beliebigen weiteren Kategorie auf gleicher Ebene
![Screenshot Kategorie einfügen auf gleicher Ebene](screenshot_categories_insert_same_level.png)

**Folgende Abb.:** Anlage einer weiteren Kategorie als Unterebene
![Screenshot Kategorie einfügen als Unterebene](/manual/de/admin/views/screenshot_categories_insert_second_level.png)

----------

[Seitenanfang](#top)

<a name="categories_2"></a>
## 2. Kategorieeinstellungen

<a name="categories_2_1"></a>
### 2.1 Name und Beschreibung

* **Name:** Kategoriename eintragen (Pflichtfeld)
* **Beschreibung:** Beschreibung der Kategorie angeben (Angabe ist optional)

![Screenshot Kategorie Name und Beschreibung eingeben](screenshot_categories_config_name_and_description.png)

<a name="categories_2_2"></a>
### 2.2 Erlaubte Dateitypen

* **Erlaubte Dateitypen:** Sie können erlaubte Dateitypen für eine Kategorie manuell festlegen oder durch Auswahl von Dateityp-Sets. Eine Kombination ist ebenfalls möglich.

* **Manuell:** Geben Sie durch Komma getrennt die Dateitypen an, für die ein Upload gestattet sind. Die Liste wird beim Speichern automatisch sortiert und alle Dateitypen werden in Kleinbuchstaben konvertiert.

![Screenshot Dateityp-Sets konfigurieren](screenshot_categories_config_file_type_sets.png)

<a name="categories_2_3"></a>
### 2.3 Vererbung von erlaubten Dateitypen

* **Vererbung der erlaubten Dateitypen:** Geben Sie an, ob die erlaubten Dateitypen auch von den Oberkategorie(n) geerbt werden sollen.

**Beispiel**: Sie haben eine Kategorie "Obst" und legen für diese erlaubte Dateitypen fest. Dann erstellen sie für "Obst" eine neue Unterkategorie z.B. "Kernobst". 
Wenn sie nun für die Kategorie "Kernobst" das Häkchen bei *Vererbung der erlaubten Dateitypen* setzen, vererbt die Oberkategorie "Obst" die erlaubten Dateitypen an die Unterkategorie "Kernobst" weiter. 
Sie können für die Unterkategorie natürlich separat noch weitere erlaubte Dateitypen hinzufügen (entweder manuell oder über die Dateityp-Set Auswahl)


**Wurden Dateityp-Sets angelegt stehen diese ebenfalls zur Auswahl:**

* **Erlaubte Dateityp-Sets:** Häkchen setzen welche Dateitypen in dieser Kategorie erlaubt sind. Man kann das vorherige Feld *Erlaubte Dateitypen* frei lassen, wenn man nur mit Sets arbeiten möchte.

![Screenshot Dateityp-Sets benutzen](screenshot_categories_config_file_type_sets_2.png)


----------

<a name="categories_2_4"></a>
### 2.4 Veröffentlichung von Dokumenten

* **Standardmäßige Veröffentlichung:** Geben Sie an, ob die in diese Kategorie hochgeladenen Dokumente standardmäßig veröffentlicht werden sollen.

<a name="categories_2_5"></a>
## 2.5 Grundsätzliche Lese-, und Verwaltungsrechte

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


----------


<a name="categories_2_6"></a>
### 2.6 Sonstige Einstellungen

* **Experten-Einstellungen:** Stylesheets (CSS) - Falls gewünscht kann hier eine ID und / oder Klasse(n) eintragen werden
* **Kategorie veröffentlichen:** Checkbox aktiv = Kategorie wird im Frontend angezeigt
* **Anzeigen ab** und **Anzeigen bis:** Von welchem Tag an soll die Kategorie angezeigt werden? Und bis zu welchem Tag soll die Kategorie angezeigt werden.
Lassen Sie die Felder leer um die Kategorie direkt und unbegrenzt anzuzeigen

Folgende Abb.: So könnte eine Kategorieübersicht aussehen

![Screenshot Kategorieübersicht](screenshot_categories_list.png)

----------

[Seitenanfang](#top)

<a name="categories_3"></a>
## 3. Bearbeitung einer Kategorie

In der Kategorieübersicht klicken Sie auf das Stiftsymbol der entsprechenden Kategorie um zu den Einstellungen zu gelangen. (**Siehe oben:** [2. Kategorieeinstellungen](#categories_2))

![Screenshot Kategorie bearbeiten](screenshot_categories_edit.png)

<a name="categories_3_1"></a>
### 3.1 Mehrere Datensätze bearbeiten
Sie können auch über die Funktion *Mehrere bearbeiten* mehrere Datensätze auswählen um Einstellungen vorzunehmen. Die Funktion können sie auch für andere Aufgaben nutzen (Kategorien verschieben, löschen usw.) 

![Screenshot Mehrere Datensätze bearbeiten](/manual/de/admin/views/screenshot_multitask.png)

Wählen sie die zu bearbeitenden Kategorien und klicken unten auf *Bearbeiten*:

![Screenshot ausgewählte Datensätze](/manual/de/admin/views/screenshot_multitask_selectionpng.png)

Wählen sie die zu bearbeitenden Felder aus und klicken auf *Weiter*:
![Screenshot zu bearbeitende Felder auswählen.png](/manual/de/admin/views/screenshot_select_existing_fields.png)

Nun können sie die Einstellungen der gewählen Kategorien vornehmen.

**Speichern nicht vergessen**

----------

<a name="categories_4"></a>
## 4. Verschieben einer Kategorie

Kategorien lassen sich einfach über die Symbole *Verschieben* und *Einfügen* an eine andere Stelle verschieben

**Kategorie verschieben:** 
![Screenshot Kategorie verschieben](screenshot_categories_move.png)


**Kategorie einfügen:**
![Screenshot Kategorie einfügen nach verchieben](screenshot_categories_insert_after_moving.png)


----------

<a name="categories_5"></a>
## 5. Löschen einer Kategorie

Das Löschen einer Kategorie ist nur dann erlaubt, wenn sich **kein** Dokument in dieser Kategorie oder in einer ihrer Unterkategorien befindet.

![Screenshot Kategorie löschen](screenshot_categories_delete.png)


----------

[Seitenanfang](#top)