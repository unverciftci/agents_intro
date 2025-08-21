<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Agents Course</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            margin: 0;
            padding: 20px;
            color: white;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 10px;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 40px;
        }
        
        .steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }
        
        .step {
            background: white;
            color: #333;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .step-number {
            background: #667eea;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 15px;
            font-weight: bold;
        }
        
        .step h3 {
            margin: 15px 0 10px;
            color: #333;
        }
        
        .step p {
            color: #666;
            line-height: 1.5;
            margin-bottom: 15px;
        }
        
        .outcome {
            background: #667eea;
            color: white;
            padding: 10px;
            border-radius: 8px;
            font-weight: bold;
        }
        
        .transformation {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 30px;
            margin: 50px 0;
            flex-wrap: wrap;
        }
        
        .transform-box {
            background: white;
            color: #333;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            min-width: 200px;
        }
        
        .arrow {
            font-size: 2rem;
            color: #ffd700;
        }
        
        @media (max-width: 768px) {
            .hero h1 { font-size: 2rem; }
            .transformation { flex-direction: column; }
            .arrow { transform: rotate(90deg); }
        }
    </style>
</head>
<body>
    <div class="container">
        <section class="hero">
            <h1>🤖 AI Agents Course</h1>
            <p>From Basic Chat to Intelligent Agents That Actually DO Things</p>
        </section>

        <h2>🚀 Your Learning Journey</h2>
        
        <div class="steps">
            <div class="step">
                <div class="step-number">1</div>
                <div style="font-size: 2rem;">💬</div>
                <h3>Meet Your AI</h3>
                <p>Load your first language model and understand the basics: prompt in → text out. Simple but powerful!</p>
                <div class="outcome">✅ Working AI chatbot</div>
            </div>

            <div class="step">
                <div class="step-number">2</div>
                <div style="font-size: 2rem;">🛠️</div>
                <h3>Add Tools</h3>
                <p>Transform your chatbot into an agent that can use tools like calculators, weather APIs, and more!</p>
                <div class="outcome">🚀 Agent with tools</div>
            </div>

            <div class="step">
                <div class="step-number">3</div>
                <div style="font-size: 2rem;">🧠</div>
                <h3>Give It Memory</h3>
                <p>Build agents that remember conversations, learn from interactions, and maintain context across sessions.</p>
                <div class="outcome">🎯 Smart, persistent agent</div>
            </div>

            <div class="step">
                <div class="step-number">4</div>
                <div style="font-size: 2rem;">🎬</div>
                <h3>Take Real Actions</h3>
                <p>Create agents that actually DO things - manage files, send emails, set reminders, and interact with the real world!</p>
                <div class="outcome">🌟 Action-taking agent</div>
            </div>
        </div>

        <section class="transformation">
            <div class="transform-box">
                <div style="font-size: 2.5rem; margin-bottom: 15px;">😴</div>
                <h3>Before</h3>
                <p>Basic chatbot that just generates text responses</p>
            </div>
            
            <div class="arrow">⭐</div>
            
            <div class="transform-box">
                <div style="font-size: 2.5rem; margin-bottom: 15px;">🚀</div>
                <h3>After</h3>
                <p>Intelligent agent that can remember, use tools, and take real actions in the world</p>
            </div>
        </section>

        <section style="margin: 50px 0;">
            <p style="font-size: 1.5rem; margin-bottom: 20px;">Ready to build the future of AI? 🌟</p>
            <button style="background: linear-gradient(135deg, #ff6b6b 0%, #ffd93d 100%); color: white; padding: 15px 30px; border: none; border-radius: 25px; font-size: 1.1rem; cursor: pointer;">
                🚀 Start Building Agents!
            </button>
        </section>
    </div>
</body>
</html>
