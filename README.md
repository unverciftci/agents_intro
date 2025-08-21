<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Agents Course Introduction</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        .hero {
            text-align: center;
            padding: 60px 20px;
            color: white;
        }
        
        .title {
            font-size: 4rem;
            font-weight: 900;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            animation: fadeInUp 1s ease-out;
        }
        
        .subtitle {
            font-size: 1.5rem;
            margin-bottom: 40px;
            opacity: 0.9;
            animation: fadeInUp 1s ease-out 0.3s both;
        }
        
        .journey-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        
        .journey-title {
            text-align: center;
            color: white;
            font-size: 2.5rem;
            margin-bottom: 50px;
            animation: fadeInUp 1s ease-out 0.6s both;
        }
        
        .journey-path {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            position: relative;
        }
        
        .step {
            background: white;
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            transform: translateY(50px);
            opacity: 0;
            animation: slideInUp 0.8s ease-out forwards;
            position: relative;
            overflow: hidden;
        }
        
        .step:nth-child(1) { animation-delay: 0.8s; }
        .step:nth-child(2) { animation-delay: 1.0s; }
        .step:nth-child(3) { animation-delay: 1.2s; }
        .step:nth-child(4) { animation-delay: 1.4s; }
        
        .step::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #667eea, #764ba2);
        }
        
        .step-number {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            font-weight: bold;
            margin: 0 auto 20px;
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
        }
        
        .step-icon {
            font-size: 3rem;
            margin-bottom: 15px;
            animation: bounce 2s infinite;
        }
        
        .step-title {
            font-size: 1.4rem;
            font-weight: bold;
            margin-bottom: 15px;
            color: #333;
        }
        
        .step-description {
            color: #666;
            line-height: 1.6;
            margin-bottom: 20px;
        }
        
        .step-outcome {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px;
            border-radius: 10px;
            font-weight: bold;
            margin-top: 20px;
        }
        
        .transformation {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 30px;
            margin: 60px 0;
            flex-wrap: wrap;
        }
        
        .transform-box {
            background: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
            flex: 1;
            min-width: 200px;
            max-width: 300px;
        }
        
        .transform-arrow {
            font-size: 3rem;
            color: #ffd700;
            animation: pulse 2s infinite;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .cta {
            text-align: center;
            padding: 40px 20px;
            color: white;
            animation: fadeInUp 1s ease-out 1.6s both;
        }
        
        .cta-text {
            font-size: 1.8rem;
            margin-bottom: 30px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
        }
        
        .start-button {
            background: linear-gradient(135deg, #ff6b6b 0%, #ffd93d 100%);
            color: white;
            padding: 20px 40px;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(255, 107, 107, 0.3);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .start-button:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 15px 30px rgba(255, 107, 107, 0.4);
        }
        
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .floating-element {
            position: absolute;
            font-size: 2rem;
            opacity: 0.1;
            animation: float 10s infinite linear;
        }
        
        .floating-element:nth-child(1) { left: 10%; animation-delay: 0s; }
        .floating-element:nth-child(2) { left: 20%; animation-delay: 2s; }
        .floating-element:nth-child(3) { left: 30%; animation-delay: 4s; }
        .floating-element:nth-child(4) { left: 40%; animation-delay: 6s; }
        .floating-element:nth-child(5) { left: 60%; animation-delay: 1s; }
        .floating-element:nth-child(6) { left: 70%; animation-delay: 3s; }
        .floating-element:nth-child(7) { left: 80%; animation-delay: 5s; }
        .floating-element:nth-child(8) { left: 90%; animation-delay: 7s; }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes slideInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }
        
        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
            100% {
                transform: scale(1);
            }
        }
        
        @keyframes float {
            from {
                transform: translateY(100vh) rotate(0deg);
            }
            to {
                transform: translateY(-100px) rotate(360deg);
            }
        }
        
        @media (max-width: 768px) {
            .title {
                font-size: 2.5rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
            
            .journey-title {
                font-size: 2rem;
            }
            
            .transformation {
                flex-direction: column;
            }
            
            .transform-arrow {
                transform: rotate(90deg);
            }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-element">🤖</div>
        <div class="floating-element">🚀</div>
        <div class="floating-element">🛠️</div>
        <div class="floating-element">🧠</div>
        <div class="floating-element">⚡</div>
        <div class="floating-element">🎯</div>
        <div class="floating-element">🔧</div>
        <div class="floating-element">💡</div>
    </div>

    <section class="hero">
        <h1 class="title">🤖 AI Agents Course</h1>
        <p class="subtitle">From Basic Chat to Intelligent Agents That Actually DO Things</p>
    </section>

    <section class="journey-container">
        <h2 class="journey-title">🚀 Your Learning Journey</h2>
        
        <div class="journey-path">
            <div class="step">
                <div class="step-number">1</div>
                <div class="step-icon">💬</div>
                <h3 class="step-title">Meet Your AI</h3>
                <p class="step-description">
                    Load your first language model and understand the basics: 
                    prompt in → text out. Simple but powerful!
                </p>
                <div class="step-outcome">
                    ✅ Working AI chatbot
                </div>
            </div>

            <div class="step">
                <div class="step-number">2</div>
                <div class="step-icon">🛠️</div>
                <h3 class="step-title">Add Tools</h3>
                <p class="step-description">
                    Transform your chatbot into an agent that can use tools like 
                    calculators, weather APIs, and more!
                </p>
                <div class="step-outcome">
                    🚀 Agent with tools
                </div>
            </div>

            <div class="step">
                <div class="step-number">3</div>
                <div class="step-icon">🧠</div>
                <h3 class="step-title">Give It Memory</h3>
                <p class="step-description">
                    Build agents that remember conversations, learn from interactions,
                    and maintain context across sessions.
                </p>
                <div class="step-outcome">
                    🎯 Smart, persistent agent
                </div>
            </div>

            <div class="step">
                <div class="step-number">4</div>
                <div class="step-icon">🎬</div>
                <h3 class="step-title">Take Real Actions</h3>
                <p class="step-description">
                    Create agents that actually DO things - manage files, send emails,
                    set reminders, and interact with the real world!
                </p>
                <div class="step-outcome">
                    🌟 Action-taking agent
                </div>
            </div>
        </div>
    </section>

    <section class="transformation">
        <div class="transform-box">
            <div style="font-size: 3rem; margin-bottom: 15px;">😴</div>
            <h3>Before</h3>
            <p>Basic chatbot that just generates text responses</p>
        </div>
        
        <div class="transform-arrow">⭐</div>
        
        <div class="transform-box">
            <div style="font-size: 3rem; margin-bottom: 15px;">🚀</div>
            <h3>After</h3>
            <p>Intelligent agent that can remember, use tools, and take real actions in the world</p>
        </div>
    </section>

    <section class="cta">
        <p class="cta-text">Ready to build the future of AI? 🌟</p>
        <button class="start-button" onclick="startCourse()">
            🚀 Start Building Agents!
        </button>
    </section>

    <script>
        function startCourse() {
            alert('🎉 Welcome to AI Agents! Let\'s start with Tutorial 1: Meet Your AI');
        }
        
        // Add some interactive sparkle
        document.addEventListener('mousemove', function(e) {
            if (Math.random() > 0.95) {
                createSparkle(e.clientX, e.clientY);
            }
        });
        
        function createSparkle(x, y) {
            const sparkle = document.createElement('div');
            sparkle.innerHTML = '✨';
            sparkle.style.position = 'fixed';
            sparkle.style.left = x + 'px';
            sparkle.style.top = y + 'px';
            sparkle.style.pointerEvents = 'none';
            sparkle.style.fontSize = '20px';
            sparkle.style.zIndex = '1000';
            sparkle.style.animation = 'fadeOut 1s forwards';
            
            document.body.appendChild(sparkle);
            
            setTimeout(() => {
                document.body.removeChild(sparkle);
            }, 1000);
        }
        
        // Add fadeOut animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes fadeOut {
                from { opacity: 1; transform: scale(1); }
                to { opacity: 0; transform: scale(0) translateY(-50px); }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
