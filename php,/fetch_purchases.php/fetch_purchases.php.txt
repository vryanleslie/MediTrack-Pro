<?php
include('db.php');

$sql = "SELECT * FROM purchases";
$result = $conn->query($sql);

$purchases = [];
while ($row = $result->fetch_assoc()) {
    $purchases[] = $row;
}

echo json_encode($purchases);
?>
