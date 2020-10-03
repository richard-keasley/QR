# class.QR

This was forked from [https://github.com/kevin-toscani/QR]

Added more options

- colours applies to HTML and image
- HTML output is grid (not table)
- pixel_size and padding apply to HTML and image outputs
- debug mode outputs HTML if image is requested
- colours are now stored in an array

### colours array
Each colour is stored as array \[R, G, B]

- [0...3] are the three states of a cell (empty, filled, etc).
- ['\_'] is the colour used for cell value "null"

## Example usage:

```php
<?php
require_once 'class.QR.php';

$string = "Hello world";

$obj = new QR($string, 'L'); // create object(string, error correction, mode)
//$obj->set_debug_mode(1); // debug shows log after output
$obj->pixel_size = 1; // size of cells
$obj->padding = 0; // number of padding cells 
$obj->colours[0] = [200, 200, 200]; // colour of empty (background) cells [R, G, B]
$obj->colours[1] = [80, 30, 30]; // colour of filled cells [R, G, B]
$obj->return_image(); // output
```
