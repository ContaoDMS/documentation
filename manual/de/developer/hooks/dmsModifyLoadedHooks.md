# "dmsModifyLoaded..."-Hooks

Die folgenden Hooks k�nnen verwendet werden um Objekte zu �ndern die vom `DmsLoader` geladen wurden.

## dmsModifyLoadedCategory

Der "dmsModifyLoadedCategory"-Hook wird zum �ndern von Kategorien nach dem Laden durch den `DmsLoader` ausgef�hrt. So k�nnen die Eigenschaften ver�ndert werden.
Er �bergibt `$category` (vorhandenee geladenes Objekt) und `$dbResultCategory` (das Datenbank-Ergebnis).
Er erwartet die ge�nderte Kategorie als R�ckgabewert.

*(seit Version 2.2.0)*


```php
// config.php

$GLOBALS['TL_HOOKS']['dmsModifyLoadedCategory'][] = array('MyDmsModificationClass', 'myDmsModifyLoadedCategory');

// MyDmsModificationClass.php

class MyDmsModificationClass
{
	public function myDmsModifyLoadedCategory(Category $category, Database_Result $dbResultCategory)
	{
		// do custom modification here
		return $category;
	}
}
```

## dmsModifyLoadedAccessRight

Der "dmsModifyLoadedAccessRight"-Hook wird zum �ndern von Zugriffsrechten nach dem Laden durch den `DmsLoader` ausgef�hrt. So k�nnen die Eigenschaften ver�ndert werden.
Er �bergibt `$accessRight` (vorhandenee geladenes Objekt) und `$dbResultAccessRight` (das Datenbank-Ergebnis).
Er erwartet das ge�nderte Zugriffsrecht als R�ckgabewert.

*(seit Version 2.2.0)*


```php
// config.php

$GLOBALS['TL_HOOKS']['dmsModifyLoadedAccessRight'][] = array('MyDmsModificationClass', 'myDmsModifyLoadedAccessRight');

// MyDmsModificationClass.php

class MyDmsModificationClass
{
	public function myDmsModifyLoadedAccessRight(AccessRight $accessRight, Database_Result $dbResultAccessRight)
	{
		// do custom modification here
		return $accessRight;
	}
}
```

## dmsModifyLoadedDocument

Der "dmsModifyLoadedDocument"-Hook wird zum �ndern von Dokumenten nach dem Laden durch den `DmsLoader` ausgef�hrt. So k�nnen die Eigenschaften ver�ndert werden.
Er �bergibt `$document` (vorhandenee geladenes Objekt) und `$dbResultDocument` (das Datenbank-Ergebnis).
Er erwartet das ge�nderte Dokument als R�ckgabewert.

*(seit Version 2.2.0)*


```php
// config.php

$GLOBALS['TL_HOOKS']['dmsModifyLoadedDocument'][] = array('MyDmsModificationClass', 'myDmsModifyLoadedDocument');

// MyDmsModificationClass.php

class MyDmsModificationClass
{
	public function myDmsModifyLoadedDocument(Document $document, Database_Result $dbResultDocument)
	{
		// do custom modification here
		return $document;
	}
}
```