# lab1<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<form name="lab"  action="lab%201.php" method="post">
    <b>Введите сумму:</b><br>
    <input type="number" size="20" required pattern="^[ 0-9]+$">
    <p>
        <select size="6" required multiple name = "val">
            <option disabled>Выбирите валюту</option>
            <option value="UAH">UAH</option>
            <option value="RUB">RUB</option>
            <option value="BYN">BYN</option>
            <option value="EUR">EUR</option>
            <option value="USD">USD</option>
        </select></p>
    <p> <input type="submit" value ="посчитать" name = "money">
    </p>
</form>
</body>
</html>
<?php
$value = $_POST['value'];
$con = $_POST['money'];
if($value == "UAH")
{
    $den = $con * 1;
}
if($value == "RUB")
{
    $den = $con * 0.41;
}
if($value == "BYN")
{
    $den = $con * 1.119;
}
if($value == "EUR")
{
    $den = $con * 27.66;
}
if($value == "USD")
{
    $den = $con * 25.08;
}
echo $den;

?>

