# FluentSQL
**API para gerenciamento de conexoes e operações com o banco mySQL, usando design patters FluentAPI**
### Instalação
```
composer require rafaelssucupira/fluent-sql
```
### Exemplo
```
<?php
require_once ("vendor/autoload.php");
use FluentSQL\SQL;

$conn = new SQL( "localhost", "db", "user", "passwd", "username" ?? null );

$result = $conn
            ->prepareQuery( "SELECT * FROM users" )
            ->sqlCommand()
            ->execQuery()
            ->build(true);

echo json_encode($result)    ;

?>
```

