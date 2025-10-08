# PVA4 - Programování a vývoj aplikací
## Cvičení 06: Require a Include

## Obsah

Pro vypracování cvičení využijte vyhotovené soubory z předchozího cvičení s formuláři.

Upravte strukturu projektu s využitím funkcí include/require a optimální struktury.

### Konfigurační soubor

- V konfiguračním souboru `config.php` budou deklarovány všechny globální proměnné, které se budou využívat v aplikaci. Deklarujte proměnnou/konstantu
  - `author` s Vaším jménem.
  - `APP_VERSION` s hodnotou `1.0.1`
  - `projectName` s názvem Vašeho projektu (může být fiktivní)

### Funkce
- V souboru `functions.php` budou deklarovány všechny funkce, které se budou využívat v aplikaci.

### Šablony
- V adresáři `templates` budou umístěny všechny šablony, které se budou využívat v aplikaci.
  - `header.php` - hlavička webové stránky
  - `footer.php` - patička webové stránky
  - `menu.php` - menu webové stránky

### Common
- Umístěte soubor `common.php`, který bude obsahovat společné nastavení aplikace.

### Menu
- Do menu přidejte položky menu na jednotlivé stránky formulářů, které jste vytvořili v předchozím cvičení.
- Aktivní stránka bude označena pomocí css třídy `active`.

### Patička
- Do patičky přidejte text `&copy; ROK author - projectName - verze APP_VERSION`, kde `author`, `projectName` a `APP_VERSION` budou nahrazeny hodnotami z konfiguračního souboru.

### Výstup formuláře
- Po odeslání formuláře zobrazte potvrzující zprávu o úspěšném odeslání formuláře.
```html
<div class="alert alert-success alert-dismissible">
  <button type="button" class="close" data-dismiss="alert" aria-hidden="true">×</button>
  <h5><i class="icon fas fa-check"></i> Alert!</h5>
  Success alert preview. This alert is dismissable.
</div>
```

- Výstup formuláře naformátujte pomocí popisného seznamu [description list](https://adminlte.io/themes/v3/pages/UI/general.html). Pozor na správné použití css tříd pro horizontální zobrazení a sloupcový layout.

```html
...
<div class="col-md-6">
    <div class="card">
      <div class="card-header">
        <h3 class="card-title">
          <i class="fas fa-text-width"></i>
          Description Horizontal
        </h3>
      </div>
      <!-- /.card-header -->
      <div class="card-body">
        <dl class="row">
          <dt class="col-sm-4">Description lists</dt>
          <dd class="col-sm-8">A description list is perfect for defining terms.</dd>
          <dt class="col-sm-4">Euismod</dt>
          <dd class="col-sm-8">Vestibulum id ligula porta felis euismod semper eget lacinia odio sem nec elit.</dd>
          <dd class="col-sm-8 offset-sm-4">Donec id elit non mi porta gravida at eget metus.</dd>
          <dt class="col-sm-4">Malesuada porta</dt>
          <dd class="col-sm-8">Etiam porta sem malesuada magna mollis euismod.</dd>
          <dt class="col-sm-4">Felis euismod semper eget lacinia</dt>
          <dd class="col-sm-8">Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo
            sit amet risus.
          </dd>
        </dl>
      </div>
      <!-- /.card-body -->
    </div>
    <!-- /.card -->
  </div>
```
