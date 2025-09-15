<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BalkanRun</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8;
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 1rem;
            overflow: hidden;
        }
        .game-container {
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
            background: #fff;
            border-radius: 2rem;
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
            padding: 1.5rem;
            max-width: 90vw;
            width: 100%;
            height: 90vh;
        }
        canvas {
            background-color: #87CEEB;
            display: block;
            border-radius: 1rem;
            border: 4px solid #333;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.2);
            touch-action: none;
        }
        .ui-panel {
            margin-top: 1rem;
            width: 100%;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
            gap: 1rem;
        }
        #distance-display {
            font-size: 2.25rem;
            font-weight: bold;
            color: #2563eb;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        #message-box {
            position: absolute;
            background-color: #fde68a;
            color: #92400e;
            padding: 1rem;
            border-radius: 0.75rem;
            font-weight: bold;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            display: none;
            transition: opacity 0.5s ease-in-out;
            max-width: 400px;
            text-align: center;
            z-index: 10;
        }
        .btn {
            padding: 0.75rem 2rem;
            border-radius: 9999px;
            font-weight: bold;
            color: white;
            transition: all 0.2s ease-in-out;
            cursor: pointer;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            background: linear-gradient(145deg, #1d4ed8, #3b82f6);
            border: none;
            font-size: 1.25rem;
        }
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 12px -1px rgba(0, 0, 0, 0.15);
        }
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }
        .modal {
            background-color: #fff;
            padding: 2.5rem;
            border-radius: 1.5rem;
            text-align: center;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
            max-width: 90vw;
            animation: fadeIn 0.3s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }
        .modal h2 {
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 1rem;
        }
        .modal p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 600px;
        }
        .modal-btn {
            background: linear-gradient(145deg, #1d4ed8, #3b82f6);
            padding: 0.75rem 2rem;
            border-radius: 9999px;
            font-weight: bold;
            color: white;
            transition: all 0.2s ease-in-out;
            cursor: pointer;
            border: none;
        }
        .modal-btn:hover {
            transform: translateY(-2px);
        }
        /* Style for the pause/resume button to make it look great */
        #pauseButton {
            background: linear-gradient(145deg, #ef4444, #f59e0b);
        }
        #pauseButton:hover {
            transform: scale(1.05);
            box-shadow: 8px 8px 16px rgba(0, 0, 0, 0.2);
        }
        #energy-bar-container {
            width: 150px;
            height: 25px;
            background-color: #e5e7eb;
            border-radius: 9999px;
            overflow: hidden;
            box-shadow: inset 0 2px 4px 0 rgba(0, 0, 0, 0.06);
        }
        #energy-bar {
            height: 100%;
            background-color: #22c55e;
            transition: width 0.3s ease-in-out;
            border-radius: 9999px;
        }
        .victory-text {
            font-size: 2.5rem;
            font-weight: bold;
            color: #1a202c;
            text-shadow: 2px 2px 0 #fff;
            position: absolute;
            top: 20%;
            left: 50%;
            transform: translateX(-50%);
            z-index: 2000;
        }
    </style>
</head>
<body>

<div class="game-container">
    <canvas id="gameCanvas"></canvas>
    <div id="message-box" class="message-box"></div>
    <div class="ui-panel">
        <div class="bg-gray-200 rounded-full px-6 py-2 shadow-inner inline-block">
            <span class="text-gray-600 font-bold text-lg">Distance:</span>
            <span id="distance-display">0 km</span>
        </div>
        <div class="flex flex-col items-center">
            <span class="text-gray-600 font-bold text-lg">Energy</span>
            <div id="energy-bar-container">
                <div id="energy-bar"></div>
            </div>
        </div>
        <div class="flex flex-col items-center w-full max-w-sm sm:max-w-md">
            <span class="text-gray-600 font-bold text-lg mb-2">Route Map</span>
            <canvas id="mapCanvas" class="w-full h-4 rounded-full shadow-inner bg-gray-200"></canvas>
            <div class="flex justify-between w-full text-xs text-gray-500 mt-1">
                <span>Skopje</span>
                <span>Stip</span>
                <span>Radovish</span>
            </div>
        </div>
        <button id="pauseButton" class="btn">Pause</button>
    </div>
