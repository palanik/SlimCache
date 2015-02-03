SlimAPCCache
============

Cache Middleware for PHP [Slim micro framework](http://www.slimframework.com/) using [apccache](http://www.php.net/manual/en/book.apc.php)

##How to Use this Middleware
```php
<?php
$app = new \Slim\Slim();

use palanik\slimapccache\SlimApcCache;

$app->add($app->add(new SlimApcCache(array(
			'ttl' => 60,
			'caching_prefix' => 'myapp_',
			)));
			
$app->get('/foo', function () use ($app) {
    echo "Hello";
});
$app->run();
?>
```
