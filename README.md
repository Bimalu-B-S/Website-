# Website-
Sample clock 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="clock">
        <span id="time"></span>
    </div>
    <script src="script.js"></script>
</body>
</html>

body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #282c34;
    color: white;
    font-family: Arial, sans-serif;
}

.clock {
    font-size: 48px;
    font-weight: bold;
    padding: 20px;
    border: 2px solid white;
    border-radius: 10px;
    background-color: #3b3f46;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
}

function updateClock() {
    const now = new Date();
    const hours = String(now.getHours()).padStart(2, '0');
    const minutes = String(now.getMinutes()).padStart(2, '0');
    const seconds = String(now.getSeconds()).padStart(2, '0');
    document.getElementById('time').textContent = `${hours}:${minutes}:${seconds}`;
}

// Update the clock every second
setInterval(updateClock, 1000);

// Initialize the clock immediately
updateClock();
