# PhpMigration
Migration Library for PHP

This project requires [PhpSanitization](https://github.com/fariscode511/PhpSanitization)

## How to use

```php
include_once 'config.php';
include_once 'Database.php';
include_once 'Sanitization.php';
include_once 'Migration.php';


$db = new Database();
$sanitize = new Sanitization();
$migrate = new Migration($db, $sanitize);


// Create Table

$migrate->createTable("users", [['id', 'int', 'unsigned', 'not null']]);

// Make it a primary key

$migrate->isPrimary("users", "id");
```

## Copyright
FarisCode
