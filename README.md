<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>POLB Mutation Classification Research</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            color: #fff;
            min-height: 100vh;
            overflow-x: hidden;
            perspective: 1000px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        header {
            text-align: center;
            margin-bottom: 3rem;
            transform-style: preserve-3d;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0) rotateX(5deg); }
            50% { transform: translateY(-10px) rotateX(5deg); }
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            background: linear-gradient(to right, #ff7e5f, #feb47b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            transform: translateZ(20px);
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 2rem;
            transform: translateZ(15px);
        }
        
        .card-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 2rem;
            width: 100%;
            max-width: 500px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transform-style: preserve-3d;
            transition: transform 0.5s ease, box-shadow 0.5s ease;
        }
        
        .card:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.3);
        }
        
        .card h2 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: #ffcc00;
            transform: translateZ(30px);
        }
        
        .card p {
            line-height: 1.6;
            margin-bottom: 1.5rem;
            transform: translateZ(20px);
        }
        
        .journal-info {
            background: rgba(0, 0, 0, 0.2);
            padding: 1.5rem;
            border-radius: 15px;
            margin: 1.5rem 0;
            transform: translateZ(15px);
        }
        
        .journal-info h3 {
            color: #4fc3f7;
            margin-bottom: 1rem;
        }
        
        .journal-info p {
            margin-bottom: 0.5rem;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(to right, #ff7e5f, #feb47b);
            color: white;
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 1rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            transform: translateZ(25px);
        }
        
        .btn:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        .floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -1;
        }
        
        .floating-element {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float-around 15s infinite linear;
        }
        
        @keyframes float-around {
            0% { transform: translate(0, 0) rotate(0deg); }
            25% { transform: translate(20px, 40px) rotate(90deg); }
            50% { transform: translate(40px, 0) rotate(180deg); }
            75% { transform: translate(20px, -40px) rotate(270deg); }
            100% { transform: translate(0, 0) rotate(360deg); }
        }
        
        .floating-element:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 10%;
            left: 10%;
            animation-duration: 20s;
        }
        
        .floating-element:nth-child(2) {
            width: 60px;
            height: 60px;
            top: 70%;
            left: 80%;
            animation-duration: 25s;
        }
        
        .floating-element:nth-child(3) {
            width: 100px;
            height: 100px;
            top: 40%;
            left: 85%;
            animation-duration: 30s;
        }
        
        .floating-element:nth-child(4) {
            width: 50px;
            height: 50px;
            top: 80%;
            left: 15%;
            animation-duration: 18s;
        }
        
        .floating-element:nth-child(5) {
            width: 70px;
            height: 70px;
            top: 15%;
            left: 75%;
            animation-duration: 22s;
        }
        
        .acknowledgment {
            text-align: center;
            margin-top: 2rem;
            font-style: italic;
            opacity: 0.8;
            transform: translateZ(10px);
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .card {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
    </div>
    
    <div class="container">
        <header>
            <h1>Enhancing POLB Mutation Classification with a Random Forest and PSO Hybrid Model</h1>
            <p class="subtitle">Our latest research published in the Journal of Information Systems Engineering and Management</p>
        </header>
        
        <div class="card-container">
            <div class="card">
                <h2>Research Overview</h2>
                <p>In this work, we propose a novel hybrid model combining Random Forest with Particle Swarm Optimization (PSO) to enhance the classification of POLB gene mutations, which are critical in cancer diagnostics.</p>
                
                <div class="journal-info">
                    <h3>Publication Details</h3>
                    <p><strong>Journal:</strong> Journal of Information Systems Engineering and Management</p>
                    <p><strong>DOI:</strong> https://doi.org/10.52783/jisem.v10i46s.8772</p>
                    <p><strong>Volume:</strong> 10 | Issue: 46s | e-ISSN: 2468-4376</p>
                </div>
                
                <p>The model achieved high performance metrics, demonstrating its potential in biomedical data analysis and precision medicine.</p>
                
                <a href="https://github.com/yasserhessein/Cancer-associated-mutations-of-POLB" class="btn pulse">
                    <i class="fas fa-book-open"></i> Read the Full Paper
                </a>
            </div>
            
            <div class="card">
                <h2>Key Contributions</h2>
                <p>This research makes several important contributions to the field of biomedical data analysis:</p>
                <ul style="margin-left: 1.5rem; margin-bottom: 1.5rem; transform: translateZ(20px);">
                    <li>Novel hybrid approach combining Random Forest and PSO</li>
                    <li>Enhanced classification accuracy for POLB gene mutations</li>
                    <li>Application of computational intelligence in precision medicine</li>
                    <li>Potential for improved cancer diagnostics</li>
                </ul>
                
                <p>Special thanks to my co-authors and everyone who supported this research journey.</p>
                
                <div class="acknowledgment">
                    <p>Advancing the frontier of computational biology and precision medicine</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Add interactive 3D effect on mouse move
        document.addEventListener('mousemove', (e) => {
            const cards = document.querySelectorAll('.card');
            const xAxis = (window.innerWidth / 2 - e.pageX) / 25;
            const yAxis = (window.innerHeight / 2 - e.pageY) / 25;
            
            cards.forEach(card => {
                card.style.transform = `rotateY(${xAxis}deg) rotateX(${yAxis}deg) translateY(-10px)`;
            });
        });
        
        // Reset cards when mouse leaves the window
        document.addEventListener('mouseleave', () => {
            const cards = document.querySelectorAll('.card');
            cards.forEach(card => {
                card.style.transform = 'rotateY(0deg) rotateX(0deg) translateY(0)';
            });
        });
    </script>
</body>
</html>