<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MindEase - Your Mental Wellness Companion</title>
    <meta name="description" content="MindEase - A calming mental health platform offering support, resources, and interactive guidance for anxiety, stress, and emotional wellness.">
    
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <!-- Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://kit.fontawesome.com/your-kit-id.js" crossorigin="anonymous"></script>
    
    <style>
        :root {
            /* Beach-inspired color palette */
            --pastel-orange: #FFD4B3;
            --soft-orange: #FFAB7A;
            --sandy-yellow: #F4E4BC;
            --creamy-white: #FFF8F0;
            --suede: #C8A882;
            --light-blue: #B8E6F0;
            --ocean-blue: #7FB3D3;
            --deep-blue: #5B9BD5;
            --warm-beige: #F5E6D3;
            --coral: #FF9F7A;
            --sage-green: #A8C090;
            --soft-gray: #F0F0F0;
            --text-dark: #2C3E50;
            --text-light: #6C7B7F;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background: linear-gradient(135deg, var(--creamy-white) 0%, var(--warm-beige) 100%);
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Navigation */
        .navbar {
            background: rgba(255, 248, 240, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Poppins', sans-serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--deep-blue);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .logo i {
            color: var(--coral);
            font-size: 2rem;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
            align-items: center;
        }

        .nav-link {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 25px;
        }

        .nav-link:hover {
            color: var(--deep-blue);
            background: var(--light-blue);
            transform: translateY(-2px);
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--ocean-blue), var(--deep-blue));
            color: white;
            padding: 0.7rem 1.5rem;
            border: none;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(123, 179, 211, 0.4);
        }

        .user-info {
            color: var(--text-dark);
            font-weight: 500;
            padding: 0.5rem 1rem;
            background: var(--light-blue);
            border-radius: 20px;
            font-size: 0.9rem;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--deep-blue);
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, var(--creamy-white) 0%, var(--pastel-orange) 50%, var(--light-blue) 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100" fill="%23FFD4B3" opacity="0.1"><path d="M0,50 Q250,0 500,50 T1000,50 L1000,100 L0,100 Z"/></svg>') repeat-x;
            animation: wave 10s linear infinite;
        }

        @keyframes wave {
            0% { transform: translateX(0); }
            100% { transform: translateX(-100px); }
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
            padding-top: 100px;
        }

        .hero-text h1 {
            font-family: 'Poppins', sans-serif;
            font-size: 3.5rem;
            font-weight: 700;
            color: var(--text-dark);
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero-text .highlight {
            color: var(--coral);
            background: linear-gradient(135deg, var(--coral), var(--deep-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero-text p {
            font-size: 1.2rem;
            color: var(--text-light);
            margin-bottom: 2rem;
            line-height: 1.8;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn-secondary {
            background: transparent;
            color: var(--deep-blue);
            border: 2px solid var(--deep-blue);
            padding: 0.7rem 1.5rem;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
        }

        .btn-secondary:hover {
            background: var(--deep-blue);
            color: white;
            transform: translateY(-2px);
        }

        .hero-image {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .floating-card {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            animation: float 6s ease-in-out infinite;
            max-width: 400px;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .floating-card h3 {
            color: var(--deep-blue);
            margin-bottom: 1rem;
            font-family: 'Poppins', sans-serif;
        }

        .floating-card p {
            color: var(--text-light);
            margin-bottom: 1rem;
        }

        .mood-indicators {
            display: flex;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .mood-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            animation: pulse 2s infinite;
        }

        .mood-dot:nth-child(1) { background: var(--sage-green); }
        .mood-dot:nth-child(2) { background: var(--coral); animation-delay: 0.5s; }
        .mood-dot:nth-child(3) { background: var(--ocean-blue); animation-delay: 1s; }

        @keyframes pulse {
            0%, 100% { opacity: 0.6; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.2); }
        }

        /* About Section */
        .about {
            padding: 5rem 0;
            background: var(--creamy-white);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text h2 {
            font-family: 'Poppins', sans-serif;
            font-size: 2.5rem;
            color: var(--text-dark);
            margin-bottom: 1.5rem;
        }

        .about-text p {
            color: var(--text-light);
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .feature-item {
            background: white;
            padding: 1.5rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .feature-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }

        .feature-item i {
            font-size: 2rem;
            color: var(--coral);
            margin-bottom: 1rem;
        }

        .feature-item h4 {
            color: var(--text-dark);
            margin-bottom: 0.5rem;
            font-family: 'Poppins', sans-serif;
        }

        .feature-item p {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        /* Services Section */
        .services {
            padding: 5rem 0;
            background: linear-gradient(135deg, var(--warm-beige) 0%, var(--sandy-yellow) 100%);
        }

        .section-header {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-header h2 {
            font-family: 'Poppins', sans-serif;
            font-size: 2.5rem;
            color: var(--text-dark);
            margin-bottom: 1rem;
        }

        .section-header p {
            color: var(--text-light);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            text-align: center;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--pastel-orange), var(--coral));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            font-size: 2rem;
            color: white;
        }

        .service-card h3 {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            margin-bottom: 1rem;
        }

        .service-card p {
            color: var(--text-light);
            margin-bottom: 1.5rem;
        }

        .helpline-numbers {
            background: var(--light-blue);
            padding: 2rem;
            border-radius: 15px;
            margin-top: 3rem;
        }

        .helpline-numbers h3 {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            text-align: center;
            margin-bottom: 1.5rem;
        }

        .helpline-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }

        .helpline-item {
            background: white;
            padding: 1rem;
            border-radius: 10px;
            text-align: center;
        }

        .helpline-item strong {
            color: var(--deep-blue);
            display: block;
            margin-bottom: 0.5rem;
        }

        .helpline-item a {
            color: var(--coral);
            text-decoration: none;
            font-weight: 600;
        }

        /* Chatbot */
        .chatbot-container {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
        }

        .chatbot-toggle {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, var(--light-blue), var(--ocean-blue));
            border: none;
            border-radius: 50%;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
            animation: bounce 2s infinite;
        }

        .chatbot-toggle:hover {
            transform: scale(1.1);
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        .chatbot-window {
            position: fixed;
            bottom: 90px;
            right: 20px;
            width: 450px;
            height: 600px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            display: none;
            flex-direction: column;
            overflow: hidden;
        }

        .chatbot-header {
            background: linear-gradient(135deg, var(--light-blue), var(--ocean-blue));
            color: white;
            padding: 1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .chatbot-avatar {
            width: 40px;
            height: 40px;
            background: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--ocean-blue);
        }

        .chatbot-info h4 {
            margin: 0;
            font-size: 1rem;
        }

        .chatbot-info p {
            margin: 0;
            font-size: 0.8rem;
            opacity: 0.9;
        }

        .chatbot-messages {
            flex: 1;
            padding: 1rem;
            overflow-y: auto;
            background: var(--creamy-white);
        }

        .message {
            margin-bottom: 1rem;
            display: flex;
            align-items: flex-start;
            gap: 0.5rem;
        }

        .message.user {
            flex-direction: row-reverse;
        }

        .message-bubble {
            max-width: 80%;
            padding: 0.8rem;
            border-radius: 15px;
            font-size: 0.9rem;
            line-height: 1.4;
        }

        .message.bot .message-bubble {
            background: var(--light-blue);
            color: var(--text-dark);
        }

        .message.user .message-bubble {
            background: var(--coral);
            color: white;
        }

        .message-avatar {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            flex-shrink: 0;
        }

        .message.bot .message-avatar {
            background: var(--ocean-blue);
            color: white;
        }

        .message.user .message-avatar {
            background: var(--suede);
            color: white;
        }

        .chatbot-input {
            padding: 1rem;
            border-top: 1px solid var(--soft-gray);
            display: flex;
            gap: 0.5rem;
        }

        .chatbot-input input {
            flex: 1;
            padding: 0.8rem;
            border: 1px solid var(--soft-gray);
            border-radius: 20px;
            outline: none;
        }

        .chatbot-input button {
            background: var(--ocean-blue);
            color: white;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-left: 0.5rem;
        }

        .chatbot-input button:hover {
            background: var(--deep-blue);
            transform: scale(1.1);
        }

        .voice-btn {
            background: var(--coral) !important;
        }

        .voice-btn.listening {
            background: var(--sage-green) !important;
            animation: pulse 1s infinite;
        }

        .voice-btn.speaking {
            background: var(--pastel-orange) !important;
            animation: pulse 1s infinite;
        }

        .voice-btn.active {
            background: var(--sage-green) !important;
        }

        /* Mood Tracker Styles */
        .mood-tracker-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-top: 3rem;
        }

        .mood-selection-card,
        .mood-history-card {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        .mood-selection-card h3,
        .mood-history-card h3 {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            margin-bottom: 1rem;
            text-align: center;
        }

        .mood-options {
            display: flex;
            justify-content: space-between;
            gap: 0.5rem;
            margin: 2rem 0;
            flex-wrap: wrap;
        }

        .mood-option {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 1rem 0.5rem;
            border-radius: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
            background: var(--soft-gray);
            flex: 1;
            min-width: 70px;
            position: relative;
        }

        .mood-option:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            background: var(--light-blue);
        }

        .mood-option.selected {
            border-color: var(--ocean-blue);
            background: var(--light-blue);
            transform: scale(1.05);
        }

        .mood-emoji {
            font-size: 2rem;
            margin-bottom: 0.5rem;
        }

        .mood-option span {
            font-size: 0.8rem;
            font-weight: 500;
            color: var(--text-dark);
            margin-bottom: 0.25rem;
        }

        .mood-value {
            font-size: 0.7rem;
            color: var(--text-light);
            background: var(--creamy-white);
            padding: 0.2rem 0.4rem;
            border-radius: 10px;
            font-weight: 600;
        }

        .mood-note-section {
            margin-top: 2rem;
            padding-top: 2rem;
            border-top: 1px solid var(--soft-gray);
        }

        .mood-note-section label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--text-dark);
        }

        .mood-note-section textarea {
            width: 100%;
            min-height: 80px;
            padding: 1rem;
            border: 2px solid var(--soft-gray);
            border-radius: 10px;
            font-family: inherit;
            resize: vertical;
            margin-bottom: 1rem;
        }

        .mood-note-section textarea:focus {
            outline: none;
            border-color: var(--ocean-blue);
        }

        .mood-actions {
            display: flex;
            gap: 1rem;
            justify-content: center;
        }

        .mood-filter {
            display: flex;
            gap: 0.5rem;
            justify-content: center;
            margin-bottom: 2rem;
        }

        .filter-btn {
            background: var(--soft-gray);
            color: var(--text-dark);
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .filter-btn:hover {
            background: var(--light-blue);
        }

        .filter-btn.active {
            background: var(--ocean-blue);
            color: white;
        }

        .mood-bar-chart {
            background: var(--creamy-white);
            border-radius: 15px;
            padding: 2rem;
            margin-bottom: 2rem;
            min-height: 300px;
        }

        .no-data {
            text-align: center;
            color: var(--text-light);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 200px;
        }

        .no-data i {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: var(--coral);
        }

        .bar-chart-container {
            display: flex;
            align-items: end;
            justify-content: space-around;
            height: 200px;
            margin: 2rem 0;
            padding: 0 1rem;
        }

        .bar-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            flex: 1;
            max-width: 60px;
        }

        .bar {
            width: 100%;
            background: linear-gradient(to top, var(--coral), var(--pastel-orange));
            border-radius: 5px 5px 0 0;
            margin-bottom: 0.5rem;
            transition: all 0.3s ease;
            position: relative;
            min-height: 10px;
        }

        .bar:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(255, 159, 122, 0.3);
        }

        .bar-label {
            font-size: 0.7rem;
            color: var(--text-dark);
            font-weight: 500;
            text-align: center;
            margin-bottom: 0.25rem;
        }

        .bar-emoji {
            font-size: 1.2rem;
            margin-bottom: 0.25rem;
        }

        .bar-value {
            font-size: 0.8rem;
            color: var(--deep-blue);
            font-weight: 600;
            background: white;
            padding: 0.2rem 0.4rem;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .mood-stats {
            display: flex;
            justify-content: space-around;
            background: var(--pastel-orange);
            padding: 1.5rem;
            border-radius: 15px;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .stat-item {
            text-align: center;
            background: white;
            padding: 1rem;
            border-radius: 10px;
            flex: 1;
            min-width: 120px;
        }

        .stat-label {
            display: block;
            font-size: 0.9rem;
            color: var(--text-light);
            margin-bottom: 0.5rem;
        }

        .stat-value {
            font-size: 1.2rem;
            font-weight: 600;
            color: var(--deep-blue);
        }

        /* Responsive Design for Mood Tracker */
        @media (max-width: 768px) {
            .mood-tracker-container {
                grid-template-columns: 1fr;
            }
            
            .mood-options {
                justify-content: center;
                gap: 0.25rem;
            }
            
            .mood-option {
                min-width: 60px;
                padding: 0.8rem 0.3rem;
            }
            
            .mood-emoji {
                font-size: 1.5rem;
            }
            
            .mood-option span {
                font-size: 0.7rem;
            }
            
            .bar-chart-container {
                height: 150px;
            }
            
            .mood-stats {
                flex-direction: column;
            }
        }

        .typing-indicator {
            display: flex;
            gap: 0.3rem;
            padding: 0.8rem;
        }

        .typing-dot {
            width: 8px;
            height: 8px;
            background: var(--ocean-blue);
            border-radius: 50%;
            animation: typing 1.4s infinite;
        }

        .typing-dot:nth-child(2) { animation-delay: 0.2s; }
        .typing-dot:nth-child(3) { animation-delay: 0.4s; }

        @keyframes typing {
            0%, 60%, 100% { transform: translateY(0); }
            30% { transform: translateY(-10px); }
        }

        .exercise-suggestions {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 0.5rem;
        }

        .exercise-btn {
            background: var(--pastel-orange);
            color: var(--text-dark);
            border: none;
            padding: 0.4rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .exercise-btn:hover {
            background: var(--coral);
            color: white;
        }

        /* Exercise Modal */
        .exercise-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
        }

        .exercise-content {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            max-width: 500px;
            width: 90%;
            text-align: center;
        }

        .exercise-content h3 {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            margin-bottom: 1rem;
        }

        .breathing-circle {
            width: 150px;
            height: 150px;
            border: 4px solid var(--ocean-blue);
            border-radius: 50%;
            margin: 2rem auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: var(--ocean-blue);
            font-weight: 600;
        }

        .breathing-circle.inhale {
            animation: breatheIn 5s ease-in-out infinite;
        }

        .breathing-circle.exhale {
            animation: breatheOut 5s ease-in-out infinite;
        }

        @keyframes breatheIn {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }

        @keyframes breatheOut {
            0%, 100% { transform: scale(1.2); }
            50% { transform: scale(1); }
        }

        .exercise-controls {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-top: 2rem;
        }

        /* Meditation Modal */
        .meditation-modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--deep-blue), var(--ocean-blue));
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
        }

        .meditation-content {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 3rem;
            border-radius: 25px;
            max-width: 600px;
            width: 90%;
            text-align: center;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        }

        .meditation-content h3 {
            font-family: 'Poppins', sans-serif;
            color: var(--text-dark);
            margin-bottom: 1rem;
            font-size: 2rem;
        }

        .meditation-timer {
            font-size: 3rem;
            font-weight: 700;
            color: var(--deep-blue);
            margin: 2rem 0;
            font-family: 'Poppins', sans-serif;
        }

        .meditation-circle {
            width: 200px;
            height: 200px;
            border: 6px solid var(--light-blue);
            border-radius: 50%;
            margin: 2rem auto;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            background: linear-gradient(135deg, var(--creamy-white), var(--pastel-orange));
        }

        .meditation-circle.active {
            animation: meditate 4s ease-in-out infinite;
        }

        @keyframes meditate {
            0%, 100% { 
                transform: scale(1);
                box-shadow: 0 0 0 0 rgba(184, 230, 240, 0.7);
            }
            50% { 
                transform: scale(1.05);
                box-shadow: 0 0 0 20px rgba(184, 230, 240, 0);
            }
        }

        .meditation-controls {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .timer-options {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin: 1rem 0;
            flex-wrap: wrap;
        }

        .timer-btn {
            background: var(--light-blue);
            color: var(--text-dark);
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .timer-btn:hover, .timer-btn.active {
            background: var(--ocean-blue);
            color: white;
        }

        .music-controls {
            margin: 1.5rem 0;
        }

        .music-btn {
            background: var(--pastel-orange);
            color: var(--text-dark);
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            margin: 0 0.5rem;
        }

        .music-btn:hover {
            background: var(--coral);
            color: white;
        }

        .music-btn.active {
            background: var(--sage-green);
            color: white;
        }

        .meditation-quote {
            font-style: italic;
            color: var(--text-light);
            margin: 1.5rem 0;
            font-size: 1.1rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-menu {
                position: fixed;
                top: 100%;
                left: 0;
                width: 100%;
                background: var(--creamy-white);
                flex-direction: column;
                padding: 2rem;
                box-shadow: 0 5px 15px rgba(0,0,0,0.1);
                transform: translateY(-100%);
                opacity: 0;
                visibility: hidden;
                transition: all 0.3s ease;
            }

            .nav-menu.active {
                transform: translateY(0);
                opacity: 1;
                visibility: visible;
            }

            .mobile-menu-btn {
                display: block;
            }

            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
                gap: 2rem;
            }

            .hero-text h1 {
                font-size: 2.5rem;
            }

            .about-content {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .features-grid {
                grid-template-columns: 1fr;
            }

            .chatbot-window {
                width: 90%;
                right: 5%;
                left: 5%;
            }

            .hero-buttons {
                justify-content: center;
            }
        }

        @media (max-width: 480px) {
            .hero-text h1 {
                font-size: 2rem;
            }

            .section-header h2 {
                font-size: 2rem;
            }

            .login-container {
                padding: 2rem;
                margin: 1rem;
            }
        }

        /* Login Gate Styles */
        .login-gate {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, var(--deep-blue) 0%, var(--ocean-blue) 50%, var(--light-blue) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            transition: all 0.5s ease;
        }

        .login-gate.hidden {
            opacity: 0;
            visibility: hidden;
            pointer-events: none;
        }

        .login-gate-container {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 3rem;
            border-radius: 25px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            width: 100%;
            max-width: 450px;
            text-align: center;
            animation: slideIn 0.6s ease-out;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .login-gate-logo {
            font-family: 'Poppins', sans-serif;
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--deep-blue);
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .login-gate-logo i {
            color: var(--coral);
            font-size: 3rem;
        }

        .login-gate-subtitle {
            color: var(--text-light);
            margin-bottom: 2rem;
            font-size: 1.1rem;
        }

        .auth-tabs {
            display: flex;
            margin-bottom: 2rem;
            background: var(--soft-gray);
            border-radius: 25px;
            padding: 0.25rem;
        }

        .auth-tab {
            flex: 1;
            padding: 0.75rem;
            border: none;
            background: transparent;
            border-radius: 20px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            color: var(--text-dark);
        }

        .auth-tab.active {
            background: white;
            color: var(--deep-blue);
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .auth-form {
            display: none;
        }

        .auth-form.active {
            display: block;
        }

        .form-group {
            margin-bottom: 1.5rem;
            text-align: left;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--text-dark);
            font-weight: 500;
        }

        .form-group input {
            width: 100%;
            padding: 1rem;
            border: 2px solid var(--soft-gray);
            border-radius: 15px;
            font-size: 1rem;
            transition: all 0.3s ease;
            background: white;
            box-sizing: border-box;
        }

        .form-group input:focus {
            outline: none;
            border-color: var(--ocean-blue);
            box-shadow: 0 0 0 3px rgba(123, 179, 211, 0.1);
        }

        .auth-btn {
            width: 100%;
            background: linear-gradient(135deg, var(--ocean-blue), var(--deep-blue));
            color: white;
            padding: 1rem;
            border: none;
            border-radius: 15px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-bottom: 1rem;
        }

        .auth-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(123, 179, 211, 0.4);
        }

        .auth-btn:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none;
        }

        .guest-access {
            margin-top: 2rem;
            padding-top: 2rem;
            border-top: 1px solid var(--soft-gray);
        }

        .guest-btn {
            background: transparent;
            color: var(--deep-blue);
            border: 2px solid var(--deep-blue);
            padding: 0.75rem 1.5rem;
            border-radius: 25px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .guest-btn:hover {
            background: var(--deep-blue);
            color: white;
            transform: translateY(-2px);
        }

        .forgot-password {
            color: var(--deep-blue);
            text-decoration: none;
            font-size: 0.9rem;
            margin-top: 1rem;
            display: inline-block;
        }

        .forgot-password:hover {
            text-decoration: underline;
        }

        .main-website {
            transition: all 0.5s ease;
        }

        .main-website.hidden {
            opacity: 0;
            pointer-events: none;
        }

        /* Utility Classes */
        .hidden { display: none !important; }
        .text-center { text-align: center; }
        .mb-1 { margin-bottom: 0.5rem; }
        .mb-2 { margin-bottom: 1rem; }
        .mb-3 { margin-bottom: 1.5rem; }
        .mt-2 { margin-top: 1rem; }
        .mt-3 { margin-top: 1.5rem; }
    </style>
</head>
<body>
    <!-- Login Gate -->
    <div class="login-gate" id="loginGate">
        <div class="login-gate-container">
            <div class="login-gate-logo">
                <i class="fas fa-heart"></i>
                MindEase
            </div>
            <p class="login-gate-subtitle">Your Mental Wellness Companion</p>
            
            <div class="auth-tabs">
                <button class="auth-tab active" onclick="switchAuthTab('login')">Sign In</button>
                <button class="auth-tab" onclick="switchAuthTab('register')">Sign Up</button>
            </div>
            
            <!-- Login Form -->
            <form class="auth-form active" id="loginForm" onsubmit="handleLogin(event)">
                <div class="form-group">
                    <label for="loginEmail">Email Address</label>
                    <input type="email" id="loginEmail" name="email" required placeholder="Enter your email">
                </div>
                <div class="form-group">
                    <label for="loginPassword">Password</label>
                    <input type="password" id="loginPassword" name="password" required placeholder="Enter your password">
                </div>
                <button type="submit" class="auth-btn">Sign In</button>
                <a href="#" class="forgot-password" onclick="showForgotPassword()">Forgot your password?</a>
            </form>
            
            <!-- Register Form -->
            <form class="auth-form" id="registerForm" onsubmit="handleRegister(event)">
                <div class="form-group">
                    <label for="registerName">Full Name</label>
                    <input type="text" id="registerName" name="name" required placeholder="Enter your full name">
                </div>
                <div class="form-group">
                    <label for="registerEmail">Email Address</label>
                    <input type="email" id="registerEmail" name="email" required placeholder="Enter your email">
                </div>
                <div class="form-group">
                    <label for="registerPassword">Password</label>
                    <input type="password" id="registerPassword" name="password" required placeholder="Create a password" minlength="6">
                </div>
                <div class="form-group">
                    <label for="confirmPassword">Confirm Password</label>
                    <input type="password" id="confirmPassword" name="confirmPassword" required placeholder="Confirm your password">
                </div>
                <button type="submit" class="auth-btn">Create Account</button>
            </form>
            
            <div class="guest-access">
                <p style="color: var(--text-light); margin-bottom: 1rem;">Want to explore first?</p>
                <button class="guest-btn" onclick="enterAsGuest()">Continue as Guest</button>
            </div>
        </div>
    </div>

    <!-- Main Website Content -->
    <div class="main-website hidden" id="mainWebsite">
    <!-- Navigation -->
    <nav class="navbar">
        <div class="container">
            <div class="nav-container">
                <a href="#home" class="logo">
                    <i class="fas fa-heart"></i>
                    MindEase
                </a>
                <ul class="nav-menu" id="navMenu">
                    <li><a href="#home" class="nav-link">Home</a></li>
                    <li><a href="#about" class="nav-link">About</a></li>
                    <li><a href="#services" class="nav-link">Services</a></li>
                    <li><a href="#mood-tracker" class="nav-link">Mood Tracker</a></li>
                    <li><a href="#chatbot" class="nav-link">AI Assistant</a></li>
                    <li><span class="user-info" id="userInfo">Guest</span></li>
                    <li><a href="#" class="btn-primary" onclick="logout()">Logout</a></li>
                </ul>
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Your Journey to <span class="highlight">Mental Wellness</span> Starts Here</h1>
                    <p>MindEase provides compassionate support, interactive guidance, and professional resources to help you navigate life's challenges with confidence and peace.</p>
                    <div class="hero-buttons">
                        <!-- Removed Start Chatting button as requested -->
                    </div>
                </div>
                <div class="hero-image">
                    <div class="floating-card">
                        <h3><i class="fas fa-brain"></i> AI-Powered Support</h3>
                        <p>Get personalized guidance for anxiety, stress, and emotional wellness through our empathetic chatbot.</p>
                        <div class="mood-indicators">
                            <div class="mood-dot"></div>
                            <div class="mood-dot"></div>
                            <div class="mood-dot"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>About MindEase</h2>
                    <p>MindEase is a comprehensive mental health platform designed to provide accessible, compassionate support for individuals dealing with anxiety, stress, depression, and other emotional challenges.</p>
                    <p>Our mission is to create a safe, welcoming space where you can find the tools, resources, and guidance needed to improve your mental wellness and build resilience.</p>
                    <p>We believe that mental health support should be available to everyone, anytime, anywhere. That's why we've created an interactive platform that combines professional resources with AI-powered guidance.</p>
                </div>
                <div class="features-grid">
                    <div class="feature-item">
                        <i class="fas fa-robot"></i>
                        <h4>AI Chatbot Support</h4>
                        <p>24/7 empathetic conversations with our intelligent chatbot trained in mental health support.</p>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-heart-pulse"></i>
                        <h4>Guided Exercises</h4>
                        <p>Interactive breathing exercises, meditation, and mindfulness practices tailored to your needs.</p>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-users"></i>
                        <h4>Professional Resources</h4>
                        <p>Access to helpline numbers, crisis support, and connections to mental health professionals.</p>
                    </div>
                    <div class="feature-item">
                        <i class="fas fa-shield-heart"></i>
                        <h4>Safe & Confidential</h4>
                        <p>Your privacy is our priority. All conversations are secure and confidential.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-header">
                <h2>Our Services & Resources</h2>
                <p>Comprehensive mental health support designed to meet you wherever you are in your wellness journey.</p>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-comments"></i>
                    </div>
                    <h3>Interactive Chatbot</h3>
                    <p>Engage with our empathetic AI chatbot that provides personalized support for anxiety, stress, and emotional challenges. Available 24/7 for immediate assistance.</p>
                    <button class="btn-primary" onclick="openChatbot()">Start Chatting</button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-lungs"></i>
                    </div>
                    <h3>Breathing Exercises</h3>
                    <p>Guided breathing techniques to help manage anxiety and stress. Interactive exercises that you can follow along with in real-time.</p>
                    <button class="btn-primary" onclick="startBreathingExercise()">Try Now</button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-leaf"></i>
                    </div>
                    <h3>Mindfulness & Meditation</h3>
                    <p>Discover peace through guided mindfulness practices and meditation sessions designed to reduce stress and improve mental clarity.</p>
                    <button class="btn-primary" onclick="startMeditation()">Begin Practice</button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-phone-alt"></i>
                    </div>
                    <h3>Crisis Support</h3>
                    <p>Immediate access to crisis helplines and emergency resources. We're here to connect you with professional help when you need it most.</p>
                    <button class="btn-primary" onclick="showHelplines()">Get Help Now</button>
                </div>
            </div>

            <!-- Helpline Numbers -->
            <div class="helpline-numbers" id="helplineNumbers" style="display: none;">
                <h3><i class="fas fa-phone"></i> Emergency Helpline Numbers</h3>
                <div class="helpline-grid">
                    <div class="helpline-item">
                        <strong>National Suicide Prevention Lifeline</strong>
                        <a href="tel:988">988</a>
                        <p>24/7 Crisis Support</p>
                    </div>
                    <div class="helpline-item">
                        <strong>Crisis Text Line</strong>
                        <a href="sms:741741">Text HOME to 741741</a>
                        <p>Free 24/7 Text Support</p>
                    </div>
                    <div class="helpline-item">
                        <strong>SAMHSA National Helpline</strong>
                        <a href="tel:1-800-662-4357">1-800-662-HELP</a>
                        <p>Treatment Referral Service</p>
                    </div>
                    <div class="helpline-item">
                        <strong>National Alliance on Mental Illness</strong>
                        <a href="tel:1-800-950-6264">1-800-950-NAMI</a>
                        <p>Information & Support</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mood Tracker Section -->
    <section id="mood-tracker" class="services">
        <div class="container">
            <div class="section-header">
                <h2>📊 Daily Mood Tracker</h2>
                <p>Track your emotional wellness journey with a simple and effective mood tracking system.</p>
            </div>
            
            <div class="mood-tracker-container">
                <!-- Today's Mood Selection -->
                <div class="mood-selection-card">
                    <h3>How are you feeling today?</h3>
                    <p id="currentDate"></p>
                    
                    <div class="mood-options">
                        <div class="mood-option" data-mood="1" onclick="selectMood(1, '😢', 'Terrible')">
                            <div class="mood-emoji">�</div>
                            <span>Terrible</span>
                            <div class="mood-value">1</div>
                        </div>
                        <div class="mood-option" data-mood="2" onclick="selectMood(2, '😔', 'Low')">
                            <div class="mood-emoji">😔</div>
                            <span>Low</span>
                            <div class="mood-value">2</div>
                        </div>
                        <div class="mood-option" data-mood="3" onclick="selectMood(3, '😐', 'Okay')">
                            <div class="mood-emoji">😐</div>
                            <span>Okay</span>
                            <div class="mood-value">3</div>
                        </div>
                        <div class="mood-option" data-mood="4" onclick="selectMood(4, '😊', 'Good')">
                            <div class="mood-emoji">😊</div>
                            <span>Good</span>
                            <div class="mood-value">4</div>
                        </div>
                        <div class="mood-option" data-mood="5" onclick="selectMood(5, '😄', 'Excellent')">
                            <div class="mood-emoji">😄</div>
                            <span>Excellent</span>
                            <div class="mood-value">5</div>
                        </div>
                    </div>
                    
                    <div class="mood-note-section" id="moodNoteSection" style="display: none;">
                        <label for="moodNote">Add a note about your mood (optional):</label>
                        <textarea id="moodNote" placeholder="What's affecting your mood today?"></textarea>
                        <div class="mood-actions">
                            <button class="btn-primary" onclick="saveMood()">Save Mood</button>
                            <button class="btn-secondary" onclick="cancelMoodSelection()">Cancel</button>
                        </div>
                    </div>
                </div>
                
                <!-- Mood History with Bar Graph -->
                <div class="mood-history-card">
                    <h3>Your Mood History</h3>
                    <div class="mood-filter">
                        <button class="filter-btn active" onclick="filterMoodHistory('week')">Last 7 Days</button>
                        <button class="filter-btn" onclick="filterMoodHistory('month')">Last 30 Days</button>
                    </div>
                    
                    <div class="mood-bar-chart" id="moodBarChart">
                        <div class="no-data">
                            <i class="fas fa-chart-bar"></i>
                            <p>Start tracking your mood to see your progress!</p>
                        </div>
                    </div>
                    
                    <div class="mood-stats" id="moodStats" style="display: none;">
                        <div class="stat-item">
                            <span class="stat-label">Average Mood:</span>
                            <span class="stat-value" id="averageMood">-</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-label">Total Days:</span>
                            <span class="stat-value" id="totalDays">-</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-label">Best Day:</span>
                            <span class="stat-value" id="bestDay">-</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Chatbot Section -->
    <section id="chatbot" class="services">
        <div class="container">
            <div class="section-header">
                <h2>🤖 AI Mental Health Assistant</h2>
                <p>Meet your personal AI companion designed to provide empathetic support, guidance, and interactive wellness exercises 24/7.</p>
            </div>
            
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-microphone"></i>
                    </div>
                    <h3>Voice Interaction</h3>
                    <p>Speak naturally with our AI assistant. Use voice commands to share your feelings and receive spoken responses for a more personal experience.</p>
                    <button class="btn-primary" onclick="demonstrateVoice()">Try Voice Demo</button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3>Emotion Recognition</h3>
                    <p>Our AI understands your emotional state and provides personalized responses, coping strategies, and exercises tailored to your needs.</p>
                    <button class="btn-primary" onclick="demonstrateEmotion()">See How It Works</button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-heart-pulse"></i>
                    </div>
                    <h3>Interactive Exercises</h3>
                    <p>Get guided through breathing exercises, meditation sessions, and mindfulness practices with real-time visual and audio guidance.</p>
                    <button class="btn-primary" onclick="startBreathingExercise()">Try Exercise</button>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shield-heart"></i>
                    </div>
                    <h3>Crisis Support</h3>
                    <p>Immediate recognition of crisis situations with instant access to professional helplines and emergency resources.</p>
                    <button class="btn-primary" onclick="showHelplines()">View Resources</button>
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 3rem; padding: 2rem; background: white; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.1);">
                <h3 style="font-family: 'Poppins', sans-serif; color: var(--text-dark); margin-bottom: 1rem;">Start Your Conversation</h3>
                <p style="color: var(--text-light); margin-bottom: 2rem;">Experience compassionate AI support right now. Click below to begin chatting with your mental health assistant.</p>
                <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;">
                    <button class="btn-primary" onclick="openChatbot()" style="font-size: 1.2rem; padding: 1rem 2rem;">
                        <i class="fas fa-comments"></i> Start Chatting Now
                    </button>
                    <button class="btn-secondary" onclick="openChatbotWithVoice()" style="font-size: 1.2rem; padding: 1rem 2rem;">
                        <i class="fas fa-microphone"></i> Start with Voice
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Chatbot -->
    <div class="chatbot-container">
        <button class="chatbot-toggle" id="chatbotToggle" onclick="toggleChatbot()">
            <i class="fas fa-comments"></i>
        </button>
        
        <div class="chatbot-window" id="chatbotWindow">
            <div class="chatbot-header">
                <div class="chatbot-avatar">
                    <i class="fas fa-robot"></i>
                </div>
                <div class="chatbot-info">
                    <h4>MindEase Assistant</h4>
                    <p>Here to support you</p>
                </div>
                <button onclick="closeChatbot()" style="margin-left: auto; background: none; border: none; color: white; font-size: 1.2rem; cursor: pointer;">
                    <i class="fas fa-times"></i>
                </button>
            </div>
            
            <div class="chatbot-messages" id="chatbotMessages">
                <div class="message bot">
                    <div class="message-avatar">🤖</div>
                    <div class="message-bubble">
                        Hello! I'm your MindEase assistant. I'm here to provide support and guidance for your mental wellness journey. How are you feeling today?
                        <br><br>
                        <small>💡 Tip: Click the speaker button (🔊) to enable voice responses, or use the microphone (🎤) for voice input!</small>
                        <div class="exercise-suggestions">
                            <button class="exercise-btn" onclick="respondToBot('I feel anxious')">Anxious</button>
                            <button class="exercise-btn" onclick="respondToBot('I feel stressed')">Stressed</button>
                            <button class="exercise-btn" onclick="respondToBot('I feel sad')">Sad</button>
                            <button class="exercise-btn" onclick="respondToBot('I feel okay')">Okay</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="chatbot-input">
                <input type="text" id="chatInput" placeholder="Type your message..." onkeypress="handleChatKeyPress(event)">
                <button onclick="sendMessage()">
                    <i class="fas fa-paper-plane"></i>
                </button>
                <button class="voice-btn" id="voiceBtn" onclick="toggleVoiceInput()" title="Voice input">
                    <i class="fas fa-microphone"></i>
                </button>
                <button class="voice-btn" id="voiceToggle" onclick="toggleVoiceResponses()" title="Voice responses OFF - Click to turn ON">
                    <i class="fas fa-volume-mute"></i>
                </button>
            </div>
        </div>
    </div>

    <!-- Exercise Modal -->
    <div class="exercise-modal" id="exerciseModal">
        <div class="exercise-content">
            <h3 id="exerciseTitle">Breathing Exercise</h3>
            <p id="exerciseDescription">Follow the circle: Inhale for 5 seconds, hold for 5 seconds, exhale for 5 seconds</p>
            
            <div class="breathing-circle" id="breathingCircle">
                <span id="breathingText">Breathe</span>
            </div>
            
            <div class="exercise-controls">
                <button class="btn-secondary" onclick="closeExercise()">Close</button>
                <button class="btn-primary" id="exerciseBtn" onclick="toggleExercise()">Start</button>
            </div>
        </div>
    </div>

    <!-- Meditation Modal -->
    <div class="meditation-modal" id="meditationModal">
        <div class="meditation-content">
            <h3>🧘‍♀️ Mindful Meditation</h3>
            <p>Find your inner peace with guided meditation</p>
            
            <div class="timer-options">
                <button class="timer-btn active" onclick="setMeditationTime(5)">5 min</button>
                <button class="timer-btn" onclick="setMeditationTime(10)">10 min</button>
                <button class="timer-btn" onclick="setMeditationTime(15)">15 min</button>
                <button class="timer-btn" onclick="setMeditationTime(20)">20 min</button>
            </div>
            
            <div class="meditation-timer" id="meditationTimer">05:00</div>
            
            <div class="meditation-circle" id="meditationCircle">
                <i class="fas fa-leaf" style="font-size: 3rem; color: var(--sage-green);"></i>
            </div>
            
            <div class="meditation-quote" id="meditationQuote">
                "Peace comes from within. Do not seek it without." - Buddha
            </div>
            
            <div class="music-controls">
                <button class="music-btn active" id="meditationMusicBtn" onclick="toggleMeditationMusic('meditation')">🧘‍♀️ Inner Peace</button>
                <button class="music-btn" id="silenceBtn" onclick="toggleMeditationMusic('silence')">🤫 Silence</button>
            </div>
            
            <div class="meditation-controls">
                <button class="btn-secondary" onclick="closeMeditation()">Close</button>
                <button class="btn-primary" id="meditationBtn" onclick="toggleMeditation()">Start</button>
            </div>
        </div>
    </div>

    </div>
    <!-- End Main Website Content -->

    <script>
        // Global variables
        let chatbotOpen = false;
        let exerciseActive = false;
        let exerciseInterval;
        let breathingPhase = 'inhale';
        let meditationActive = false;
        let meditationTimer = null;
        let meditationTime = 5; // minutes
        let meditationTimeLeft = 300; // seconds
        let currentMeditationMusic = 'meditation';
        let meditationAudio = null;
        let isListening = false;
        let isSpeaking = false;
        let voiceEnabled = false; // Voice responses disabled by default
        let recognition = null;
        let speechSynthesis = window.speechSynthesis;

        // Mood tracking variables
        let selectedMood = null;
        let moodData = JSON.parse(localStorage.getItem('mindeaseMoodData')) || [];
        let currentFilter = 'week';

        // Authentication variables
        let isAuthenticated = false;
        let currentUser = null;

        // Meditation quotes
        const meditationQuotes = [
            "Peace comes from within. Do not seek it without. - Buddha",
            "The present moment is the only time over which we have dominion. - Thich Nhat Hanh",
            "Meditation is not evasion; it is a serene encounter with reality. - Thich Nhat Hanh",
            "Your calm mind is the ultimate weapon against your challenges. - Bryant McGill",
            "In the midst of movement and chaos, keep stillness inside of you. - Deepak Chopra",
            "The quieter you become, the more able you are to hear. - Rumi",
            "Meditation is the tongue of the soul and the language of our spirit. - Jeremy Taylor",
            "Be still and know. - Psalm 46:10"
        ];

        // Initialize speech recognition
        function initializeSpeechRecognition() {
            if ('webkitSpeechRecognition' in window || 'SpeechRecognition' in window) {
                const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
                recognition = new SpeechRecognition();
                recognition.continuous = false;
                recognition.interimResults = false;
                recognition.lang = 'en-US';
                
                recognition.onstart = function() {
                    isListening = true;
                    updateVoiceButton();
                };
                
                recognition.onresult = function(event) {
                    const transcript = event.results[0][0].transcript;
                    document.getElementById('chatInput').value = transcript;
                    sendMessage();
                };
                
                recognition.onerror = function(event) {
                    console.error('Speech recognition error:', event.error);
                    isListening = false;
                    updateVoiceButton();
                };
                
                recognition.onend = function() {
                    isListening = false;
                    updateVoiceButton();
                };
            }
        }

        // Voice input functionality
        function toggleVoiceInput() {
            if (!recognition) {
                initializeSpeechRecognition();
            }
            
            if (isListening) {
                recognition.stop();
            } else {
                recognition.start();
            }
        }

        function updateVoiceButton() {
            const voiceBtn = document.getElementById('voiceBtn');
            const voiceToggle = document.getElementById('voiceToggle');
            const icon = voiceBtn.querySelector('i');
            
            if (isListening) {
                voiceBtn.classList.add('listening');
                icon.className = 'fas fa-stop';
            } else if (isSpeaking) {
                voiceBtn.classList.add('speaking');
                icon.className = 'fas fa-volume-up';
            } else {
                voiceBtn.classList.remove('listening', 'speaking');
                icon.className = 'fas fa-microphone';
            }
            
            // Update voice toggle button
            if (voiceToggle) {
                const toggleIcon = voiceToggle.querySelector('i');
                if (voiceEnabled) {
                    voiceToggle.classList.add('active');
                    voiceToggle.title = 'Voice responses ON - Click to turn OFF';
                    toggleIcon.className = 'fas fa-volume-up';
                } else {
                    voiceToggle.classList.remove('active');
                    voiceToggle.title = 'Voice responses OFF - Click to turn ON';
                    toggleIcon.className = 'fas fa-volume-mute';
                }
            }
        }

        // Toggle voice responses on/off
        function toggleVoiceResponses() {
            voiceEnabled = !voiceEnabled;
            updateVoiceButton();
            
            // Stop any current speech
            if (!voiceEnabled && speechSynthesis.speaking) {
                speechSynthesis.cancel();
                isSpeaking = false;
                updateVoiceButton();
            }
            
            // Show feedback message
            const statusMessage = voiceEnabled ? 'Voice responses enabled 🔊' : 'Voice responses disabled 🔇';
            addMessage(statusMessage, 'bot');
        }

        // Text-to-speech functionality
        function speakText(text) {
            // Only speak if voice is enabled
            if (!voiceEnabled) return;
            
            if (speechSynthesis.speaking) {
                speechSynthesis.cancel();
            }
            
            const utterance = new SpeechSynthesisUtterance(text);
            utterance.rate = 0.8;
            utterance.pitch = 1;
            utterance.volume = 0.8;
            
            // Try to use a female voice for more calming effect
            const voices = speechSynthesis.getVoices();
            const femaleVoice = voices.find(voice => 
                voice.name.includes('Female') || 
                voice.name.includes('Samantha') || 
                voice.name.includes('Karen') ||
                voice.gender === 'female'
            );
            if (femaleVoice) {
                utterance.voice = femaleVoice;
            }
            
            utterance.onstart = function() {
                isSpeaking = true;
                updateVoiceButton();
            };
            
            utterance.onend = function() {
                isSpeaking = false;
                updateVoiceButton();
            };
            
            speechSynthesis.speak(utterance);
        }

        // Demo functions for chatbot section
        function demonstrateVoice() {
            openChatbot();
            setTimeout(() => {
                addMessage("Voice features: Click the microphone 🎤 to speak your message, and click the speaker button 🔊 to enable/disable voice responses.", 'bot');
            }, 1000);
        }

        function demonstrateEmotion() {
            openChatbot();
            setTimeout(() => {
                addMessage("I'm feeling really stressed about work", 'user');
                setTimeout(() => {
                    generateBotResponse("I'm feeling really stressed about work");
                }, 1500);
            }, 1000);
        }

        function openChatbotWithVoice() {
            openChatbot();
            setTimeout(() => {
                // Enable voice responses and show instructions
                voiceEnabled = true;
                updateVoiceButton();
                addMessage("Voice mode activated! 🔊 I'll now speak my responses. You can use the microphone to talk to me or type normally.", 'bot');
            }, 1000);
        }

        // Mobile menu toggle
        document.getElementById('mobileMenuBtn').addEventListener('click', function() {
            const navMenu = document.getElementById('navMenu');
            navMenu.classList.toggle('active');
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Show login section
        function showLogin() {
            document.getElementById('login').classList.remove('hidden');
            document.getElementById('login').scrollIntoView({ behavior: 'smooth' });
        }

        // Chatbot functionality
        function toggleChatbot() {
            const chatbotWindow = document.getElementById('chatbotWindow');
            const chatbotToggle = document.getElementById('chatbotToggle');
            
            if (chatbotOpen) {
                closeChatbot();
            } else {
                openChatbot();
            }
        }

        function openChatbot() {
            const chatbotWindow = document.getElementById('chatbotWindow');
            const chatbotToggle = document.getElementById('chatbotToggle');
            
            chatbotWindow.style.display = 'flex';
            chatbotToggle.innerHTML = '<i class="fas fa-times"></i>';
            chatbotOpen = true;
            
            // Focus on input
            setTimeout(() => {
                document.getElementById('chatInput').focus();
            }, 300);
        }

        function closeChatbot() {
            const chatbotWindow = document.getElementById('chatbotWindow');
            const chatbotToggle = document.getElementById('chatbotToggle');
            
            chatbotWindow.style.display = 'none';
            chatbotToggle.innerHTML = '<i class="fas fa-comments"></i>';
            chatbotOpen = false;
        }

        function sendMessage() {
            const input = document.getElementById('chatInput');
            const message = input.value.trim();
            
            if (message) {
                addMessage(message, 'user');
                input.value = '';
                
                // Show typing indicator
                showTypingIndicator();
                
                // Generate bot response
                setTimeout(() => {
                    hideTypingIndicator();
                    generateBotResponse(message);
                }, 1000 + Math.random() * 2000);
            }
        }

        function respondToBot(message) {
            addMessage(message, 'user');
            
            // Show typing indicator
            showTypingIndicator();
            
            // Generate bot response
            setTimeout(() => {
                hideTypingIndicator();
                generateBotResponse(message);
            }, 1000 + Math.random() * 2000);
        }

        function handleChatKeyPress(event) {
            if (event.key === 'Enter') {
                sendMessage();
            }
        }

        function addMessage(message, sender) {
            const messagesContainer = document.getElementById('chatbotMessages');
            const messageDiv = document.createElement('div');
            messageDiv.className = `message ${sender}`;
            
            const avatar = sender === 'user' ? '👤' : '🤖';
            
            messageDiv.innerHTML = `
                <div class="message-avatar">${avatar}</div>
                <div class="message-bubble">${message}</div>
            `;
            
            messagesContainer.appendChild(messageDiv);
            messagesContainer.scrollTop = messagesContainer.scrollHeight;
            
            // Speak the bot response if it's from the bot
            if (sender === 'bot') {
                // Clean the message for speech (remove HTML and special characters)
                const cleanMessage = message.replace(/<[^>]*>/g, '').replace(/[🤖💙🆘]/g, '');
                speakText(cleanMessage);
            }
        }

        function showTypingIndicator() {
            const messagesContainer = document.getElementById('chatbotMessages');
            const typingDiv = document.createElement('div');
            typingDiv.className = 'message bot';
            typingDiv.id = 'typingIndicator';
            
            typingDiv.innerHTML = `
                <div class="message-avatar">🤖</div>
                <div class="message-bubble">
                    <div class="typing-indicator">
                        <div class="typing-dot"></div>
                        <div class="typing-dot"></div>
                        <div class="typing-dot"></div>
                    </div>
                </div>
            `;
            
            messagesContainer.appendChild(typingDiv);
            messagesContainer.scrollTop = messagesContainer.scrollHeight;
        }

        function hideTypingIndicator() {
            const typingIndicator = document.getElementById('typingIndicator');
            if (typingIndicator) {
                typingIndicator.remove();
            }
        }

        function generateBotResponse(userMessage) {
            const message = userMessage.toLowerCase();
            let response = '';
            let suggestions = [];

            // Emotion detection and responses
            if (message.includes('anxious') || message.includes('anxiety') || message.includes('worried')) {
                response = "I understand you're feeling anxious. That's completely normal and you're not alone. Anxiety can feel overwhelming, but there are techniques that can help you feel more grounded and calm.";
                suggestions = [
                    { text: 'Breathing Exercise', action: 'startBreathingExercise()' },
                    { text: 'Anxiety Tips', action: 'showAnxietyTips()' },
                    { text: 'Grounding Technique', action: 'startGrounding()' },
                    { text: 'Quick Calm Methods', action: 'showQuickCalmTips()' }
                ];
            } else if (message.includes('stressed') || message.includes('stress') || message.includes('overwhelmed')) {
                response = "Stress can feel really heavy sometimes. It's important to acknowledge what you're going through. Let's work together to find some relief and help you feel more balanced.";
                suggestions = [
                    { text: 'Stress Relief Tips', action: 'showStressTips()' },
                    { text: 'Breathing Exercise', action: 'startBreathingExercise()' },
                    { text: 'Mindfulness Practice', action: 'startMeditation()' },
                    { text: 'Quick Stress Busters', action: 'showQuickStressBusters()' }
                ];
            } else if (message.includes('sad') || message.includes('depressed') || message.includes('down')) {
                response = "I hear that you're feeling sad, and I want you to know that your feelings are valid. It's okay to not be okay sometimes. You're taking a positive step by reaching out.";
                suggestions = [
                    { text: 'Mood Boosting Tips', action: 'showHappinessTips()' },
                    { text: 'Self-Care Activities', action: 'showSelfCareTips()' },
                    { text: 'Gentle Breathing', action: 'startBreathingExercise()' },
                    { text: 'Professional Help', action: 'showHelplines()' }
                ];
            } else if (message.includes('angry') || message.includes('mad') || message.includes('frustrated')) {
                response = "I can sense your frustration and anger. These are valid emotions, and it's important to process them in healthy ways. Let me help you find some techniques to manage these feelings.";
                suggestions = [
                    { text: 'Anger Management', action: 'showAngerTips()' },
                    { text: 'Calming Breathing', action: 'startBreathingExercise()' },
                    { text: 'Physical Release', action: 'showPhysicalReleaseTips()' },
                    { text: 'Mindful Pause', action: 'showMindfulPauseTips()' }
                ];
            } else if (message.includes('lonely') || message.includes('alone') || message.includes('isolated')) {
                response = "Feeling lonely can be really painful. You're not alone in experiencing this, and reaching out shows strength. Let's explore some ways to help you feel more connected.";
                suggestions = [
                    { text: 'Connection Tips', action: 'showConnectionTips()' },
                    { text: 'Self-Compassion', action: 'showSelfCompassionTips()' },
                    { text: 'Social Activities', action: 'showSocialTips()' },
                    { text: 'Positive Affirmations', action: 'showAffirmations()' }
                ];
            } else if (message.includes('happy') || message.includes('good') || message.includes('great') || message.includes('joy')) {
                response = "It's wonderful to hear you're feeling positive! Happiness is precious, and it's great that you're experiencing it. Let's explore ways to maintain and enhance these good feelings.";
                suggestions = [
                    { text: 'Happiness Tips', action: 'showHappinessTips()' },
                    { text: 'Gratitude Practice', action: 'showGratitudeTips()' },
                    { text: 'Mindful Meditation', action: 'startMeditation()' },
                    { text: 'Share Joy Tips', action: 'showJoyTips()' }
                ];
            } else if (message.includes('tired') || message.includes('exhausted') || message.includes('fatigue')) {
                response = "Feeling tired or exhausted can affect both your physical and mental wellbeing. It's important to listen to your body and mind. Let me share some strategies to help restore your energy.";
                suggestions = [
                    { text: 'Energy Boosting Tips', action: 'showEnergyTips()' },
                    { text: 'Rest & Recovery', action: 'showRestTips()' },
                    { text: 'Gentle Movement', action: 'showGentleMovementTips()' },
                    { text: 'Sleep Hygiene', action: 'showSleepTips()' }
                ];
            } else if (message.includes('okay') || message.includes('fine') || message.includes('good')) {
                response = "I'm glad to hear you're feeling okay! It's wonderful when we have moments of stability. Is there anything specific you'd like to work on or any way I can support your continued wellness?";
                suggestions = [
                    { text: 'Daily Mindfulness', action: 'startMeditation()' },
                    { text: 'Wellness Tips', action: 'respondToBot("How can I maintain good mental health?")' },
                    { text: 'Breathing Practice', action: 'startBreathingExercise()' }
                ];
            } else if (message.includes('help') || message.includes('crisis') || message.includes('emergency')) {
                response = "I'm concerned about you and want to make sure you get the support you need. Please know that there are people who care and want to help. Here are some immediate resources:";
                suggestions = [
                    { text: 'Call 988 (Crisis Line)', action: 'window.open("tel:988")' },
                    { text: 'Text Crisis Line', action: 'window.open("sms:741741")' },
                    { text: 'More Resources', action: 'showHelplines()' }
                ];
            } else if (message.includes('breathing') || message.includes('breathe')) {
                response = "Breathing exercises are a wonderful way to calm your nervous system and reduce stress. Would you like to try a guided breathing exercise with me?";
                suggestions = [
                    { text: 'Start Breathing Exercise', action: 'startBreathingExercise()' },
                    { text: 'Learn About Breathing', action: 'respondToBot("Tell me about breathing techniques")' }
                ];
            } else if (message.includes('mood') || message.includes('track') || message.includes('feeling')) {
                const recentMood = moodData.length > 0 ? moodData[moodData.length - 1] : null;
                if (recentMood) {
                    const moodDate = new Date(recentMood.date).toLocaleDateString();
                    response = `I see you've been tracking your mood! Your last entry was "${recentMood.moodText}" (${recentMood.moodValue}/5) on ${moodDate}. ${recentMood.note ? `You noted: "${recentMood.note}". ` : ''}How are you feeling right now?`;
                } else {
                    response = "I'd love to help you track your mood! Have you tried our mood tracker? It's a great way to understand your emotional patterns over time.";
                }
                suggestions = [
                    { text: 'Open Mood Tracker', action: 'document.getElementById("mood-tracker").scrollIntoView({behavior: "smooth"})' },
                    { text: 'I feel good today', action: 'respondToBot("I feel good today")' },
                    { text: 'I feel stressed', action: 'respondToBot("I feel stressed")' },
                    { text: 'Mood Tips', action: 'showMoodTrackingTips()' }
                ];
            } else if (message.includes('thank') || message.includes('thanks')) {
                response = "You're very welcome! I'm here whenever you need support. Remember, taking care of your mental health is a sign of strength, not weakness. You're doing great by reaching out.";
                suggestions = [
                    { text: 'Daily Check-in', action: 'respondToBot("How should I check in with myself daily?")' },
                    { text: 'More Resources', action: 'showHelplines()' }
                ];
            } else {
                response = "Thank you for sharing with me. I'm here to listen and support you. Every feeling you have is valid, and it's okay to take things one step at a time. How can I best help you right now?";
                suggestions = [
                    { text: 'Breathing Exercise', action: 'startBreathingExercise()' },
                    { text: 'Meditation', action: 'startMeditation()' },
                    { text: 'Talk About Feelings', action: 'respondToBot("I want to talk about my feelings")' },
                    { text: 'Get Resources', action: 'showHelplines()' }
                ];
            }

            // Add the response
            const messagesContainer = document.getElementById('chatbotMessages');
            const messageDiv = document.createElement('div');
            messageDiv.className = 'message bot';
            
            let suggestionsHTML = '';
            if (suggestions.length > 0) {
                suggestionsHTML = '<div class="exercise-suggestions">';
                suggestions.forEach(suggestion => {
                    suggestionsHTML += `<button class="exercise-btn" onclick="${suggestion.action}">${suggestion.text}</button>`;
                });
                suggestionsHTML += '</div>';
            }
            
            messageDiv.innerHTML = `
                <div class="message-avatar">🤖</div>
                <div class="message-bubble">
                    ${response}
                    ${suggestionsHTML}
                </div>
            `;
            
            messagesContainer.appendChild(messageDiv);
            messagesContainer.scrollTop = messagesContainer.scrollHeight;
        }

        // Exercise functions
        function startBreathingExercise() {
            document.getElementById('exerciseTitle').textContent = 'Breathing Exercise';
            document.getElementById('exerciseDescription').textContent = 'Follow the circle: Inhale as it expands, exhale as it contracts';
            document.getElementById('exerciseModal').style.display = 'flex';
        }

        function startMindfulness() {
            addMessage("Let's try a quick mindfulness exercise. Close your eyes and take three deep breaths. Notice five things you can hear around you right now. This helps ground you in the present moment.", 'bot');
        }

        // Meditation Functions
        function startMeditation() {
            document.getElementById('meditationModal').style.display = 'flex';
            // Set random quote
            const randomQuote = meditationQuotes[Math.floor(Math.random() * meditationQuotes.length)];
            document.getElementById('meditationQuote').textContent = randomQuote;
            
            // Start with meditation music by default
            currentMeditationMusic = 'meditation';
            document.getElementById('meditationMusicBtn').classList.add('active');
        }

        function setMeditationTime(minutes) {
            meditationTime = minutes;
            meditationTimeLeft = minutes * 60;
            updateMeditationDisplay();
            
            // Update active button
            document.querySelectorAll('.timer-btn').forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
        }

        function updateMeditationDisplay() {
            const minutes = Math.floor(meditationTimeLeft / 60);
            const seconds = meditationTimeLeft % 60;
            document.getElementById('meditationTimer').textContent = 
                `${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
        }

        function toggleMeditation() {
            const btn = document.getElementById('meditationBtn');
            const circle = document.getElementById('meditationCircle');
            
            if (!meditationActive) {
                // Start meditation
                meditationActive = true;
                btn.textContent = 'Pause';
                circle.classList.add('active');
                startMeditationTimer();
                
                // Start meditation music if selected
                if (currentMeditationMusic === 'meditation' && !meditationAudio) {
                    playMeditationAudio();
                }
            } else {
                // Pause meditation
                meditationActive = false;
                btn.textContent = 'Resume';
                circle.classList.remove('active');
                if (meditationTimer) {
                    clearInterval(meditationTimer);
                }
                if (meditationAudio) {
                    meditationAudio.pause();
                }
            }
        }

        function startMeditationTimer() {
            meditationTimer = setInterval(() => {
                if (meditationTimeLeft > 0) {
                    meditationTimeLeft--;
                    updateMeditationDisplay();
                } else {
                    // Meditation complete
                    completeMeditation();
                }
            }, 1000);
        }

        function toggleMeditationMusic(type) {
            // Remove active class from all music buttons
            document.querySelectorAll('.music-btn').forEach(btn => btn.classList.remove('active'));
            
            // Stop current music
            if (meditationAudio) {
                meditationAudio.pause();
                meditationAudio = null;
            }
            
            // If clicking the same type, just stop music
            if (currentMeditationMusic === type) {
                currentMeditationMusic = null;
                return;
            }
            
            // Set new music type and activate button
            currentMeditationMusic = type;
            if (type === 'meditation') {
                document.getElementById('meditationMusicBtn').classList.add('active');
                playMeditationAudio();
            } else if (type === 'silence') {
                document.getElementById('silenceBtn').classList.add('active');
            }
        }

        function playMeditationAudio() {
            meditationAudio = new Audio('https://www.freemeditation.com.au/wp-content/uploads/Bryan-Charles-Wilson-Inner-Peace-01-Namostute.mp3');
            meditationAudio.loop = true;
            meditationAudio.volume = 0.6;
            
            meditationAudio.play().catch(error => {
                console.log('Audio playback failed:', error);
                // Fallback: show message to user
                alert('Please click anywhere on the page first to enable audio playback, then try again.');
            });
        }

        function closeMeditation() {
            meditationActive = false;
            if (meditationTimer) {
                clearInterval(meditationTimer);
            }
            if (meditationAudio) {
                meditationAudio.pause();
                meditationAudio = null;
            }
            document.getElementById('meditationModal').style.display = 'none';
            document.getElementById('meditationBtn').textContent = 'Start';
            document.getElementById('meditationCircle').classList.remove('active');
            
            // Reset timer
            meditationTimeLeft = meditationTime * 60;
            updateMeditationDisplay();
            
            // Reset music buttons
            document.querySelectorAll('.music-btn').forEach(btn => btn.classList.remove('active'));
            document.getElementById('meditationMusicBtn').classList.add('active');
            currentMeditationMusic = 'meditation';
        }

        function completeMeditation() {
            meditationActive = false;
            clearInterval(meditationTimer);
            document.getElementById('meditationBtn').textContent = 'Start';
            document.getElementById('meditationCircle').classList.remove('active');
            
            // Stop meditation music
            if (meditationAudio) {
                meditationAudio.pause();
                meditationAudio = null;
            }
            
            // Show completion message
            alert('🧘‍♀️ Meditation complete! Well done on taking time for your mental wellness.');
            
            // Reset timer
            meditationTimeLeft = meditationTime * 60;
            updateMeditationDisplay();
        }

        // Tip functions for different emotions and situations
        function showAnxietyTips() {
            const tips = `
                <strong>🌸 Anxiety Management Tips:</strong><br><br>
                • <strong>5-4-3-2-1 Technique:</strong> Name 5 things you see, 4 you can touch, 3 you hear, 2 you smell, 1 you taste<br>
                • <strong>Progressive Muscle Relaxation:</strong> Tense and release each muscle group for 5 seconds<br>
                • <strong>Limit Caffeine:</strong> Reduce coffee, tea, and energy drinks<br>
                • <strong>Regular Exercise:</strong> Even 10 minutes of walking can help<br>
                • <strong>Journaling:</strong> Write down your worries to externalize them<br>
                • <strong>Deep Breathing:</strong> Inhale for 5, hold for 5, exhale for 5<br><br>
                Remember: Anxiety is temporary and manageable. You're stronger than you think! 💪
            `;
            addMessage(tips, 'bot');
        }

        function showStressTips() {
            const tips = `
                <strong>🌿 Stress Relief Strategies:</strong><br><br>
                • <strong>Time Management:</strong> Break large tasks into smaller, manageable steps<br>
                • <strong>Say No:</strong> It's okay to decline additional responsibilities<br>
                • <strong>Take Breaks:</strong> 5-10 minute breaks every hour<br>
                • <strong>Nature Therapy:</strong> Spend time outdoors or look at nature photos<br>
                • <strong>Laugh:</strong> Watch funny videos or call a friend who makes you smile<br>
                • <strong>Organize:</strong> Clean your space to clear your mind<br>
                • <strong>Listen to Music:</strong> Calming or uplifting songs can shift your mood<br><br>
                You've got this! Stress is manageable with the right tools. 🌟
            `;
            addMessage(tips, 'bot');
        }

        function showHappinessTips() {
            const tips = `
                <strong>😊 Mood Boosting Activities:</strong><br><br>
                • <strong>Gratitude List:</strong> Write 3 things you're grateful for daily<br>
                • <strong>Random Acts of Kindness:</strong> Help someone or give a compliment<br>
                • <strong>Connect with Loved Ones:</strong> Call, text, or hug someone you care about<br>
                • <strong>Do Something Creative:</strong> Draw, write, sing, or craft<br>
                • <strong>Get Moving:</strong> Dance, stretch, or take a walk<br>
                • <strong>Treat Yourself:</strong> Enjoy a favorite healthy snack or activity<br>
                • <strong>Celebrate Small Wins:</strong> Acknowledge your daily accomplishments<br><br>
                Happiness grows when shared and practiced! 🌈
            `;
            addMessage(tips, 'bot');
        }

        function showAngerTips() {
            const tips = `
                <strong>🔥 Anger Management Techniques:</strong><br><br>
                • <strong>Count to 10:</strong> Or 20, or 100 - give yourself time to cool down<br>
                • <strong>Physical Release:</strong> Do jumping jacks, punch a pillow, or go for a run<br>
                • <strong>Express Safely:</strong> Write in a journal or talk to a trusted friend<br>
                • <strong>Identify Triggers:</strong> Notice what situations make you angry<br>
                • <strong>Use "I" Statements:</strong> "I feel..." instead of "You always..."<br>
                • <strong>Take a Timeout:</strong> Remove yourself from the situation temporarily<br>
                • <strong>Practice Forgiveness:</strong> For others and yourself<br><br>
                Anger is a normal emotion. It's how we handle it that matters! 🕊️
            `;
            addMessage(tips, 'bot');
        }

        function showConnectionTips() {
            const tips = `
                <strong>💝 Building Connections:</strong><br><br>
                • <strong>Reach Out First:</strong> Send a text to an old friend<br>
                • <strong>Join Groups:</strong> Find clubs, classes, or volunteer opportunities<br>
                • <strong>Be Present:</strong> Put away devices during conversations<br>
                • <strong>Share Vulnerably:</strong> Open up about your experiences<br>
                • <strong>Listen Actively:</strong> Show genuine interest in others<br>
                • <strong>Online Communities:</strong> Join supportive forums or groups<br>
                • <strong>Pet Therapy:</strong> Spend time with animals if possible<br><br>
                Connection starts with small steps. You matter and belong! 🤗
            `;
            addMessage(tips, 'bot');
        }

        function showSelfCareTips() {
            const tips = `
                <strong>🛁 Self-Care Essentials:</strong><br><br>
                • <strong>Bubble Bath:</strong> Warm water with Epsom salts or essential oils<br>
                • <strong>Skincare Routine:</strong> Take time to pamper your skin<br>
                • <strong>Read for Pleasure:</strong> Escape into a good book<br>
                • <strong>Healthy Meals:</strong> Nourish your body with nutritious food<br>
                • <strong>Digital Detox:</strong> Take breaks from social media<br>
                • <strong>Comfortable Clothes:</strong> Wear something that makes you feel good<br>
                • <strong>Early Bedtime:</strong> Prioritize quality sleep<br><br>
                Self-care isn't selfish - it's necessary! You deserve love and care. 💖
            `;
            addMessage(tips, 'bot');
        }

        function showQuickCalmTips() {
            const tips = `
                <strong>⚡ Quick Calm Techniques (2-5 minutes):</strong><br><br>
                • <strong>Cold Water:</strong> Splash on face or hold ice cubes<br>
                • <strong>Humming:</strong> Hum your favorite tune to activate vagus nerve<br>
                • <strong>Shoulder Rolls:</strong> Release physical tension<br>
                • <strong>Smell Something Pleasant:</strong> Essential oils, flowers, or coffee<br>
                • <strong>Look Up:</strong> Literally look at the ceiling or sky<br>
                • <strong>Squeeze and Release:</strong> Clench fists tight, then release<br>
                • <strong>Name Colors:</strong> Look around and name every blue thing you see<br><br>
                These work in moments when you need instant relief! 🌸
            `;
            addMessage(tips, 'bot');
        }

        function showEnergyTips() {
            const tips = `
                <strong>⚡ Natural Energy Boosters:</strong><br><br>
                • <strong>Hydrate:</strong> Drink a full glass of water<br>
                • <strong>Power Nap:</strong> 10-20 minutes maximum<br>
                • <strong>Protein Snack:</strong> Nuts, yogurt, or hard-boiled egg<br>
                • <strong>Stretch:</strong> Simple neck and shoulder stretches<br>
                • <strong>Fresh Air:</strong> Step outside or open a window<br>
                • <strong>Upbeat Music:</strong> Listen to energizing songs<br>
                • <strong>Green Tea:</strong> Gentle caffeine with L-theanine<br><br>
                Small actions can create big energy shifts! 🔋
            `;
            addMessage(tips, 'bot');
        }

        function showGratitudeTips() {
            const tips = `
                <strong>🙏 Gratitude Practice Ideas:</strong><br><br>
                • <strong>Three Good Things:</strong> Write down 3 positive moments from today<br>
                • <strong>Gratitude Letter:</strong> Write to someone who helped you<br>
                • <strong>Photo Gratitude:</strong> Take pictures of things you appreciate<br>
                • <strong>Body Appreciation:</strong> Thank your body for what it does<br>
                • <strong>Small Moments:</strong> Notice tiny joys like warm coffee or sunshine<br>
                • <strong>Gratitude Walk:</strong> Appreciate nature while walking<br>
                • <strong>Before Sleep:</strong> End each day with grateful thoughts<br><br>
                Gratitude transforms ordinary moments into blessings! ✨
            `;
            addMessage(tips, 'bot');
        }

        function showQuickStressBusters() {
            const tips = `
                <strong>🚀 Instant Stress Busters:</strong><br><br>
                • <strong>Desk Push-ups:</strong> 10 quick push-ups against your desk<br>
                • <strong>Funny Video:</strong> Watch a 2-minute comedy clip<br>
                • <strong>Aromatherapy:</strong> Smell peppermint or lavender<br>
                • <strong>Positive Mantra:</strong> "This too shall pass" or "I am capable"<br>
                • <strong>Tidy Up:</strong> Organize one small area<br>
                • <strong>Call a Friend:</strong> 3-minute check-in with someone positive<br>
                • <strong>Chew Gum:</strong> Reduces cortisol and improves focus<br><br>
                Quick relief is always within reach! 🎯
            `;
            addMessage(tips, 'bot');
        }

        function showPhysicalReleaseTips() {
            const tips = `
                <strong>💪 Physical Release for Anger:</strong><br><br>
                • <strong>Punch a Pillow:</strong> Safe way to release physical tension<br>
                • <strong>Scream into a Pillow:</strong> Let it out without disturbing others<br>
                • <strong>Intense Exercise:</strong> Run, bike, or do burpees<br>
                • <strong>Squeeze a Stress Ball:</strong> Channel energy into your hands<br>
                • <strong>Tear Paper:</strong> Rip up old newspapers or magazines<br>
                • <strong>Dance Aggressively:</strong> Move your body to release energy<br>
                • <strong>Cold Shower:</strong> Shock your system to reset<br><br>
                Physical release helps process emotional energy safely! 🏃‍♀️
            `;
            addMessage(tips, 'bot');
        }

        function showMindfulPauseTips() {
            const tips = `
                <strong>🧘 Mindful Pause Techniques:</strong><br><br>
                • <strong>STOP Method:</strong> Stop, Take a breath, Observe, Proceed mindfully<br>
                • <strong>Body Scan:</strong> Notice tension from head to toe<br>
                • <strong>Breath Awareness:</strong> Focus only on your breathing for 1 minute<br>
                • <strong>Loving-Kindness:</strong> Send good wishes to yourself and others<br>
                • <strong>Present Moment:</strong> Notice 3 things you can see, hear, feel right now<br>
                • <strong>Gentle Self-Talk:</strong> Speak to yourself like a good friend<br>
                • <strong>Acceptance:</strong> "This feeling is temporary and will pass"<br><br>
                Mindful pauses create space between trigger and reaction! 🌱
            `;
            addMessage(tips, 'bot');
        }

        function showSelfCompassionTips() {
            const tips = `
                <strong>💕 Self-Compassion Practices:</strong><br><br>
                • <strong>Kind Inner Voice:</strong> Talk to yourself like you would a best friend<br>
                • <strong>Self-Forgiveness:</strong> "I'm human and I make mistakes"<br>
                • <strong>Comfort Touch:</strong> Place hand on heart or give yourself a hug<br>
                • <strong>Common Humanity:</strong> Remember others feel this way too<br>
                • <strong>Mindful Awareness:</strong> Notice self-criticism without judgment<br>
                • <strong>Self-Care Rituals:</strong> Do something nurturing for yourself<br>
                • <strong>Positive Affirmations:</strong> "I am worthy of love and kindness"<br><br>
                You deserve the same compassion you give others! 🤗
            `;
            addMessage(tips, 'bot');
        }

        function showSocialTips() {
            const tips = `
                <strong>👥 Social Connection Ideas:</strong><br><br>
                • <strong>Coffee Date:</strong> Invite someone for coffee or tea<br>
                • <strong>Group Activities:</strong> Join a book club, hiking group, or class<br>
                • <strong>Volunteer:</strong> Help others while meeting like-minded people<br>
                • <strong>Online Communities:</strong> Join forums about your interests<br>
                • <strong>Neighbor Connection:</strong> Introduce yourself to neighbors<br>
                • <strong>Workplace Socializing:</strong> Eat lunch with colleagues<br>
                • <strong>Family Time:</strong> Schedule regular calls or visits<br><br>
                Small social steps lead to meaningful connections! 🌟
            `;
            addMessage(tips, 'bot');
        }

        function showAffirmations() {
            const tips = `
                <strong>✨ Positive Affirmations:</strong><br><br>
                • "I am worthy of love and belonging"<br>
                • "I choose peace over worry"<br>
                • "I am stronger than my challenges"<br>
                • "I deserve happiness and joy"<br>
                • "I am enough, just as I am"<br>
                • "I trust in my ability to handle whatever comes"<br>
                • "I am surrounded by love and support"<br>
                • "Every day, I am growing and learning"<br><br>
                Repeat these daily to rewire your inner dialogue! 💫
            `;
            addMessage(tips, 'bot');
        }

        function showJoyTips() {
            const tips = `
                <strong>🎉 Spreading and Amplifying Joy:</strong><br><br>
                • <strong>Share Your Happiness:</strong> Tell someone about your good news<br>
                • <strong>Compliment Others:</strong> Spread positivity to brighten someone's day<br>
                • <strong>Capture the Moment:</strong> Take photos or journal about happy times<br>
                • <strong>Pay It Forward:</strong> Do something kind for a stranger<br>
                • <strong>Celebrate Small Wins:</strong> Acknowledge your daily achievements<br>
                • <strong>Create Joy Rituals:</strong> Dance, sing, or do something fun daily<br>
                • <strong>Gratitude Sharing:</strong> Tell people why you appreciate them<br><br>
                Joy multiplies when shared with others! 🌈
            `;
            addMessage(tips, 'bot');
        }

        function showRestTips() {
            const tips = `
                <strong>😴 Rest and Recovery Tips:</strong><br><br>
                • <strong>Power Nap:</strong> 10-20 minutes to recharge without grogginess<br>
                • <strong>Digital Sunset:</strong> No screens 1 hour before bed<br>
                • <strong>Cozy Environment:</strong> Dim lights, comfortable temperature<br>
                • <strong>Gentle Stretching:</strong> Light yoga or stretches before rest<br>
                • <strong>Herbal Tea:</strong> Chamomile or passionflower for relaxation<br>
                • <strong>Reading:</strong> Something light and enjoyable<br>
                • <strong>Progressive Relaxation:</strong> Tense and release each muscle group<br><br>
                Quality rest is essential for mental and physical health! 🛌
            `;
            addMessage(tips, 'bot');
        }

        function showGentleMovementTips() {
            const tips = `
                <strong>🚶‍♀️ Gentle Movement Ideas:</strong><br><br>
                • <strong>Slow Walk:</strong> 5-10 minutes at a comfortable pace<br>
                • <strong>Chair Stretches:</strong> Neck rolls, shoulder shrugs, ankle circles<br>
                • <strong>Tai Chi:</strong> Slow, flowing movements<br>
                • <strong>Gentle Yoga:</strong> Child's pose, cat-cow, gentle twists<br>
                • <strong>Deep Breathing with Arms:</strong> Raise arms on inhale, lower on exhale<br>
                • <strong>Wall Push-ups:</strong> Gentle strength movement<br>
                • <strong>Balance Practice:</strong> Stand on one foot for 30 seconds<br><br>
                Movement doesn't have to be intense to be beneficial! 🌿
            `;
            addMessage(tips, 'bot');
        }

        function showSleepTips() {
            const tips = `
                <strong>🌙 Better Sleep Hygiene:</strong><br><br>
                • <strong>Consistent Schedule:</strong> Same bedtime and wake time daily<br>
                • <strong>Cool, Dark Room:</strong> 65-68°F with blackout curtains<br>
                • <strong>No Caffeine After 2 PM:</strong> Avoid stimulants late in the day<br>
                • <strong>Bedtime Routine:</strong> 30-60 minutes of calming activities<br>
                • <strong>Comfortable Bedding:</strong> Invest in quality pillows and sheets<br>
                • <strong>White Noise:</strong> Fan, app, or earplugs for consistent sound<br>
                • <strong>Worry Journal:</strong> Write down concerns before bed<br><br>
                Good sleep is the foundation of mental wellness! 💤
            `;
            addMessage(tips, 'bot');
        }

        function startGrounding() {
            addMessage("Here's a grounding technique: Look around and name 5 things you can see, 4 things you can touch, 3 things you can hear, 2 things you can smell, and 1 thing you can taste. This helps bring you back to the present moment.", 'bot');
        }

        function toggleExercise() {
            const btn = document.getElementById('exerciseBtn');
            const circle = document.getElementById('breathingCircle');
            const text = document.getElementById('breathingText');
            
            if (!exerciseActive) {
                // Start exercise
                exerciseActive = true;
                btn.textContent = 'Stop';
                startBreathingAnimation();
            } else {
                // Stop exercise
                exerciseActive = false;
                btn.textContent = 'Start';
                stopBreathingAnimation();
            }
        }

        function startBreathingAnimation() {
            const circle = document.getElementById('breathingCircle');
            const text = document.getElementById('breathingText');
            
            function breathingCycle() {
                if (!exerciseActive) return;
                
                // Inhale phase (5 seconds)
                breathingPhase = 'inhale';
                text.textContent = 'Inhale...';
                circle.className = 'breathing-circle inhale';
                
                setTimeout(() => {
                    if (!exerciseActive) return;
                    
                    // Hold phase (5 seconds)
                    text.textContent = 'Hold...';
                    
                    setTimeout(() => {
                        if (!exerciseActive) return;
                        
                        // Exhale phase (5 seconds)
                        breathingPhase = 'exhale';
                        text.textContent = 'Exhale...';
                        circle.className = 'breathing-circle exhale';
                        
                        setTimeout(() => {
                            if (exerciseActive) {
                                breathingCycle(); // Repeat
                            }
                        }, 5000);
                    }, 5000);
                }, 5000);
            }
            
            breathingCycle();
        }

        function stopBreathingAnimation() {
            const circle = document.getElementById('breathingCircle');
            const text = document.getElementById('breathingText');
            
            circle.className = 'breathing-circle';
            text.textContent = 'Breathe';
        }

        function closeExercise() {
            exerciseActive = false;
            document.getElementById('exerciseModal').style.display = 'none';
            document.getElementById('exerciseBtn').textContent = 'Start';
            stopBreathingAnimation();
        }

        // Show helplines
        function showHelplines() {
            const helplineSection = document.getElementById('helplineNumbers');
            helplineSection.style.display = 'block';
            helplineSection.scrollIntoView({ behavior: 'smooth' });
        }

        // Navbar scroll effect
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 100) {
                navbar.style.background = 'rgba(255, 248, 240, 0.98)';
            } else {
                navbar.style.background = 'rgba(255, 248, 240, 0.95)';
            }
        });

        // Initialize chatbot with welcome message
        document.addEventListener('DOMContentLoaded', function() {
            // Check if user is already authenticated
            checkAuthentication();
            
            // Initialize speech recognition
            initializeSpeechRecognition();
            
            // Initialize voice button states
            updateVoiceButton();
            
            // Initialize mood tracker
            initializeMoodTracker();
            
            // Auto-open chatbot after 3 seconds for demo (only if authenticated)
            setTimeout(() => {
                if (isAuthenticated && !chatbotOpen) {
                    const toggle = document.getElementById('chatbotToggle');
                    if (toggle) {
                        toggle.style.animation = 'bounce 1s ease-in-out 3';
                    }
                }
            }, 3000);
        });

        // Authentication Functions
        function checkAuthentication() {
            const savedUser = localStorage.getItem('mindEaseUser');
            if (savedUser) {
                currentUser = JSON.parse(savedUser);
                isAuthenticated = true;
                showMainWebsite();
            } else {
                showLoginGate();
            }
        }

        function switchAuthTab(tab) {
            // Update tab buttons
            document.querySelectorAll('.auth-tab').forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            
            // Update forms
            document.querySelectorAll('.auth-form').forEach(form => form.classList.remove('active'));
            document.getElementById(tab + 'Form').classList.add('active');
        }

        function handleLogin(event) {
            event.preventDefault();
            
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;
            
            // Simple validation (in a real app, this would connect to a backend)
            if (email && password) {
                // Simulate authentication
                currentUser = {
                    name: email.split('@')[0], // Use part of email as name
                    email: email,
                    loginTime: new Date().toISOString(),
                    isGuest: false
                };
                
                // Save user data
                localStorage.setItem('mindEaseUser', JSON.stringify(currentUser));
                isAuthenticated = true;
                
                // Show success and transition to main site
                showLoginSuccess('Welcome back! Redirecting to MindEase...');
                setTimeout(() => {
                    showMainWebsite();
                }, 1500);
            } else {
                alert('Please fill in all fields.');
            }
        }

        function handleRegister(event) {
            event.preventDefault();
            
            const name = document.getElementById('registerName').value;
            const email = document.getElementById('registerEmail').value;
            const password = document.getElementById('registerPassword').value;
            const confirmPassword = document.getElementById('confirmPassword').value;
            
            // Validation
            if (!name || !email || !password || !confirmPassword) {
                alert('Please fill in all fields.');
                return;
            }
            
            if (password !== confirmPassword) {
                alert('Passwords do not match.');
                return;
            }
            
            if (password.length < 6) {
                alert('Password must be at least 6 characters long.');
                return;
            }
            
            // Simulate registration
            currentUser = {
                name: name,
                email: email,
                registrationTime: new Date().toISOString(),
                isGuest: false
            };
            
            // Save user data
            localStorage.setItem('mindEaseUser', JSON.stringify(currentUser));
            isAuthenticated = true;
            
            // Show success and transition to main site
            showLoginSuccess(`Welcome to MindEase, ${name}! Setting up your account...`);
            setTimeout(() => {
                showMainWebsite();
            }, 2000);
        }

        function enterAsGuest() {
            currentUser = {
                name: 'Guest User',
                email: null,
                isGuest: true,
                guestSession: new Date().toISOString()
            };
            
            isAuthenticated = true;
            
            // Show guest message and transition
            showLoginSuccess('Welcome, Guest! Exploring MindEase...');
            setTimeout(() => {
                showMainWebsite();
            }, 1500);
        }

        function showLoginSuccess(message) {
            const container = document.querySelector('.login-gate-container');
            container.innerHTML = `
                <div style="text-align: center; padding: 2rem;">
                    <div class="login-gate-logo">
                        <i class="fas fa-heart"></i>
                        MindEase
                    </div>
                    <div style="margin: 2rem 0;">
                        <i class="fas fa-check-circle" style="font-size: 3rem; color: var(--sage-green); margin-bottom: 1rem;"></i>
                        <p style="color: var(--text-dark); font-size: 1.1rem; margin: 0;">${message}</p>
                    </div>
                    <div style="width: 100%; height: 4px; background: var(--soft-gray); border-radius: 2px; overflow: hidden;">
                        <div style="width: 100%; height: 100%; background: linear-gradient(90deg, var(--ocean-blue), var(--sage-green)); animation: loading 1.5s ease-in-out;"></div>
                    </div>
                </div>
                <style>
                    @keyframes loading {
                        0% { transform: translateX(-100%); }
                        100% { transform: translateX(0); }
                    }
                </style>
            `;
        }

        function showLoginGate() {
            document.getElementById('loginGate').classList.remove('hidden');
            document.getElementById('mainWebsite').classList.add('hidden');
            
            // Reset user info in navigation
            const userInfo = document.getElementById('userInfo');
            if (userInfo) {
                userInfo.textContent = 'Guest';
            }
        }

        function showMainWebsite() {
            document.getElementById('loginGate').classList.add('hidden');
            document.getElementById('mainWebsite').classList.remove('hidden');
            
            // Update user info in navigation
            const userInfo = document.getElementById('userInfo');
            if (userInfo && currentUser) {
                userInfo.textContent = currentUser.isGuest ? 'Guest User' : currentUser.name;
            }
            
            // Update welcome message in chatbot if user is logged in
            if (currentUser && !currentUser.isGuest) {
                setTimeout(() => {
                    const welcomeMessage = document.querySelector('.message.bot .message-bubble');
                    if (welcomeMessage) {
                        welcomeMessage.innerHTML = `
                            Hello ${currentUser.name}! I'm your MindEase assistant. I'm here to provide support and guidance for your mental wellness journey. How are you feeling today?
                            <br><br>
                            <small>💡 Tip: Click the speaker button (🔊) to enable voice responses, or use the microphone (🎤) for voice input!</small>
                            <div class="exercise-suggestions">
                                <button class="exercise-btn" onclick="respondToBot('I feel anxious')">Anxious</button>
                                <button class="exercise-btn" onclick="respondToBot('I feel stressed')">Stressed</button>
                                <button class="exercise-btn" onclick="respondToBot('I feel sad')">Sad</button>
                                <button class="exercise-btn" onclick="respondToBot('I feel okay')">Okay</button>
                            </div>
                        `;
                    }
                }, 1000);
            }
        }

        function logout() {
            localStorage.removeItem('mindEaseUser');
            currentUser = null;
            isAuthenticated = false;
            
            // Reset any user-specific data
            if (speechSynthesis.speaking) {
                speechSynthesis.cancel();
            }
            
            // Close chatbot if open
            if (chatbotOpen) {
                closeChatbot();
            }
            
            // Reset voice settings
            voiceEnabled = false;
            isListening = false;
            isSpeaking = false;
            
            // Show logout message and then login gate
            showLogoutMessage();
            
            setTimeout(() => {
                // Reset login gate to original state
                resetLoginGate();
                // Show login gate again
                showLoginGate();
            }, 2000);
        }

        function showLogoutMessage() {
            const loginGate = document.getElementById('loginGate');
            loginGate.classList.remove('hidden');
            
            const container = document.querySelector('.login-gate-container');
            container.innerHTML = `
                <div style="text-align: center; padding: 2rem;">
                    <div class="login-gate-logo">
                        <i class="fas fa-heart"></i>
                        MindEase
                    </div>
                    <div style="margin: 2rem 0;">
                        <i class="fas fa-sign-out-alt" style="font-size: 3rem; color: var(--coral); margin-bottom: 1rem;"></i>
                        <h3 style="color: var(--text-dark); margin-bottom: 0.5rem;">Logged Out Successfully</h3>
                        <p style="color: var(--text-light); margin: 0;">Thank you for using MindEase. Take care of your mental wellness!</p>
                    </div>
                    <div style="width: 100%; height: 4px; background: var(--soft-gray); border-radius: 2px; overflow: hidden;">
                        <div style="width: 100%; height: 100%; background: linear-gradient(90deg, var(--coral), var(--pastel-orange)); animation: loading 2s ease-in-out;"></div>
                    </div>
                </div>
                <style>
                    @keyframes loading {
                        0% { transform: translateX(-100%); }
                        100% { transform: translateX(0); }
                    }
                </style>
            `;
        }

        function resetLoginGate() {
            const container = document.querySelector('.login-gate-container');
            container.innerHTML = `
                <div class="login-gate-logo">
                    <i class="fas fa-heart"></i>
                    MindEase
                </div>
                <p class="login-gate-subtitle">Your Mental Wellness Companion</p>
                
                <div class="auth-tabs">
                    <button class="auth-tab active" onclick="switchAuthTab('login')">Sign In</button>
                    <button class="auth-tab" onclick="switchAuthTab('register')">Sign Up</button>
                </div>
                
                <!-- Login Form -->
                <form class="auth-form active" id="loginForm" onsubmit="handleLogin(event)">
                    <div class="form-group">
                        <label for="loginEmail">Email Address</label>
                        <input type="email" id="loginEmail" name="email" required placeholder="Enter your email">
                    </div>
                    <div class="form-group">
                        <label for="loginPassword">Password</label>
                        <input type="password" id="loginPassword" name="password" required placeholder="Enter your password">
                    </div>
                    <button type="submit" class="auth-btn">Sign In</button>
                    <a href="#" class="forgot-password" onclick="showForgotPassword()">Forgot your password?</a>
                </form>
                
                <!-- Register Form -->
                <form class="auth-form" id="registerForm" onsubmit="handleRegister(event)">
                    <div class="form-group">
                        <label for="registerName">Full Name</label>
                        <input type="text" id="registerName" name="name" required placeholder="Enter your full name">
                    </div>
                    <div class="form-group">
                        <label for="registerEmail">Email Address</label>
                        <input type="email" id="registerEmail" name="email" required placeholder="Enter your email">
                    </div>
                    <div class="form-group">
                        <label for="registerPassword">Password</label>
                        <input type="password" id="registerPassword" name="password" required placeholder="Create a password" minlength="6">
                    </div>
                    <div class="form-group">
                        <label for="confirmPassword">Confirm Password</label>
                        <input type="password" id="confirmPassword" name="confirmPassword" required placeholder="Confirm your password">
                    </div>
                    <button type="submit" class="auth-btn">Create Account</button>
                </form>
                
                <div class="guest-access">
                    <p style="color: var(--text-light); margin-bottom: 1rem;">Want to explore first?</p>
                    <button class="guest-btn" onclick="enterAsGuest()">Continue as Guest</button>
                </div>
            `;
        }

        function showForgotPassword() {
            alert('Password reset functionality would be implemented here. For now, you can create a new account or continue as a guest.');
        }

        // Mood Tracker Functions
        function initializeMoodTracker() {
            // Set current date
            const today = new Date();
            const dateString = today.toLocaleDateString('en-US', { 
                weekday: 'long', 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric' 
            });
            document.getElementById('currentDate').textContent = dateString;
            
            // Check if mood already logged today
            checkTodaysMood();
            
            // Display mood history
            displayMoodBarChart();
            
            // Update stats
            updateMoodStats();
        }

        function checkTodaysMood() {
            const today = new Date().toDateString();
            const todaysMood = moodData.find(entry => new Date(entry.date).toDateString() === today);
            
            if (todaysMood) {
                // Highlight the selected mood
                const moodOption = document.querySelector(`[data-mood="${todaysMood.moodValue}"]`);
                if (moodOption) {
                    moodOption.classList.add('selected');
                }
                
                // Show a message that mood is already logged
                const moodSection = document.getElementById('moodNoteSection');
                moodSection.style.display = 'block';
                moodSection.innerHTML = `
                    <div style="text-align: center; padding: 1rem; background: var(--sage-green); color: white; border-radius: 10px;">
                        <i class="fas fa-check-circle"></i>
                        <p style="margin: 0.5rem 0 0 0;">Today's mood: <strong>${todaysMood.moodText}</strong> (${todaysMood.moodValue}/5)</p>
                        ${todaysMood.note ? `<p style="margin: 0.5rem 0 0 0; font-style: italic;">"${todaysMood.note}"</p>` : ''}
                        <button class="btn-secondary" onclick="updateTodaysMood()" style="margin-top: 1rem;">Update Mood</button>
                    </div>
                `;
            }
        }

        function selectMood(moodValue, emoji, moodText) {
            // Remove previous selection
            document.querySelectorAll('.mood-option').forEach(option => {
                option.classList.remove('selected');
            });
            
            // Select current mood
            const selectedOption = document.querySelector(`[data-mood="${moodValue}"]`);
            selectedOption.classList.add('selected');
            
            selectedMood = {
                moodValue: moodValue,
                emoji: emoji,
                moodText: moodText
            };
            
            // Show note section
            document.getElementById('moodNoteSection').style.display = 'block';
            document.getElementById('moodNoteSection').innerHTML = `
                <label for="moodNote">Add a note about your mood (optional):</label>
                <textarea id="moodNote" placeholder="What's affecting your mood today?"></textarea>
                <div class="mood-actions">
                    <button class="btn-primary" onclick="saveMood()">Save Mood</button>
                    <button class="btn-secondary" onclick="cancelMoodSelection()">Cancel</button>
                </div>
            `;
        }

        function saveMood() {
            if (!selectedMood) {
                alert('Please select a mood first!');
                return;
            }
            
            const note = document.getElementById('moodNote').value.trim();
            const today = new Date();
            const todayString = today.toDateString();
            
            // Check if mood already exists for today
            const existingIndex = moodData.findIndex(entry => new Date(entry.date).toDateString() === todayString);
            
            const moodEntry = {
                date: today.toISOString(),
                moodValue: selectedMood.moodValue,
                emoji: selectedMood.emoji,
                moodText: selectedMood.moodText,
                note: note,
                timestamp: Date.now()
            };
            
            if (existingIndex >= 0) {
                // Update existing entry
                moodData[existingIndex] = moodEntry;
            } else {
                // Add new entry
                moodData.push(moodEntry);
            }
            
            // Save to localStorage
            localStorage.setItem('mindeaseMoodData', JSON.stringify(moodData));
            
            // Show success message
            showMoodSavedMessage();
            
            // Update displays
            displayMoodBarChart();
            updateMoodStats();
            
            // Check today's mood again
            setTimeout(checkTodaysMood, 500);
        }

        function showMoodSavedMessage() {
            const moodSection = document.getElementById('moodNoteSection');
            moodSection.innerHTML = `
                <div style="text-align: center; padding: 2rem; background: var(--sage-green); color: white; border-radius: 10px;">
                    <i class="fas fa-heart" style="font-size: 2rem; margin-bottom: 1rem;"></i>
                    <h4 style="margin: 0 0 0.5rem 0;">Mood Saved!</h4>
                    <p style="margin: 0;">Keep tracking to see your progress over time!</p>
                </div>
            `;
            
            setTimeout(() => {
                moodSection.style.display = 'none';
                resetMoodSelection();
            }, 2000);
        }

        function cancelMoodSelection() {
            resetMoodSelection();
        }

        function resetMoodSelection() {
            selectedMood = null;
            document.getElementById('moodNoteSection').style.display = 'none';
            
            // Remove selections (except if already logged today)
            const today = new Date().toDateString();
            const todaysMood = moodData.find(entry => new Date(entry.date).toDateString() === today);
            
            if (!todaysMood) {
                document.querySelectorAll('.mood-option').forEach(option => {
                    option.classList.remove('selected');
                });
            }
        }

        function updateTodaysMood() {
            // Remove today's entry and allow re-selection
            const today = new Date().toDateString();
            moodData = moodData.filter(entry => new Date(entry.date).toDateString() !== today);
            localStorage.setItem('mindeaseMoodData', JSON.stringify(moodData));
            
            // Reset the interface
            document.querySelectorAll('.mood-option').forEach(option => {
                option.classList.remove('selected');
            });
            document.getElementById('moodNoteSection').style.display = 'none';
            
            // Update displays
            displayMoodBarChart();
            updateMoodStats();
        }

        function filterMoodHistory(period) {
            currentFilter = period;
            
            // Update active filter button
            document.querySelectorAll('.filter-btn').forEach(btn => btn.classList.remove('active'));
            event.target.classList.add('active');
            
            displayMoodBarChart();
        }

        function displayMoodBarChart() {
            const chartContainer = document.getElementById('moodBarChart');
            
            if (moodData.length === 0) {
                chartContainer.innerHTML = `
                    <div class="no-data">
                        <i class="fas fa-chart-bar"></i>
                        <p>Start tracking your mood to see your progress!</p>
                    </div>
                `;
                return;
            }
            
            // Filter data based on selected period
            let filteredData = [...moodData];
            const now = new Date();
            
            if (currentFilter === 'week') {
                const weekAgo = new Date(now.getTime() - 7 * 24 * 60 * 60 * 1000);
                filteredData = moodData.filter(entry => new Date(entry.date) >= weekAgo);
            } else if (currentFilter === 'month') {
                const monthAgo = new Date(now.getTime() - 30 * 24 * 60 * 60 * 1000);
                filteredData = moodData.filter(entry => new Date(entry.date) >= monthAgo);
            }
            
            if (filteredData.length === 0) {
                chartContainer.innerHTML = `
                    <div class="no-data">
                        <i class="fas fa-calendar"></i>
                        <p>No mood entries found for this period.</p>
                    </div>
                `;
                return;
            }
            
            // Sort by date (newest first)
            filteredData.sort((a, b) => new Date(b.date) - new Date(a.date));
            
            // Create bar chart
            const maxBars = currentFilter === 'week' ? 7 : 10; // Show max 10 bars for month view
            const displayData = filteredData.slice(0, maxBars);
            
            const barsHTML = displayData.map(entry => {
                const date = new Date(entry.date);
                const dateStr = date.toLocaleDateString('en-US', { 
                    month: 'short', 
                    day: 'numeric'
                });
                
                const barHeight = (entry.moodValue / 5) * 160; // Max height 160px
                
                return `
                    <div class="bar-item" title="${entry.moodText} - ${dateStr}${entry.note ? '\n' + entry.note : ''}">
                        <div class="bar-emoji">${entry.emoji}</div>
                        <div class="bar" style="height: ${barHeight}px;"></div>
                        <div class="bar-label">${dateStr}</div>
                        <div class="bar-value">${entry.moodValue}</div>
                    </div>
                `;
            }).join('');
            
            chartContainer.innerHTML = `
                <div class="bar-chart-container">
                    ${barsHTML}
                </div>
            `;
        }

        function updateMoodStats() {
            const statsContainer = document.getElementById('moodStats');
            
            if (moodData.length === 0) {
                statsContainer.style.display = 'none';
                return;
            }
            
            statsContainer.style.display = 'flex';
            
            // Calculate average mood
            const totalMood = moodData.reduce((sum, entry) => sum + entry.moodValue, 0);
            const averageMood = (totalMood / moodData.length).toFixed(1);
            
            // Find best day
            const bestEntry = moodData.reduce((best, entry) => 
                entry.moodValue > best.moodValue ? entry : best
            );
            const bestDate = new Date(bestEntry.date).toLocaleDateString('en-US', { 
                month: 'short', 
                day: 'numeric' 
            });
            
            // Update stats display
            document.getElementById('averageMood').textContent = `${averageMood}/5 ${bestEntry.emoji}`;
            document.getElementById('totalDays').textContent = moodData.length;
            document.getElementById('bestDay').textContent = `${bestDate} (${bestEntry.moodValue}/5)`;
        }

        function showMoodTrackingTips() {
            const tips = `
                <strong>📊 Mood Tracking Benefits:</strong><br><br>
                • <strong>Pattern Recognition:</strong> Identify what triggers good and bad moods<br>
                • <strong>Progress Tracking:</strong> See your emotional wellness journey over time<br>
                • <strong>Self-Awareness:</strong> Become more mindful of your emotional states<br>
                • <strong>Treatment Support:</strong> Share data with healthcare providers<br>
                • <strong>Goal Setting:</strong> Work towards more positive mood patterns<br>
                • <strong>Trigger Identification:</strong> Notice what affects your mental health<br><br>
                Visit our Mood Tracker section to start your journey! 📈
            `;
            addMessage(tips, 'bot');
        }

        // Close modal when clicking outside
        document.getElementById('exerciseModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeExercise();
            }
        });

        document.getElementById('meditationModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeMeditation();
            }
        });

        // Handle navigation for login
        document.querySelectorAll('a[href="#login"]').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                showLogin();
            });
        });
    </script>
</body>
</html>
