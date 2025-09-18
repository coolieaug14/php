<html>
<head>
    <title>Student Details</title>
</head>
<body>
<form method="post" action="">
    username: <input type="text" name="name">
    password: <input type="password" name="password">
    <input type="submit" value="Submit">
</form>
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $name = $_POST['name'];
    $password = $_POST['password'];
    if ($name == "admin" && $password == "admin123") {
        header("Location: homepage.php");
        exit();
    } else {
        echo "<h3 style='color:red;'>Invalid Credentials</h3>";
    }
}
?>
</body>
</html>
