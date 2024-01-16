<?php
// Set the API endpoint URL
$url = 'https://api.vaktija.ba/vaktija/v1/110';

// Send an HTTP request to the API and get the response
$response = file_get_contents($url);

// Convert the JSON response to a PHP array
$data = json_decode($response, true);

// Get the prayer times from the array
$prayer_times = $data['vakat'];

// Set the timezone
date_default_timezone_set('Europe/Sarajevo');

$prayer_name = '';

foreach ($prayer_times as $key => $value) {
    switch ($key) {
        case 0:
            $prayer_name = "Sabah";
            break;
        case 1:
            $prayer_name = "Sunrise";
            break;
        case 2:
            $prayer_name = "Podne";
            break;
        case 3:
            $prayer_name = "Ikindija";
            break;
        case 4:
            $prayer_name = "Aksam";
            break;
        case 5:
            $prayer_name = "Jacija";
            break;
    }
}

echo "</table>";

// Set the prayer times
$fajr_time = strtotime($prayer_times[0]);
$sunrise_time = strtotime($prayer_times[1]);
$dhuhr_time = strtotime($prayer_times[2]);
$asr_time = strtotime($prayer_times[3]);
$maghrib_time = strtotime($prayer_times[4]);
$isha_time = strtotime($prayer_times[5]);

// Determine the time to the next prayer
$next_prayer = '';
$next_prayer_time = 0;
$countdown = 0;
$current_time = time();

if ($current_time < $fajr_time) {
    $next_prayer = 'Sabah';
    $next_prayer_time = $fajr_time;
} elseif ($current_time < $dhuhr_time) {
    $next_prayer = 'Podne';
    $next_prayer_time = $dhuhr_time;
} elseif ($current_time < $asr_time) {
    $next_prayer = 'Ikindija';
    $next_prayer_time = $asr_time;
} elseif ($current_time < $maghrib_time) {
    $next_prayer = 'Aksam';
    $next_prayer_time = $maghrib_time;
} elseif ($current_time < $isha_time) {
    $next_prayer = 'Jacija';
    $next_prayer_time = $isha_time;
} else {
    $next_prayer = 'Sabah';
    $next_prayer_time = strtotime('+1 day', $fajr_time);
}

$countdown = $next_prayer_time - $current_time;
?>

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Vakat</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            font-size: 40px;
            background-color: #f0f0f0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        #prayer-times {
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            height: 20vh;
            background-color: #f0f0f0;
            border-bottom: 1px solid #999;
            padding-bottom: 20px;
            margin-bottom: 20px;
        }
        #prayer-times span {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 0 30px;
        }
        #prayer-times span:first-child {
            margin-left: 0;
        }
        #prayer-times span:last-child {
            margin-right: 0;
        }
        #prayer-times span em {
            font-size: 34px;
            color: #999;
            margin-top: 5px;
        }
        #prayer-times span.highlight {
            color: #f1c40f;
        }
        #countdown-timer {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 20vh;
            color: green;
            font-size: 36px;
            font-weight: bold;
            text-align: center;
        }
        #sabah-time {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 10vh;
            background-color: #f0f0f0;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div id="sabah-time">
        <p style="font-size: 32px;">
            Vrijeme ezana za Sabah namaz: <span style="font-weight: bold;"><?= date("H:i", $sunrise_time - 1800) ?></span>
        </p>
    </div>
    <div id="prayer-times">
    <?php foreach ($prayer_times as $key => $value): ?>
    <?php switch ($key):
        case 0:
            $prayer_name = "Zora";
            break;
        case 1:
            $prayer_name = "Izlazak sunca";
            break;
        case 2:
            $prayer_name = "Podne";
            break;
        case 3:
            $prayer_name = "Ikindija";
            break;
        case 4:
            $prayer_name = "Aksam";
            break;
        case 5:
            $prayer_name = "Jacija";
            break;
    endswitch; ?>

<span style="color: <?= $prayer_name === $next_prayer ? 'orange' : 'green'; ?>; font-weight: bold;">
        <span><?= $prayer_name ?></span><br>
        <em><?= $value ?></em>
    </span>
<?php endforeach; ?>
    </div>
    <div id="countdown-timer" data-countdown="<?= $countdown ?>">
        <?= gmdate("H:i:s", $countdown) ?> do namaza <?= $next_prayer ?>
    </div>
    <script>
    function updateCountdownTimer() {
        var countdownElement = document.getElementById("countdown-timer");
        var countdown = parseInt(countdownElement.getAttribute("data-countdown"));

        // Provjerite je li countdown istekao (vrijeme za namaz)
        if (countdown <= 0) {
            // Osvježite stranicu
            location.reload();
        } else {
            countdown = countdown - 1;
            var hours = Math.floor(countdown / 3600);
            var minutes = Math.floor((countdown % 3600) / 60);
            var seconds = countdown % 60;
            countdownElement.innerHTML = (hours < 10 ? "0" : "") + hours + ":" + (minutes < 10 ? "0" : "") + minutes + ":" + (seconds < 10 ? "0" : "") + seconds + " do namaza <?= $next_prayer ?>";
            countdownElement.setAttribute("data-countdown", countdown);
        }
    }

    // Pozivamo funkciju kako bismo postavili inicijalno vreme
    updateCountdownTimer();

    // Postavljanje intervala za ažuriranje svake sekunde
    setInterval(updateCountdownTimer, 1000);
</script>
</body>
</html>
