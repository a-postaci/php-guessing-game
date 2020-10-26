<?php
$oldguess = "";
$message = false;

session_start();

if (! isset ($_SESSION['randomnumber'])) {
    $_SESSION['randomnumber'] = rand(1,100);
}

if (isset($_POST['guess'])) {
    $oldguess = $_POST['guess'] + 0;
    if ($_POST['guess'] == $_SESSION['randomnumber']) {
        $message = " Well done, insert new guess to keep playing";
        session_unset();
    } else if ($_POST['guess'] < $_SESSION['randomnumber']) {
        $message = "Guess is too low";
    } else {
        $message = "Guess is too high";
    }
}

?>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Gues Game</title>
</head>

<body>

    <h1>Guess Game</h1>
    <p>What is the number that I have picked ?</p>



    <form action="" method="POST">
        <p>
            <label for="guess">Enter your guess:</label>
            <input type="text" name="guess" id="guess" size=35 value="<?= htmlentities($oldguess) ?>">
        </p>
        <input type="submit" value="Try">
    </form>


    <?php
    if ($message !== false) {
        echo ("<p><b>$message</b></p>");
    }
    ?>


</body>

</html>
