# class.QR

## Example usage:

```<?php include('class.QR.php');

$string = "De tijd met mij vergeten bent. Tot blauwer dan blauw als ze lacht. Zeg mij maar wie wie wie wie wie heeft het gedaan.";

$ob_qr = new QR($string, 'M');

?><!doctype html>
<html>
<head><style>
	table { margin: 100px; border-collapse: collapse; }
	td { width: 5px; height: 5px; } 
	.td { background-color: #ddd; }
	.m0 { background-color: #fff; }
	.m1 { background-color: #000; }
	.m2 { background-color: #f09; }
	.m3 { background-color: #ff0; }
</style></head>
<body><?php echo $ob_qr->return_html(); ?></body>
</html>```