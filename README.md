Prueba

```php
<?php 
    include 'broker.php';

    class brokerTest extends PHPUnit_Framework_TestCase
    {
        public function testSuccess()
        {
            $broker = new broker;

            $this->assertEquals(
                '<xml><xmlOrden>xmlOrden</xmlOrden><provision>workorder</provision><operacion>cancelworkorder</operacion><metodo>CancelWorkOrder</metodo><version>3.0.0.0</version></xml>',
                $broker->CancelWorkOrder('xmlOrde')
            );
        }
    }    

 ?>

```

Pass

```php
phpunit brokerTest.php
PHPUnit 3.7.21 by Sebastian Bergmann.

.

Time: 0 seconds, Memory: 1.75Mb

OK (1 test, 1 assertion)
```

Fail

```php
phpunit brokerTest.php
PHPUnit 3.7.21 by Sebastian Bergmann.

F

Time: 0 seconds, Memory: 1.75Mb

There was 1 failure:

1) brokerTest::testSuccess
Failed asserting that two strings are equal.
--- Expected
+++ Actual
@@ @@
-'<xml><xmlOrden>xmlOrden</xmlOrden><provision>workorder</provision><operacion>cancelworkorder</operacion><metodo>CancelWorkOrder</metodo><version>3.0.0.0</version></xml>'
+'<xml><xmlOrden>xmlOrde</xmlOrden><provision>workorder</provision><operacion>cancelworkorder</operacion><metodo>CancelWorkOrder</metodo><version>3.0.0.0</version></xml>'

C:\Users\j.sandoval\Desktop\pruebas\brokerTest.php:13

FAILURES!
Tests: 1, Assertions: 1, Failures: 1.
```
