# PhpMigration

Migration Library for PHP

## How to use

```php

include_once 'config.php';
include_once 'Database.php';
include_once 'Utils.php';
include_once 'Options/Options.php';
include_once 'Options/Types.php';
include_once 'Migration.php';

$db = new Database($config);
$utils = new Utils();
$migrate = new Migration($db, $utils);

// Create Table

$migrate->createTable("users", [
    [
        'id',
        Types::Integer(),
        Options::UnSigned(),
        Options::NotNull()
    ]
]);

// Create a primary key

$migrate->isPrimary("users", "id"); 

```

## Copyright

FarisCode
