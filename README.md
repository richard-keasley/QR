# class.QR

This was forked from [https://github.com/kevin-toscani/QR]

Added more options

- colours applies to HTML and image
- HTML output is grid (not table)
- pixel_size and padding apply to HTML and image outputs
- debug mode outputs HTML if image is requested
- colours are now stored in an array

## colours array
Each colour is stored as array [R, G, B]

- [0...3] are the three states of a cell (background, foreground, etc).
- ['_'] is the colour used for cell value "null"

## Example usage:

```
<?php
require_once 'class.QR.php';

$code = filter_input(INPUT_GET, 'code');
$string = "{your url}?code=$code";

$img = new QR($string, 'L');
//$img->set_debug_mode(1);
$img->pixel_size = 1;
$img->padding = 0;
$img->colours[1] = [80, 30, 30];
$img->return_image(); 
```