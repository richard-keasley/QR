# class.QR

This was forked from [https://github.com/kevin-toscani/QR]

Added more options

- colours applies to HTML and image
- HTML output is grid (not table)
- debug output is always HTML
- colours are now stored as array(0...3)

## Example usage:

require_once 'class.QR.php';

$code = filter_input(INPUT_GET, 'code');
$string = "{your url}?code=$code";

$img = new QR($string, 'L');
//$img->set_debug_mode(1);
$img->pixel_size = 1;
$img->padding = 0;
$img->colours[1] = [80, 30, 30];
$img->return_image(); 
 
