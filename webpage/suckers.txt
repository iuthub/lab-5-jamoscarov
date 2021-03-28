<?php
$name = $_REQUEST["name"];
$section = $_REQUEST["section"];
$cnumber = $_REQUEST["card_number"];
$ctype = $_REQUEST["card_type"];
?>


<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<!-- saved from url=(0075)http://www.webstepbook.com/supplements/labsection/lab4-buyagrade/sucker.php -->
<html xmlns="http://www.w3.org/1999/xhtml">
<head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <title>Buy Your Way to a Better Education!</title>
    <link href="./Buy Your Way to a Better Education!_files/buyagrade.css" type="text/css" rel="stylesheet">
</head>

<body>
<h1>Thanks, sucker!</h1>

<p>Your information has been recorded.</p>

<dl>
    <dt>Name</dt>
    <dd> <?= $name ?></dd>

    <dt>Section</dt>
    <dd><?= $section ?></dd>

    <dt>Credit Card</dt>
    <dd><?= $cnumber ."(". $ctype .")" ?></dd>
</dl>

<?php
$text = file_get_contents("sucker.php");
file_put_contents("suckers.txt", $text);
?>


</body></html>