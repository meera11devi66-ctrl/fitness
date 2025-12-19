<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fitness Workout - Exercise & Training</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Style */
        header {
            background: linear-gradient(135deg, #1a2a6c, #2a3c8f, #3a4fb2);
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 28px;
            font-weight: 700;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            color: #4cd964;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            font-size: 18px;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #4cd964;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(26, 42, 108, 0.85), rgba(26, 42, 108, 0.9)), url('https://images.unsplash.com/photo-1536922246289-88c42f957773?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 80px 0;
            text-align: center;
            border-radius: 0 0 30px 30px;
            margin-bottom: 40px;
        }
        
        .hero h1 {
            font-size: 42px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 20px;
            max-width: 800px;
            margin: 0 auto 30px;
        }
        
        .cta-button {
            display: inline-block;
            background-color: #4cd964;
            color: white;
            padding: 15px 35px;
            font-size: 18px;
            font-weight: 600;
            text-decoration: none;
            border-radius: 50px;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(76, 217, 100, 0.4);
        }
        
        .cta-button:hover {
            background-color: #3bc453;
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(76, 217, 100, 0.6);
        }
        
        /* Main Content */
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 50px;
        }
        
        /* Workout Sidebar */
        .workout-sidebar {
            flex: 1;
            min-width: 300px;
            background-color: white;
            border-radius: 15px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .sidebar-title {
            font-size: 24px;
            color: #1a2a6c;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #f0f0f0;
        }
        
        .workout-categories {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-bottom: 25px;
        }
        
        .category-btn {
            background-color: #f8f9fa;
            border: none;
            padding: 16px 20px;
            text-align: left;
            border-radius: 10px;
            font-size: 17px;
            font-weight: 500;
            color: #333;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
        }
        
        .category-btn i {
            margin-right: 12px;
            font-size: 20px;
        }
        
        .category-btn:hover, .category-btn.active {
            background-color: #1a2a6c;
            color: white;
            transform: translateX(5px);
        }
        
        /* Advertisement Placeholder */
        .ad-placeholder {
            background-color: #f8f9fa;
            border: 2px dashed #ccc;
            border-radius: 10px;
            padding: 30px 15px;
            text-align: center;
            margin-top: 20px;
            margin-bottom: 20px;
        }
        
        .ad-label {
            font-size: 24px;
            font-weight: bold;
            color: #888;
            margin-bottom: 10px;
        }
        
        .ad-text {
            color: #aaa;
            font-size: 14px;
        }
        
        /* Workout Main Area */
        .workout-main {
            flex: 2;
            min-width: 300px;
        }
        
        .workout-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }
        
        .workout-card {
            background-color: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .workout-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .workout-img {
            height: 180px;
            background-size: cover;
            background-position: center;
        }
        
        .workout-info {
            padding: 20px;
        }
        
        .workout-title {
            font-size: 20px;
            color: #1a2a6c;
            margin-bottom: 10px;
        }
        
        .workout-desc {
            color: #666;
            font-size: 15px;
            margin-bottom: 15px;
        }
        
        .workout-meta {
            display: flex;
            justify-content: space-between;
            color: #777;
            font-size: 14px;
            margin-bottom: 20px;
        }
        
        .start-workout-btn {
            display: block;
            width: 100%;
            background-color: #4cd964;
            color: white;
            border: none;
            padding: 12px;
            border-radius: 8px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .start-workout-btn:hover {
            background-color: #3bc453;
        }
        
        /* Workout Performance Section */
        .workout-performance {
            background-color: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 40px;
            display: none;
        }
        
        .performance-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #f0f0f0;
        }
        
        .performance-title {
            font-size: 26px;
            color: #1a2a6c;
        }
        
        .timer {
            font-size: 32px;
            font-weight: 700;
            color: #4cd964;
            background-color: #f8f9fa;
            padding: 10px 20px;
            border-radius: 10px;
        }
        
        .exercise-container {
            margin-bottom: 30px;
        }
        
        .current-exercise {
            background-color: #f8f9fa;
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 25px;
            text-align: center;
        }
        
        .exercise-name {
            font-size: 28px;
            color: #1a2a6c;
            margin-bottom: 15px;
        }
        
        .exercise-reps {
            font-size: 22px;
            color: #4cd964;
            font-weight: 600;
            margin-bottom: 20px;
        }
        
        .exercise-desc {
            color: #666;
            font-size: 16px;
            line-height: 1.7;
        }
        
        .exercise-controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }
        
        .control-btn {
            padding: 12px 25px;
            font-size: 16px;
            font-weight: 600;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .start-btn {
            background-color: #4cd964;
            color: white;
        }
        
        .pause-btn {
            background-color: #ff9500;
            color: white;
        }
        
        .reset-btn {
            background-color: #ff3b30;
            color: white;
        }
        
        .next-btn {
            background-color: #1a2a6c;
            color: white;
        }
        
        .control-btn:hover {
            opacity: 0.9;
            transform: scale(1.05);
        }
        
        .exercise-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .exercise-item {
            display: flex;
            align-items: center;
            padding: 15px;
            background-color: #f8f9fa;
            border-radius: 10px;
            transition: all 0.3s;
        }
        
        .exercise-item.active {
            background-color: #e8f5e9;
            border-left: 5px solid #4cd964;
        }
        
        .exercise-item.completed {
            opacity: 0.7;
        }
        
        .exercise-number {
            background-color: #1a2a6c;
            color: white;
            width: 35px;
            height: 35px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            margin-right: 15px;
            font-weight: 600;
        }
        
        .exercise-details {
            flex-grow: 1;
        }
        
        .exercise-item-name {
            font-weight: 600;
            color: #333;
            margin-bottom: 5px;
        }
        
        .exercise-item-reps {
            color: #777;
            font-size: 14px;
        }
        
        /* Ad Banner */
        .ad-banner {
            background: linear-gradient(to right, #1a2a6c, #2a3c8f);
            color: white;
            text-align: center;
            padding: 20px;
            border-radius: 10px;
            margin: 30px 0;
        }
        
        .ad-banner h3 {
            font-size: 24px;
            margin-bottom: 10px;
        }
        
        .ad-banner p {
            font-size: 16px;
            opacity: 0.9;
        }
        
        /* Footer */
        footer {
            background-color: #1a2a6c;
            color: white;
            padding: 40px 0 20px;
            margin-top: 50px;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-bottom: 30px;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
            margin-bottom: 30px;
        }
        
        .footer-section h3 {
            font-size: 22px;
            margin-bottom: 20px;
            color: #4cd964;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 12px;
        }
        
        .footer-links a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: #4cd964;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 15px;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .performance-header {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .timer {
                margin-top: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-dumbbell"></i>
                    Fitness Workout
                </div>
                <nav>
                    <ul>
                        <li><a href="#home"><i class="fas fa-home"></i> Home</a></li>
                        <li><a href="#workouts"><i class="fas fa-running"></i> Workouts</a></li>
                        <li><a href="#performance"><i class="fas fa-play-circle"></i> Perform</a></li>
                        <li><a href="#about"><i class="fas fa-info-circle"></i> About</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Achieve Your Fitness Goals</h1>
            <p>Exercise with our comprehensive workout collection and track your progress. From beginners to advanced level, we have something for everyone.</p>
            <a href="#workouts" class="cta-button">Start Workout <i class="fas fa-arrow-right"></i></a>
        </div>
    </section>

    <div class="container">
        <!-- Ad Banner -->
        <div class="ad-banner">
            <h3>Ad Space Available</h3>
            <p>Your advertisement could be here! Contact us for advertising opportunities.</p>
        </div>
        
        <!-- Main Content -->
        <div class="main-content">
            <!-- Workout Sidebar -->
            <div class="workout-sidebar">
                <h2 class="sidebar-title">Workout Categories</h2>
                <div class="workout-categories">
                    <button class="category-btn active" data-category="all">
                        <i class="fas fa-list"></i> All Workouts
                    </button>
                    <button class="category-btn" data-category="strength">
                        <i class="fas fa-dumbbell"></i> Strength Training
                    </button>
                    <button class="category-btn" data-category="cardio">
                        <i class="fas fa-heartbeat"></i> Cardio
                    </button>
                    <button class="category-btn" data-category="yoga">
                        <i class="fas fa-spa"></i> Yoga & Flexibility
                    </button>
                    <button class="category-btn" data-category="beginner">
                        <i class="fas fa-user"></i> For Beginners
                    </button>
                    <button class="category-btn" data-category="advanced">
                        <i class="fas fa-fire"></i> Advanced Workouts
                    </button>
                </div>
                
                <!-- Ad Placeholder -->
                <div class="ad-placeholder">
                    <div class="ad-label">ADVERTISEMENT</div>
                    <div class="ad-text">Your ad would be displayed here</div>
                </div>
                
                <!-- Another Ad Placeholder -->
                <div class="ad-placeholder">
                    <div class="ad-label">SPONSORED</div>
                    <div class="ad-text">Sponsored content area</div>
                </div>
            </div>

            <!-- Workout Main Area -->
            <div class="workout-main">
                <h2 class="sidebar-title" id="workouts">Workout Collection</h2>
                
                <!-- Ad Placeholder -->
                <div class="ad-placeholder" style="margin-bottom: 25px;">
                    <div class="ad-label">AD BANNER</div>
                    <div class="ad-text">Advertisement space for fitness products</div>
                </div>
                
                <!-- Workout List -->
                <div class="workout-list">
                    <!-- Workout Cards will be added by JavaScript -->
                </div>

                <!-- Workout Performance Section -->
                <div class="workout-performance" id="performance">
                    <div class="performance-header">
                        <h2 class="performance-title">Workout Performance</h2>
                        <div class="timer" id="timer">00:00</div>
                    </div>
                    
                    <!-- Ad Placeholder inside workout performance -->
                    <div class="ad-placeholder" style="margin-bottom: 20px;">
                        <div class="ad-label">SPONSORED</div>
                        <div class="ad-text">Try our premium workout plans!</div>
                    </div>
                    
                    <div class="exercise-container">
                        <div class="current-exercise">
                            <h3 class="exercise-name" id="current-exercise-name">Exercise Name</h3>
                            <div class="exercise-reps" id="current-exercise-reps">Reps: 12 x 3</div>
                            <p class="exercise-desc" id="current-exercise-desc">Exercise description will be shown here. Focus on proper form and technique.</p>
                            
                            <div class="exercise-controls">
                                <button class="control-btn start-btn" id="start-exercise">
                                    <i class="fas fa-play"></i> Start
                                </button>
                                <button class="control-btn pause-btn" id="pause-exercise">
                                    <i class="fas fa-pause"></i> Pause
                                </button>
                                <button class="control-btn reset-btn" id="reset-exercise">
                                    <i class="fas fa-redo"></i> Reset
                                </button>
                                <button class="control-btn next-btn" id="next-exercise">
                                    <i class="fas fa-forward"></i> Next
                                </button>
                            </div>
                        </div>
                        
                        <h3 style="margin-bottom: 15px; color: #1a2a6c;">Exercise List</h3>
                        <div class="exercise-list" id="exercise-list">
                            <!-- Exercise list will be added by JavaScript -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer id="about">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Fitness Workout</h3>
                    <p>Your personal fitness companion. We help you achieve your health and fitness goals.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#workouts">Workouts</a></li>
                        <li><a href="#performance">Perform</a></li>
                        <li><a href="#">Progress Tracker</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Contact Us</h3>
                    <ul class="footer-links">
                        <li><i class="fas fa-envelope"></i> info@fitnessworkout.com</li>
                        <li><i class="fas fa-phone"></i> +91 98765 43210</li>
                        <li><i class="fas fa-map-marker-alt"></i> Mumbai, India</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                &copy; 2023 Fitness Workout. All rights reserved.
            </div>
        </div>
    </footer>

    <script>
        // Workout Data
        const workouts = [
            {
                id: 1,
                name: "Full Body Workout",
                description: "A complete workout targeting all major muscle groups.",
                category: "strength",
                duration: "45 minutes",
                difficulty: "Intermediate",
                exercises: 8,
                img: "https://images.unsplash.com/photo-1534367507877-0edd93bd013b?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80"
            },
            {
                id: 2,
                name: "HIIT Cardio",
                description: "High-intensity interval training that helps burn calories fast.",
                category: "cardio",
                duration: "30 minutes",
                difficulty: "Hard",
                exercises: 10,
                img: "https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80"
            },
            {
                id: 3,
                name: "Beginner Yoga",
                description: "Basic yoga poses to improve flexibility and reduce stress.",
                category: "yoga",
                duration: "40 minutes",
                difficulty: "Easy",
                exercises: 12,
                img: "https://images.unsplash.com/photo-1599901860904-17e6ed7083a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80"
            },
            {
                id: 4,
                name: "Push-up Challenge",
                description: "Push-up variations to build upper body strength.",
                category: "strength",
                duration: "25 minutes",
                difficulty: "Intermediate",
                exercises: 6,
                img: "https://images.unsplash.com/photo-1598974357801-cbca100e5d10?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80"
            },
            {
                id: 5,
                name: "Runner's Cardio",
                description: "Cardio workout focused on running to build endurance.",
                category: "cardio",
                duration: "50 minutes",
                difficulty: "Intermediate",
                exercises: 7,
                img: "https://images.unsplash.com/photo-1558618666-fcd25c85cd64?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80"
            },
            {
                id: 6,
                name: "Advanced Plyometrics",
                description: "Advanced plyometric exercises to boost power and speed.",
                category: "advanced",
                duration: "35 minutes",
                difficulty: "Hard",
                exercises: 9,
                img: "https://images.unsplash.com/photo-1549060279-7e168fce7090?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80"
            }
        ];

        // Exercise Data
        const exercises = [
            {
                name: "Push-ups",
                reps: "12 reps x 3 sets",
                description: "Place your hands slightly wider than shoulder-width apart, bend elbows and bring chest close to floor, then push back up.",
                workoutId: 1
            },
            {
                name: "Squats",
                reps: "15 reps x 3 sets",
                description: "Keep feet shoulder-width apart, push hips back and lower down until thighs are parallel to floor, then rise back up.",
                workoutId: 1
            },
            {
                name: "Plank",
                reps: "30 seconds x 3 sets",
                description: "Hold your body in a straight line on elbows and toes, keeping core engaged in plank position.",
                workoutId: 1
            },
            {
                name: "Burpees",
                reps: "10 reps x 3 sets",
                description: "Start standing, go into a squat, place hands on floor, kick feet back, do a push-up, bring feet back, and jump up.",
                workoutId: 2
            },
            {
                name: "Mountain Climbers",
                reps: "20 reps x 3 sets",
                description: "Start in push-up position, alternate bringing each knee toward chest, moving at a fast pace.",
                workoutId: 2
            },
            {
                name: "Jumping Jacks",
                reps: "30 reps x 3 sets",
                description: "Start standing, jump feet apart while raising arms overhead, then return to starting position.",
                workoutId: 2
            },
            {
                name: "Sun Salutation",
                reps: "5 rounds",
                description: "A sequence of yoga poses that warms up the body and improves flexibility.",
                workoutId: 3
            },
            {
                name: "Tree Pose",
                reps: "30 seconds per leg",
                description: "Balance on one leg while placing the sole of the other foot on the inner thigh of the standing leg, bring hands to prayer position.",
                workoutId: 3
            }
        ];

        // DOM Elements
        const workoutList = document.querySelector('.workout-list');
        const categoryButtons = document.querySelectorAll('.category-btn');
        const workoutPerformance = document.querySelector('.workout-performance');
        const timerElement = document.getElementById('timer');
        const currentExerciseName = document.getElementById('current-exercise-name');
        const currentExerciseReps = document.getElementById('current-exercise-reps');
        const currentExerciseDesc = document.getElementById('current-exercise-desc');
        const exerciseList = document.getElementById('exercise-list');
        const startBtn = document.getElementById('start-exercise');
        const pauseBtn = document.getElementById('pause-exercise');
        const resetBtn = document.getElementById('reset-exercise');
        const nextBtn = document.getElementById('next-exercise');

        // Timer Variables
        let timerInterval;
        let seconds = 0;
        let isTimerRunning = false;
        let currentWorkoutId = null;
        let currentExerciseIndex = 0;

        // Render Workout Cards
        function renderWorkouts(category = 'all') {
            workoutList.innerHTML = '';
            
            const filteredWorkouts = category === 'all' 
                ? workouts 
                : workouts.filter(workout => workout.category === category);
            
            filteredWorkouts.forEach(workout => {
                const workoutCard = document.createElement('div');
                workoutCard.className = 'workout-card';
                workoutCard.innerHTML = `
                    <div class="workout-img" style="background-image: url('${workout.img}')"></div>
                    <div class="workout-info">
                        <h3 class="workout-title">${workout.name}</h3>
                        <p class="workout-desc">${workout.description}</p>
                        <div class="workout-meta">
                            <span><i class="far fa-clock"></i> ${workout.duration}</span>
                            <span><i class="fas fa-signal"></i> ${workout.difficulty}</span>
                            <span><i class="fas fa-dumbbell"></i> ${workout.exercises} exercises</span>
                        </div>
                        <button class="start-workout-btn" data-id="${workout.id}">
                            <i class="fas fa-play-circle"></i> Start Workout
                        </button>
                    </div>
                `;
                
                workoutList.appendChild(workoutCard);
            });
            
            // Add event listeners to workout start buttons
            document.querySelectorAll('.start-workout-btn').forEach(button => {
                button.addEventListener('click', function() {
                    const workoutId = parseInt(this.getAttribute('data-id'));
                    startWorkout(workoutId);
                });
            });
        }

        // Start Workout
        function startWorkout(workoutId) {
            currentWorkoutId = workoutId;
            currentExerciseIndex = 0;
            
            // Show workout performance section
            workoutPerformance.style.display = 'block';
            
            // Scroll to workout performance section
            workoutPerformance.scrollIntoView({ behavior: 'smooth' });
            
            // Reset timer
            resetTimer();
            
            // Load exercises
            loadExercises(workoutId);
            
            // Show first exercise
            showCurrentExercise();
        }

        // Load Exercises
        function loadExercises(workoutId) {
            const workoutExercises = exercises.filter(exercise => exercise.workoutId === workoutId);
            
            // Render exercise list
            exerciseList.innerHTML = '';
            workoutExercises.forEach((exercise, index) => {
                const exerciseItem = document.createElement('div');
                exerciseItem.className = 'exercise-item';
                if (index === 0) exerciseItem.classList.add('active');
                
                exerciseItem.innerHTML = `
                    <div class="exercise-number">${index + 1}</div>
                    <div class="exercise-details">
                        <div class="exercise-item-name">${exercise.name}</div>
                        <div class="exercise-item-reps">${exercise.reps}</div>
                    </div>
                `;
                
                exerciseList.appendChild(exerciseItem);
            });
        }

        // Show Current Exercise
        function showCurrentExercise() {
            const workoutExercises = exercises.filter(exercise => exercise.workoutId === currentWorkoutId);
            
            if (currentExerciseIndex < workoutExercises.length) {
                const exercise = workoutExercises[currentExerciseIndex];
                
                // Update current exercise details
                currentExerciseName.textContent = exercise.name;
                currentExerciseReps.textContent = exercise.reps;
                currentExerciseDesc.textContent = exercise.description;
                
                // Update exercise list
                document.querySelectorAll('.exercise-item').forEach((item, index) => {
                    item.classList.remove('active', 'completed');
                    if (index === currentExerciseIndex) {
                        item.classList.add('active');
                    } else if (index < currentExerciseIndex) {
                        item.classList.add('completed');
                    }
                });
            } else {
                // Workout completed
                currentExerciseName.textContent = "Workout Completed!";
                currentExerciseReps.textContent = "Congratulations!";
                currentExerciseDesc.textContent = "You have successfully completed this workout. Well done!";
                
                // Stop timer
                stopTimer();
                
                // Mark all exercises as completed
                document.querySelectorAll('.exercise-item').forEach(item => {
                    item.classList.remove('active');
                    item.classList.add('completed');
                });
            }
        }

        // Timer Functions
        function startTimer() {
            if (!isTimerRunning) {
                isTimerRunning = true;
                timerInterval = setInterval(() => {
                    seconds++;
                    updateTimerDisplay();
                }, 1000);
            }
        }

        function stopTimer() {
            isTimerRunning = false;
            clearInterval(timerInterval);
        }

        function resetTimer() {
            stopTimer();
            seconds = 0;
            updateTimerDisplay();
        }

        function updateTimerDisplay() {
            const minutes = Math.floor(seconds / 60);
            const remainingSeconds = seconds % 60;
            timerElement.textContent = `${minutes.toString().padStart(2, '0')}:${remainingSeconds.toString().padStart(2, '0')}`;
        }

        // Event Listeners
        // Category buttons
        categoryButtons.forEach(button => {
            button.addEventListener('click', function() {
                // Update active button
                categoryButtons.forEach(btn => btn.classList.remove('active'));
                this.classList.add('active');
                
                // Filter workouts
                const category = this.getAttribute('data-category');
                renderWorkouts(category);
            });
        });

        // Exercise control buttons
        startBtn.addEventListener('click', startTimer);
        
        pauseBtn.addEventListener('click', stopTimer);
        
        resetBtn.addEventListener('click', function() {
            resetTimer();
            currentExerciseIndex = 0;
            showCurrentExercise();
        });
        
        nextBtn.addEventListener('click', function() {
            currentExerciseIndex++;
            showCurrentExercise();
        });

        // Render workouts on page load
        document.addEventListener('DOMContentLoaded', function() {
            renderWorkouts();
            
            // Add smooth scrolling for navigation links
            document.querySelectorAll('nav a, .cta-button').forEach(link => {
                link.addEventListener('click', function(e) {
                    if (this.getAttribute('href').startsWith('#')) {
                        e.preventDefault();
                        const targetId = this.getAttribute('href');
                        const targetElement = document.querySelector(targetId);
                        
                        if (targetElement) {
                            targetElement.scrollIntoView({ behavior: 'smooth' });
                        }
                    }
                });
            });
            
            // Simulate ad rotation (changing ad text)
            const adLabels = document.querySelectorAll('.ad-label');
            const adTexts = [
                "Premium fitness equipment sale!",
                "Try our 30-day workout challenge!",
                "Get personalized diet plans",
                "Yoga mats at 50% discount",
                "Subscribe for premium workouts"
            ];
            
            let adIndex = 0;
            setInterval(() => {
                adLabels.forEach(label => {
                    label.textContent = "ADVERTISEMENT";
                });
                
                // Change ad text in placeholder areas
                document.querySelectorAll('.ad-text').forEach((adText, index) => {
                    adText.textContent = adTexts[(adIndex + index) % adTexts.length];
                });
                
                adIndex = (adIndex + 1) % adTexts.length;
            }, 5000);
        });
    </script>
</body>
</html>
