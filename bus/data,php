<?php
// Assuming your database is named 'bus_pass' and has a table named 'applications'
$servername = "your_server_name";
$username = "your_username";
$password = "your_password";
$dbname = "bus_pass";

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);

// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

// Handle form submission
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = $_POST["name"];
    $from = $_POST["from"];
    $destination = $_POST["destination"];
    $passType = $_POST["passType"];
    $passDuration = $_POST["passDuration"];

    // Insert data into the database
    $sql = "INSERT INTO applications (name, from_location, destination, pass_type, pass_duration) 
            VALUES ('$name', '$from', '$destination', '$passType', '$passDuration')";

    if ($conn->query($sql) === TRUE) {
        echo "Application submitted successfully.";
    } else {
        echo "Error: " . $sql . "<br>" . $conn->error;
    }
}

// Close the database connection
$conn->close();
?>
