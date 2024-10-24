# PVA4 - Programování a vývoj aplikací
## Lekce 06: Funkce, Null, Require a Include

## Obsah

## Funkce
V souboru functions.php deklarujte funkce 

### 1
Deklarujte funkci celsiusToFahrenheit, která převede hodnotu zadanou v celsiích na fahrenheity. Funkce bude mít jeden vstupní parametr a výstupem bude převedená hodnota.

### 2
Deklarujte funkci pro nalezení maximální hodnoty v poli. Funkce bude mít jeden vstupní parametr typu pole a výstupem bude číslo označující maximální hodnota v poli.

Pro pole použijte hodnoty:
`39, 63, 32, 34, 38, 18, 87, 29, 87, 26, 32, 60, 8, 96, 99, 67, 5, 19, 22, 40, 32, 78, 54, 9, 85, 75, 26, 55, 11, 33, 68, 30, 25, 2, 68, 31, 9, 2, 48, 79, 99, 27, 53, 89, 62, 42, 36, 63, 7, 71`

### 3
Vytvořte funkci `jePrvocislo`, která zjistí, zda je číslo prvočíslem.

### 4
Ze vzorových hodnot pouze za využití funkcí, cyklu a podmínek vytvořte dvě pole,
a) první pole `prvocisla` obsahuje pouze prvočísla
b) druhé pole `pole` pouze ostatní hodnoty

### 5
Deklarujte funkci `jeSilneHeslo`, které bude dle aktuálních bezpečnostních best practise ověřovat, zda-li vstupní řetězec je silné heslo. Funkce bude mít jeden vstupní parametr a výstupem bude boolean hodnota.



## Require a Include
### 1. Index
1. Do souboru `index.php` integrujte obsahové soubory `templ_header` a `templ_footer` a "sestavte" výslednou webovou stránku.

### 2. Functions - showMenu
Práce v souboru `functions.php`, sekce `Functions`
1. Deklarujte funkci `showMenu`, která bude obsahovat menu aplikace. Pro vzhled menu využijte přiložený zdrojový kód.
2. Pomocí funkce showMenu zobrazte uživateli menu. 

```
<header class="masthead mb-auto">
    <div class="inner">
      <h3 class="masthead-brand">EduCover</h3>
      <nav class="nav nav-masthead justify-content-center">
        <a class="nav-link" href="#">Home</a>
        <a class="nav-link" href="#">About Me</a>
        <a class="nav-link" href="#">Contact</a>
      </nav>
    </div>
  </header>
```

### 3. Config
1. V souboru `config` deklarujte proměnnou `author` s Vaším jménem.
2. Upravte hlavičku html stránky a zobrazte v meta tagu Vaše jméno za využití hodnoty z souboru `config`.

### 4. Functions - showAuthor
1. Deklarujte funkci `showAuthor`. Funkce bude mít vstupní parametr name. Vstupní parametr bude proměnná author z souboru `config` a `rok`. 
 
    Výstup fce bude odpovídat tvaru `used by _author_, PVA4 _rok_` např. `used by Adam Fišer, PVA4 2021`.
2. Funkci použijte k zobrazení v souboru `templ_footer` namísto komentáře `<!-- here -->`. 

 

### 5. Menu
Upravte funkci `showMenu` využtím cyklu tak, aby položky byly automaticky generovány dle hodnot pole.  
Klíč pole odkazuje na cílovou stránku a hodnota prvku pole se bude zobrazovat uživateli. 

Deklarace pole:
```
$aMenu = array(
                "about_me" => "About me",
                "contact"  => "Contact",
                "hobbies"  => "Hobbies",
                "school"   => "School"
                "work"     => "My work"
                "photos"   => "Photos"
                );
```

### 5. Označení aktuální stránky
Upravte funkci menu způsobem, aby byla označena aktivní položka menu. Aktivní položku nastavíte css styl `active`. Ostatní položky je mít nebudou.

Aktivní položka menu je určena prostřednictvím parametru 'page' přicházející z URL. Hodnota odpovídá klíči pole.

Například pro hodnotu `...?active=hobbies` zobrazíte jako aktivní menu Hobbies.
