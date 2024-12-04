const canvas = document.getElementById("wheel");
const ctx = canvas.getContext("2d");
const spinBtn = document.getElementById("spin-btn");
const resultDisplay = document.getElementById("result");

const options = [
    "1 Personal Class", "1 Week Pass Freeze",
    "1 Group Class", "1 Split Class with Friend",
    "2 Group Classes", "+5% Discount",
    "Free Consultation with Coach", 
    "1 Personal Class", "1 Week Pass Freeze",
    "1 Group Class", "1 Split Class with Friend",
    "2 Group Classes", "+5% Discount",
    "Free Consultation with Coach"
];

const colors = ['#FFC1CC', '#FFB347', '#A7FFEB', '#FFD1DC', '#D5AAFF', '#C4FCEF', '#FFABAB', '#FFDAC1', '#FFF5BA', '#B9FBC0', '#A2E4B8', '#D0E1FF', '#FFBCBC', '#D1C4E9'];

const segments = options.length;
const segmentAngle = (2 * Math.PI) / segments;
let currentAngle = 0;

// Draw the wheel
function drawWheel() {
    options.forEach((option, i) => {
        const angle = i * segmentAngle;

        // Draw segment
        ctx.beginPath();
        ctx.moveTo(250, 250);
        ctx.arc(250, 250, 250, angle, angle + segmentAngle);
        ctx.fillStyle = colors[i % colors.length];
        ctx.fill();
        ctx.stroke();

        // Add text
        ctx.save();
        ctx.translate(250, 250);
        ctx.rotate(angle + segmentAngle / 2);
        ctx.textAlign = "center";
        ctx.fillStyle = "#000";
        ctx.font = "16px Arial";
        ctx.fillText(option, 150, 10);
        ctx.restore();
    });
}

drawWheel();

// Spin the wheel
spinBtn.addEventListener("click", () => {
    // Disable the spin button after the first click
    spinBtn.disabled = true;
    spinBtn.textContent = "Spinning...";

    const spinAmount = Math.random() * 360 + 720; // Random spin (720 for 2 full rotations)
    const spinDuration = 2000; // Duration of spin animation in ms
    const startTime = performance.now();

    function animateWheel(time) {
        const elapsedTime = time - startTime;
        const easing = elapsedTime / spinDuration; // Linear easing
        const easedAngle = Math.min(easing, 1) * spinAmount;

        currentAngle = easedAngle % 360;
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // Rotate the wheel
        ctx.save();
        ctx.translate(250, 250);
        ctx.rotate((currentAngle * Math.PI) / 180);
        ctx.translate(-250, -250);
        drawWheel();
        ctx.restore();

        if (elapsedTime < spinDuration) {
            requestAnimationFrame(animateWheel);
        } else {
            determineResult(currentAngle);
        }
    }

    requestAnimationFrame(animateWheel);
});

// Determine which segment the wheel lands on
function determineResult(angle) {
    const adjustedAngle = (360 - angle + 90) % 360; // Adjust for offset
    const segmentIndex = Math.floor(adjustedAngle / (360 / segments));
    resultDisplay.textContent = `You won: ${options[segmentIndex]}!`;

    // Update button to show the spin is complete
    spinBtn.textContent = "Spin Complete";
}