</div>

<div id="modal-container" class="modal-overlay hidden">
    <div id="start-modal" class="modal">
        <h2 class="text-blue-800">BalkanRun</h2>
        <p>Eat kebapcinja od Destan and somuni to keep your energy up. Help Kiril and Irena run from Skopje to Radovish! Click, tap, or use the **spacebar** to jump.</p>
        <button id="startButton" class="modal-btn">Start Game</button>
    </div>
</div>

<audio id="background-music" src="https://www.learningcontainer.com/wp-content/uploads/2020/02/Ambient-Music-Loop.mp3" loop preload="auto"></audio>
<audio id="victory-sound" src="https://soundbible.com/mp3/TaDa-SoundBible.com-1884170618.mp3" preload="auto"></audio>

<script>
    // Constants for the game
    const BASE_GAME_SPEED = 5;
    const JUMP_POWER = -25;
    const GRAVITY = 1.2;
    const TOTAL_DISTANCE_KM = 115; // Skopje to Stip to Radovish
    const DAY_NIGHT_CYCLE_KM = 60;

    // Milestones and messages for the run
    const MILESTONES = [
        { km: 5, name: "Village of Ilinden" },
        { km: 45, name: "Sveti Nikole" },
        { km: 85, name: "Stip" },
        { km: TOTAL_DISTANCE_KM, name: "Radovish" }
    ];

    const MILESTONE_MESSAGES = {
        "Village of Ilinden": "You've reached the village of Ilinden! Keep on running!",
        "Sveti Nikole": "You've reached Sveti Nikole, the city of paprika! Keep running!",
        "Stip": "Welcome to Stip, home of the pastrmajlija! You're almost there!",
        "Radovish": "WELCOME TO RADOVIS"
    };

    // Canvas and UI elements
    const canvas = document.getElementById('gameCanvas');
    const ctx = canvas.getContext('2d');
    const distanceDisplay = document.getElementById('distance-display');
    const energyBar = document.getElementById('energy-bar');
    const messageBox = document.getElementById('message-box');
    const modalContainer = document.getElementById('modal-container');
    const startButton = document.getElementById('startButton');
    const pauseButton = document.getElementById('pauseButton');
    const mapCanvas = document.getElementById('mapCanvas');
    const mapCtx = mapCanvas.getContext('2d');
    const backgroundMusic = document.getElementById('background-music');
    const victorySound = document.getElementById('victory-sound');

    // Game state variables
    let isGameRunning = false;
    let isPaused = false;
    let distance = 0;
    let energy = 100;
    const maxEnergy = 100;
    let milestonesShown = new Set();
    let messageTimer;
    let animationFrame = 0;
    let gameSpeed = BASE_GAME_SPEED;
    
    // Arrays for effects
    const particles = [];
    let clouds = [];
    let obstacles = [];
    
    // Character and item images
    const characterImage = new Image();
    characterImage.src = 'https://i.postimg.cc/PxjxYR28/Subject-2-removebg-preview.png';

    const kebapceImage = new Image();
    kebapceImage.src = 'https://i.postimg.cc/FzF0gRDc/Subject-2.png';

    const somuniImage = new Image();
    somuniImage.src = 'https://i.postimg.cc/vTm6xKZt/Subject-3.png';
    
    // Game objects
    const characters = {
        x: 50,
        y: 0,
        width: 60,
        height: 100,
        yVelocity: 0,
        isJumping: false,
        groundY: 0,
        draw() {
            let yOffset = 0;
            let tilt = 0;
            if (!this.isJumping) {
                const bobbingFrequency = 0.1;
                const bobbingAmplitude = 2;
                yOffset = Math.sin(animationFrame * bobbingFrequency) * bobbingAmplitude;
                tilt = Math.cos(animationFrame * bobbingFrequency) * 0.05;
            }
            ctx.save();
            ctx.translate(this.x + this.width / 2, this.y + this.height / 2);
            ctx.rotate(tilt);
            ctx.drawImage(characterImage, -this.width / 2, -this.height / 2 + yOffset, this.width, this.height);
            ctx.restore();
        },
        jump() {
            if (!this.isJumping && isGameRunning && !isPaused) {
                this.yVelocity = JUMP_POWER;
                this.isJumping = true;
            }
        }
    };

    class Kebapce {
        constructor(x, y) {
            this.x = x;
            this.y = y;
            this.width = 60; 
            this.height = 60; 
        }

        draw() {
            ctx.drawImage(kebapceImage, this.x, this.y, this.width, this.height);
        }
    }

    class Somuni {
        constructor(x, y) {
            this.x = x;
            this.y = y;
            this.width = 100;
            this.height = 100;
        }

        draw() {
             ctx.drawImage(somuniImage, this.x, this.y, this.width, this.height);
        }
    }
    
    class Obstacle {
        constructor(x, type) {
            this.x = x;
            this.type = type;
            this.emoji = '';
            this.width = 0;
            this.height = 0;
            this.y = 0;

            switch(this.type) {
                case 'cow':
                    this.emoji = '🐮';
                    this.width = 80;
                    this.height = 60;
                    this.y = characters.groundY - this.height + 15;
                    break;
                case 'trashcan':
                    this.emoji = '🗑️';
                    this.width = 50;
                    this.height = 60;
                    this.y = characters.groundY - this.height + 15;
                    break;
                case 'car':
                    this.emoji = '🚗';
                    this.width = 120;
                    this.height = 60;
                    this.y = characters.groundY - this.height + 15;
                    break;
            }
        }
        
        draw() {
            ctx.font = `${this.height}px sans-serif`;
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText(this.emoji, this.x + this.width / 2, this.y + this.height / 2);
        }
    }
    
    class SomuniDancer {
        constructor(x, y) {
            this.x = x;
            this.y = y;
            this.size = Math.random() * 100 + 50;
            this.vx = (Math.random() - 0.5) * 5;
            this.vy = (Math.random() - 0.5) * 5;
            this.angle = Math.random() * Math.PI * 2;
            this.rotationSpeed = (Math.random() - 0.5) * 0.05;
            this.bounce = Math.random() * 0.1 + 0.05;
            this.time = 0;
        }

        draw() {
            ctx.save();
            ctx.translate(this.x, this.y);
            ctx.rotate(this.angle);
            ctx.drawImage(somuniImage, -this.size / 2, -this.size / 2, this.size, this.size);
            ctx.restore();
        }

        update() {
            this.x += this.vx;
            this.y += this.vy + Math.sin(this.time) * 2;
            this.angle += this.rotationSpeed;
            this.time += this.bounce;

            if (this.x > canvas.width + this.size || this.x < -this.size) {
                this.vx *= -1;
            }
            if (this.y > canvas.height + this.size || this.y < -this.size) {
                this.vy *= -1;
            }
        }
    }


    class Particle {
        constructor(x, y, color) {
            this.x = x;
            this.y = y;
            this.size = Math.random() * 5 + 2;
            this.color = color;
            this.velocity = {
                x: (Math.random() - 0.5) * 4,
                y: (Math.random() - 0.5) * 4 - 2
            };
            this.alpha = 1;
            this.friction = 0.95;
            this.gravity = 0.1;
        }

        draw() {
            ctx.save();
            ctx.globalAlpha = this.alpha;
            ctx.fillStyle = this.color;
            ctx.beginPath();
            ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
            ctx.fill();
            ctx.restore();
        }

        update() {
            this.velocity.x *= this.friction;
            this.velocity.y *= this.friction;
            this.velocity.y += this.gravity;
            this.x += this.velocity.x;
            this.y += this.velocity.y;
            this.alpha -= 0.02;
        }
    }

    class BackgroundLayer {
        constructor(color, heightRatio, speedRatio) {
            this.color = color;
            this.height = canvas.height * heightRatio;
            this.speed = speedRatio;
            this.offset = 0;
            this.points = [];
            for (let i = 0; i <= canvas.width / 50 + 2; i++) {
                this.points.push(Math.random() * 0.4 + 0.6);
            }
        }
        
        draw() {
            ctx.fillStyle = this.color;
            ctx.beginPath();
            ctx.moveTo(0, canvas.height);
            
            for (let i = 0; i < this.points.length; i++) {
                const x = i * 50 - this.offset % 50;
                const h = Math.sin((x / 100) * (Math.random() * 0.5 + 0.5) + this.offset / 100) * this.height * 0.2 + this.height * this.points[i];
                ctx.lineTo(x, canvas.height - h);
            }
            
            ctx.lineTo(canvas.width, canvas.height);
            ctx.closePath();
            ctx.fill();
        }

        update() {
            this.offset += gameSpeed * this.speed;
        }
    }

    // Arrays to hold game objects
    const kebapce = [];
    const somuni = [];
    const markers = [];
    let backgroundLayers = [];
    let dancingSomunis = [];
    
    // Spacing for objects
    const minObjectGap = 200;
    const maxObjectGap = 500;
    let lastObjectX = canvas.width;
    let lastMarkerKm = 0;

    function generateObject() {
        const requiredGap = Math.random() * (maxObjectGap - minObjectGap) + minObjectGap;
        if (canvas.width - lastObjectX < requiredGap) {
            return;
        }

        const objectTypes = ['obstacle', 'kebapce', 'somuni'];
        const randomType = objectTypes[Math.floor(Math.random() * objectTypes.length)];

        const objectY = characters.groundY - Math.random() * 50 - 20;

        switch(randomType) {
            case 'kebapce':
                kebapce.push(new Kebapce(canvas.width, objectY));
                break;
            case 'somuni':
                somuni.push(new Somuni(canvas.width, objectY));
                break;
            case 'obstacle':
                const obstacleTypes = ['cow', 'trashcan', 'car'];
                const randomObstacle = obstacleTypes[Math.floor(Math.random() * obstacleTypes.length)];
                obstacles.push(new Obstacle(canvas.width, randomObstacle));
                break;
        }

        lastObjectX = canvas.width;
    }
    
    function generateMilestones() {
        const currentKm = Math.floor(distance);
        const milestone = MILESTONES.find(m => m.km > lastMarkerKm && currentKm >= m.km);
        if (milestone) {
             markers.push({
                 km: milestone.km,
                 name: milestone.name,
                 x: canvas.width,
                 y: characters.groundY + 10
             });
             lastMarkerKm = milestone.km;
        }
    }
    
    function generateParticles(x, y, count, color) {
        for (let i = 0; i < count; i++) {
            particles.push(new Particle(x, y, color));
        }
    }

    function moveObjects() {
        for (let i = kebapce.length - 1; i >= 0; i--) {
            kebapce[i].x -= gameSpeed;
            if (kebapce[i].x + kebapce[i].width < 0) {
                kebapce.splice(i, 1);
            }
        }
        for (let i = somuni.length - 1; i >= 0; i--) {
            somuni[i].x -= gameSpeed;
            if (somuni[i].x + somuni[i].width < 0) {
                somuni.splice(i, 1);
            }
        }
        for (let i = obstacles.length - 1; i >= 0; i--) {
            obstacles[i].x -= gameSpeed;
            if (obstacles[i].x + obstacles[i].width < 0) {
                obstacles.splice(i, 1);
            }
        }
        for (let i = clouds.length - 1; i >= 0; i--) {
            clouds[i].x -= clouds[i].speed;
            if (clouds[i].x + clouds[i].size < 0) {
                clouds.splice(i, 1);
                generateCloud();
            }
        }
         for (let i = markers.length - 1; i >= 0; i--) {
            markers[i].x -= gameSpeed;
            if (markers[i].x + 50 < 0) {
                markers.splice(i, 1);
            }
        }
        for (let i = particles.length - 1; i >= 0; i--) {
            particles[i].update();
            if (particles[i].alpha <= 0) {
                particles.splice(i, 1);
            }
        }
        lastObjectX -= gameSpeed;
    }

    function checkCollisions() {
        for (let i = kebapce.length - 1; i >= 0; i--) {
            const kbb = kebapce[i];
            const collision = (characters.x < kbb.x + kbb.width && characters.x + characters.width > kbb.x && characters.y < kbb.y + kbb.height && characters.y + characters.height > kbb.y);
            if (collision) {
                energy = Math.min(maxEnergy, energy + 25);
                generateParticles(kbb.x + kbb.width / 2, kbb.y + kbb.height / 2, 10, '#f59e0b');
                updateEnergyBar();
                kebapce.splice(i, 1);
            }
        }
        
        for (let i = somuni.length - 1; i >= 0; i--) {
            const som = somuni[i];
            const collision = (characters.x < som.x + som.width && characters.x + characters.width > som.x && characters.y < som.y + som.height && characters.y + characters.height > som.y);
            if (collision) {
                energy = Math.min(maxEnergy, energy + 50);
                generateParticles(som.x + som.width / 2, som.y + som.height / 2, 20, '#fef3c7');
                updateEnergyBar();
                somuni.splice(i, 1);
            }
        }

        for (let i = obstacles.length - 1; i >= 0; i--) {
            const obs = obstacles[i];
            const collision = (characters.x < obs.x + obs.width && characters.x + characters.width > obs.x && characters.y + characters.height > obs.y);
            if (collision) {
                showMessage("ne trcaj kako muva bez glava... pazi malce", 'corner', 3000); // 3 seconds for obstacle message
                energy = Math.max(0, energy - 15);
                updateEnergyBar();
                return;
            }
        }
    }

    function drawLandscape() {
        const dayProgress = Math.abs(Math.sin((distance / DAY_NIGHT_CYCLE_KM) * Math.PI));
        
        // Sky gradient
        const startColor = `rgb(${135 + 120 * dayProgress}, ${206 + 50 * dayProgress}, ${235 - 15 * dayProgress})`;
        const endColor = `rgb(${255 - 15 * (1-dayProgress)}, ${255 - 15 * (1-dayProgress)}, ${255 - 15 * (1-dayProgress)})`;
        const skyGradient = ctx.createLinearGradient(0, 0, 0, canvas.height);
        skyGradient.addColorStop(0, startColor);
        skyGradient.addColorStop(1, endColor);
        ctx.fillStyle = skyGradient;
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        
        // Stars
        if (dayProgress < 0.5) {
            ctx.fillStyle = `rgba(255, 255, 255, ${1 - dayProgress})`;
            for (let i = 0; i < 100; i++) {
                const x = Math.random() * canvas.width;
                const y = Math.random() * (canvas.height / 2);
                const size = Math.random() * 2;
                ctx.beginPath();
                ctx.arc(x, y, size, 0, Math.PI * 2);
                ctx.fill();
            }
        }
        
        // Clouds
        ctx.fillStyle = '#fff';
        clouds.forEach(cloud => {
            ctx.globalAlpha = cloud.alpha;
            ctx.beginPath();
            ctx.arc(cloud.x, cloud.y, cloud.size, 0, Math.PI * 2);
            ctx.arc(cloud.x + cloud.size * 0.8, cloud.y + cloud.size * 0.2, cloud.size * 0.7, 0, Math.PI * 2);
            ctx.arc(cloud.x + cloud.size * 1.5, cloud.y, cloud.size, 0, Math.PI * 2);
            ctx.fill();
        });
        ctx.globalAlpha = 1;

        // Draw background layers
        backgroundLayers.forEach(layer => {
            layer.update();
            layer.draw();
        });

        const groundHeight = 50;
        const groundY = canvas.height - groundHeight;

        // Draw ground
        ctx.fillStyle = '#4b5563';
        ctx.fillRect(0, groundY, canvas.width, groundHeight);

        // Draw a simple road
        ctx.fillStyle = '#555';
        ctx.fillRect(0, groundY - 20, canvas.width, 20);

        // Draw road lines
        ctx.fillStyle = '#fde047';
        let lineOffset = -distance * 2 % 40;
        for (let i = lineOffset; i < canvas.width; i += 40) {
            ctx.fillRect(i, groundY - 10, 20, 2);
        }
    }
    
    function drawMilestones() {
        markers.forEach(marker => {
            ctx.fillStyle = '#fef3c7'; // Light wood color
            ctx.beginPath();
            ctx.moveTo(marker.x, marker.y);
            ctx.lineTo(marker.x + 40, marker.y - 10);
            ctx.lineTo(marker.x + 40, marker.y - 60);
            ctx.lineTo(marker.x, marker.y - 50);
            ctx.closePath();
            ctx.fill();

            ctx.fillStyle = '#000';
            ctx.font = '16px Inter';
            ctx.textAlign = 'center';
            const name = marker.name.split(" ");
            let y = marker.y - 45;
            name.forEach(line => {
                ctx.fillText(line, marker.x + 20, y);
                y += 18;
            });
        });
    }

    function updateEnergyBar() {
        energyBar.style.width = `${energy}%`;
        if (energy < 20) {
            energyBar.style.backgroundColor = '#ef4444';
        } else if (energy < 50) {
            energyBar.style.backgroundColor = '#f59e0b';
        } else {
            energyBar.style.backgroundColor = '#22c55e';
        }
    }

    function drawMap() {
        mapCanvas.width = mapCanvas.clientWidth;
        mapCanvas.height = mapCanvas.clientHeight;
        mapCtx.clearRect(0, 0, mapCanvas.width, mapCanvas.height);
        
        // Draw the route line
        mapCtx.fillStyle = '#3b82f6';
        mapCtx.fillRect(0, mapCanvas.height / 2 - 2, mapCanvas.width, 4);

        // Draw milestones on the map
        const stipProgress = MILESTONES[2].km / TOTAL_DISTANCE_KM;
        const stipX = stipProgress * mapCanvas.width;
        mapCtx.beginPath();
        mapCtx.arc(stipX, mapCanvas.height / 2, 5, 0, Math.PI * 2);
        mapCtx.fillStyle = '#3b82f6';
        mapCtx.fill();
        
        const radovishX = mapCanvas.width;
        mapCtx.beginPath();
        mapCtx.arc(radovishX, mapCanvas.height / 2, 5, 0, Math.PI * 2);
        mapCtx.fillStyle = '#3b82f6';
        mapCtx.fill();

        // Calculate and draw the character's position
        const progress = Math.min(1, distance / TOTAL_DISTANCE_KM);
        const markerX = progress * mapCanvas.width;
        mapCtx.beginPath();
        mapCtx.arc(markerX, mapCanvas.height / 2, 7, 0, Math.PI * 2);
        mapCtx.fillStyle = energy < 20 ? '#ef4444' : '#22c55e';
        mapCtx.fill();
    }
    
    function showVictoryScreen() {
        isGameRunning = false;
        isPaused = true;
        backgroundMusic.pause();
        victorySound.play();
        
        for(let i = 0; i < 5; i++) {
            dancingSomunis.push(new SomuniDancer(Math.random() * canvas.width, Math.random() * canvas.height));
        }

        // Confetti burst
        const confettiColors = ['#f43f5e', '#ec4899', '#a855f7', '#6366f1', '#3b82f6', '#06b6d4', '#10b981', '#f59e0b', '#f97316'];
        for (let i = 0; i < 200; i++) {
            const randomColor = confettiColors[Math.floor(Math.random() * confettiColors.length)];
            generateParticles(Math.random() * canvas.width, Math.random() * canvas.height, 1, randomColor);
        }

        // A simple flash effect
        canvas.style.opacity = 0;
        setTimeout(() => {
            canvas.style.opacity = 1;
        }, 100);
        
        victoryAnimationLoop();
    }

    function victoryAnimationLoop() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = '#87CEEB';
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        
        dancingSomunis.forEach(som => {
            som.update();
            som.draw();
        });

        particles.forEach(p => p.update());
        particles.forEach(p => p.draw());

        ctx.font = 'bold 3rem Inter';
        ctx.fillStyle = '#1e40af';
        ctx.textAlign = 'center';
        ctx.textBaseline = 'middle';
        ctx.fillText("VICTORY!", canvas.width / 2, canvas.height / 2 - 100);
        
        ctx.font = 'bold 2rem Inter';
        ctx.fillStyle = '#333';
        ctx.fillText("Welcome to Radovish!", canvas.width / 2, canvas.height / 2 - 40);

        requestAnimationFrame(victoryAnimationLoop);
    }
    
    function animate() {
        if (!isGameRunning || isPaused) {
            return;
        }

        animationFrame++;
        
        gameSpeed = BASE_GAME_SPEED + Math.floor(distance / 50) * 0.5;

        characters.yVelocity += GRAVITY;
        characters.y += characters.yVelocity;
        if (characters.y >= characters.groundY) {
            characters.y = characters.groundY;
            characters.yVelocity = 0;
            characters.isJumping = false;
        }

        moveObjects();
        generateObject();
        generateMilestones();

        distance += gameSpeed / 100;
        distanceDisplay.textContent = `${Math.floor(distance)} km`;
        // Removed energy depletion code to prevent the energy bar from decreasing
        // energy -= 0.05;
        updateEnergyBar();
        drawMap();

        ctx.clearRect(0, 0, canvas.width, canvas.height);
        drawLandscape();
        characters.draw();
        kebapce.forEach(kbb => kbb.draw());
        somuni.forEach(som => som.draw());
        obstacles.forEach(obs => obs.draw());
        particles.forEach(p => p.draw());
        drawMilestones();

        checkCollisions();
        checkMessages();
        
        requestAnimationFrame(animate);
    }

    function checkMessages() {
        const currentDistance = Math.floor(distance);
        
        for (const milestone of MILESTONES) {
            if (currentDistance >= milestone.km && !milestonesShown.has(milestone.name)) {
                showMessage(MILESTONE_MESSAGES[milestone.name], 'center', 8000); // 8 seconds for milestone messages
                milestonesShown.add(milestone.name);
                if (milestone.name === "Radovish") {
                    endGame();
                }
                break;
            }
        }
    }

    function showMessage(text, position, duration) {
        messageBox.textContent = text;
        messageBox.style.display = 'block';

        if (position === 'corner') {
            messageBox.style.top = '1rem';
            messageBox.style.right = '1rem';
            messageBox.style.left = 'auto';
            messageBox.style.transform = 'none';
        } else {
            messageBox.style.top = '2rem';
            messageBox.style.left = '50%';
            messageBox.style.right = 'auto';
            messageBox.style.transform = 'translateX(-50%)';
        }

        clearTimeout(messageTimer);
        messageTimer = setTimeout(() => {
            messageBox.style.opacity = '0';
            setTimeout(() => {
                messageBox.style.display = 'none';
                messageBox.style.opacity = '1';
            }, 500);
        }, duration);
    }

    function endGame() {
        isGameRunning = false;
        isPaused = true;
        showVictoryScreen();
    }

    function startGame() {
        modalContainer.classList.add('hidden');
        isGameRunning = true;
        isPaused = false;
        distance = 0;
        energy = 100;
        kebapce.length = 0;
        somuni.length = 0;
        obstacles.length = 0;
        particles.length = 0;
        milestonesShown.clear();
        lastMarkerKm = 0;
        lastObjectX = canvas.width;
        pauseButton.textContent = 'Pause';
        gameSpeed = BASE_GAME_SPEED;
        updateEnergyBar();
        backgroundMusic.play();
        
        animate();
    }

    function togglePause() {
        if (!isGameRunning) return;
        isPaused = !isPaused;
        pauseButton.textContent = isPaused ? 'Resume' : 'Pause';
        if (!isPaused) {
            backgroundMusic.play();
            animate();
        } else {
            backgroundMusic.pause();
        }
    }

    function setupEventListeners() {
        canvas.addEventListener('click', () => characters.jump());
        canvas.addEventListener('touchstart', (e) => {
            e.preventDefault();
            characters.jump();
        });
        document.addEventListener('keydown', (e) => {
            if (e.code === 'Space' || e.key === ' ') {
                characters.jump();
            }
        });
        startButton.addEventListener('click', startGame);
        pauseButton.addEventListener('click', togglePause);
    }

    function resizeCanvas() {
        canvas.width = window.innerWidth * 0.8;
        canvas.height = window.innerHeight * 0.6;
        characters.groundY = canvas.height - 50 - characters.height;
        characters.y = characters.groundY;
        
        // Define background layers with different colors and speeds for parallax effect
        backgroundLayers = [
            new BackgroundLayer('#5f6d7c', 0.2, 0.2), // Farthest layer
            new BackgroundLayer('#7c8998', 0.3, 0.4),
            new BackgroundLayer('#94a3b8', 0.4, 0.6)  // Closest layer
        ];
    }

    window.addEventListener('load', () => {
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        setupEventListeners();
        modalContainer.classList.remove('hidden');
    });

</script>
</body>
</html>
