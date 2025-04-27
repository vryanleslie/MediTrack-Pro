<?php
include('db.php');

if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $product_id = $_POST['product_id'];
    $quantity = $_POST['quantity'];
    $date = $_POST['date'];

    $sql = "INSERT INTO sales (product_id, quantity, date) VALUES ('$product_id', '$quantity', '$date')";
    
    if ($conn->query($sql) === TRUE) {
        echo "New sale added successfully";
    } else {
        echo "Error: " . $sql . "<br>" . $conn->error;
    }
}
?>
