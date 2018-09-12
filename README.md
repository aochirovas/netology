# netology
Homeworks for Netology

<?php
try
{
$pdo=new PDO("mysql:host=localhost;dbname=global,charset=utf8","aochirova","neto1829");
$sth=$pdo->prepare("SELECT*FROM books");
$sth->execute();
$result=$sth->fetchALL(PDO::FETCH_ASSOC);
print_r($result);
}
catch(PDOException $e)
{
	die("Error: ".$e->getMessage());
}
?>
