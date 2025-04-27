<?php
include('db.php');

$sql = "SELECT * FROM sales";
$result = $conn->query($sql);

$sales = [];
while ($row = $result->fetch_assoc()) {
    $sales[] = $row;
}

echo json_encode($sales);
?>
