# Bench - A single-method PHP 5.3+ benchmarking utility

* Copyright: (c) 2012 Johnny Broadway
* License: http://www.opensource.org/licenses/mit-license.php

Keep track of milliseconds passed and memory usage throughout
a script's execution. Simply call `Bench::mark()` at the end
of each step (with an optional note), then call it again at
the end passing a true boolean to have it print the output.
If you also set `$raw` to true, it will output the memory
without rounding to KB.
    
### Usage:

```php
<?php

// start benchmarking:
require 'Bench.php';
Bench::mark ('start');

// perform some logic here

Bench::mark ('notes...');

// perform some more logic

Bench::mark ('next marker');

// output the results:
Bench::mark (true);

?>
```
