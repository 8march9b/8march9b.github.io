<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Поздравление наших любимых девочек</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=SF+Pro+Display:wght@300;400;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'SF Pro Display', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 25%, #f093fb 50%, #f5576c 75%, #ffd1ff 100%);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }

        /* Animated background particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 0;
            pointer-events: none;
        }

        .particle {
            position: absolute;
            width: 10px;
            height: 10px;
            background: rgba(255, 255, 255, 0.5);
            border-radius: 50%;
            animation: float 15s infinite;
            filter: blur(1px);
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) rotate(720deg);
                opacity: 0;
            }
        }

        /* Glass morphism base */
        .glass {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(20px) saturate(180%);
            -webkit-backdrop-filter: blur(20px) saturate(180%);
            border: 1px solid rgba(255, 255, 255, 0.4);
            border-radius: 24px;
            box-shadow: 
                0 8px 32px rgba(31, 38, 135, 0.2),
                inset 0 4px 20px rgba(255, 255, 255, 0.3),
                inset 0 -4px 20px rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .glass::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                45deg,
                transparent 30%,
                rgba(255, 255, 255, 0.3) 50%,
                transparent 70%
            );
            animation: shine 8s infinite;
            pointer-events: none;
        }

        @keyframes shine {
            0% {
                transform: translateX(-100%) translateY(-100%) rotate(45deg);
            }
            100% {
                transform: translateX(100%) translateY(100%) rotate(45deg);
            }
        }

        /* Liquid effect on hover */
        .liquid-hover {
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .liquid-hover:hover {
            transform: scale(1.02) translateY(-2px);
            background: rgba(255, 255, 255, 0.25);
            box-shadow: 
                0 20px 60px rgba(31, 38, 135, 0.3),
                inset 0 4px 30px rgba(255, 255, 255, 0.4),
                inset 0 -4px 30px rgba(255, 255, 255, 0.2);
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
            position: relative;
            z-index: 1;
        }

        /* Header */
        .header {
            text-align: center;
            margin-bottom: 50px;
            animation: fadeInDown 1s ease-out;
        }

        .header h1 {
            font-size: clamp(2rem, 5vw, 3.5rem);
            font-weight: 700;
            color: white;
            text-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            margin-bottom: 10px;
            letter-spacing: -0.02em;
        }

        .header .subtitle {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 300;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .march-8 {
            font-size: 4rem;
            margin: 20px 0;
            animation: pulse 2s infinite;
            filter: drop-shadow(0 4px 10px rgba(0,0,0,0.2));
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Grid layout for names */
        .girls-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .girl-card {
            padding: 25px;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 12px;
            animation: fadeInUp 0.6s ease-out backwards;
        }

        .girl-card:nth-child(1) { animation-delay: 0.1s; }
        .girl-card:nth-child(2) { animation-delay: 0.2s; }
        .girl-card:nth-child(3) { animation-delay: 0.3s; }
        .girl-card:nth-child(4) { animation-delay: 0.4s; }
        .girl-card:nth-child(5) { animation-delay: 0.5s; }
        .girl-card:nth-child(6) { animation-delay: 0.6s; }
        .girl-card:nth-child(7) { animation-delay: 0.7s; }
        .girl-card:nth-child(8) { animation-delay: 0.8s; }
        .girl-card:nth-child(9) { animation-delay: 0.9s; }
        .girl-card:nth-child(10) { animation-delay: 1.0s; }
        .girl-card:nth-child(11) { animation-delay: 1.1s; }
        .girl-card:nth-child(12) { animation-delay: 1.2s; }
        .girl-card:nth-child(13) { animation-delay: 1.3s; }

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

        .girl-avatar {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(255,255,255,0.4), rgba(255,255,255,0.1));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            border: 2px solid rgba(255, 255, 255, 0.5);
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .girl-card:hover .girl-avatar {
            transform: scale(1.1) rotate(5deg);
        }

        .girl-name {
            font-size: 1.3rem;
            font-weight: 600;
            color: white;
            text-align: center;
            text-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .girl-surname {
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.8);
            font-weight: 400;
        }

        /* Modal styles */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(10px);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .modal-overlay.active {
            display: flex;
            opacity: 1;
        }

        .modal-content {
            max-width: 600px;
            width: 90%;
            max-height: 80vh;
            overflow-y: auto;
            padding: 40px;
            transform: scale(0.8) translateY(20px);
            transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
            position: relative;
        }

        .modal-overlay.active .modal-content {
            transform: scale(1) translateY(0);
        }

        .close-btn {
            position: absolute;
            top: 20px;
            right: 20px;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.3);
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }

        .close-btn:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: rotate(90deg);
        }

        .modal-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .modal-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(255,255,255,0.5), rgba(255,255,255,0.2));
            margin: 0 auto 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            border: 3px solid rgba(255, 255, 255, 0.6);
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .modal-title {
            font-size: 2rem;
            color: white;
            font-weight: 700;
            margin-bottom: 5px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.2);
        }

        .modal-subtitle {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.1rem;
        }

        .compliments-list {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .compliment-item {
            background: rgba(255, 255, 255, 0.2);
            padding: 20px;
            border-radius: 16px;
            border: 1px solid rgba(255, 255, 255, 0.3);
            color: white;
            font-size: 1.1rem;
            line-height: 1.5;
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease, background 0.3s ease;
            animation: slideIn 0.5s ease-out backwards;
        }

        .compliment-item:nth-child(1) { animation-delay: 0.1s; }
        .compliment-item:nth-child(2) { animation-delay: 0.2s; }
        .compliment-item:nth-child(3) { animation-delay: 0.3s; }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .compliment-item:hover {
            transform: translateX(5px);
            background: rgba(255, 255, 255, 0.3);
        }

        .compliment-item::before {
            content: '✨';
            margin-right: 10px;
            font-size: 1.2rem;
        }

        .flower-decoration {
            position: absolute;
            font-size: 2rem;
            opacity: 0.3;
            animation: floatFlower 6s ease-in-out infinite;
        }

        @keyframes floatFlower {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        .footer {
            text-align: center;
            margin-top: 50px;
            padding: 30px;
            color: rgba(255, 255, 255, 0.8);
            font-size: 1rem;
        }

        .heart {
            color: #ff6b9d;
            animation: heartbeat 1.5s infinite;
            display: inline-block;
        }

        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }

        /* Mobile optimizations */
        @media (max-width: 768px) {
            .girls-grid {
                grid-template-columns: 1fr;
            }
            
            .modal-content {
                padding: 30px 20px;
            }
            
            .header h1 {
                font-size: 1.8rem;
            }
        }

        /* Loading animation */
        .loading {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            z-index: 9999;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: opacity 0.5s ease;
        }

        .loading.hidden {
            opacity: 0;
            pointer-events: none;
        }

        .loader {
            width: 60px;
            height: 60px;
            border: 4px solid rgba(255, 255, 255, 0.3);
            border-top-color: white;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <!-- Loading screen -->
    <div class="loading" id="loading">
        <div class="loader"></div>
    </div>

    <!-- Background particles -->
    <div class="particles" id="particles"></div>

    <div class="container">
        <!-- Header -->
        <header class="header">
            <div class="march-8">🌸</div>
            <h1>Поздравление наших любимых девочек</h1>
            <p class="subtitle">С Международным женским днём! Выбирай своё имя и получи персональное поздравление ✨</p>
            <div class="march-8">🌷</div>
        </header>

        <!-- Girls Grid -->
        <div class="girls-grid" id="girlsGrid">
            <!-- Cards will be inserted here by JavaScript -->
        </div>

        <!-- Footer -->
        <footer class="footer glass">
            <p>С любовью и уважением к прекрасному полу <span class="heart">❤️</span></p>
            <p style="margin-top: 10px; font-size: 0.9rem; opacity: 0.8;">8 марта 2026</p>
        </footer>
    </div>

    <!-- Modal -->
    <div class="modal-overlay" id="modal">
        <div class="modal-content glass">
            <button class="close-btn" onclick="closeModal()">×</button>
            <div class="flower-decoration" style="top: 20px; left: 20px;">🌺</div>
            <div class="flower-decoration" style="bottom: 20px; right: 20px; animation-delay: 1s;">🌹</div>
            
            <div class="modal-header">
                <div class="modal-avatar" id="modalAvatar">👩</div>
                <h2 class="modal-title" id="modalName">Имя</h2>
                <p class="modal-subtitle" id="modalSurname">Фамилия</p>
            </div>
            
            <div class="compliments-list" id="complimentsList">
                <!-- Compliments will be inserted here -->
            </div>
        </div>
    </div>

    <script>
        // Data for girls (sorted alphabetically by surname)
        const girls = [
            {
                surname: 'Александрова',
                name: 'Милена',
                avatar: '👑',
                compliments: [
                    'Милена, ты как весеннее солнце — освещаешь всё вокруг теплом и радостью! Твоя улыбка способна растопить любые льдины.',
                    'Ты обладаешь редким даром — делать мир вокруг себя ярче и добрее. Пусть этот день подарит тебе столько же счастья, сколько ты даришь другим!',
                    'Твоя элегантность и внутренняя сила восхищают. Ты — настоящая королева, достойная только лучшего!'
                ]
            },
            {
                surname: 'Бысыина',
                name: 'Диана',
                avatar: '🌙',
                compliments: [
                    'Диана, ты как луна — загадочная, прекрасная и освещаешь путь в темноте. Твоя мудрость и красота безграничны!',
                    'В тебе сочетаются нежность и сила, как в настоящей богине. Пусть этот день принесёт тебе заслуженное счастье и любовь!',
                    'Ты умеешь видеть красоту в мелочах и делать жизнь волшебной. Оставайся такой же чудесной!'
                ]
            },
            {
                surname: 'Евсеева',
                name: 'Амелия',
                avatar: '🎀',
                compliments: [
                    'Амелия, ты словно цветок в саду — нежная, изысканная и неповторимая! Твоя доброта делает мир лучше.',
                    'Ты обладаешь удивительным обаянием, которое притягивает сердца. Пусть весна подарит тебе исполнение всех желаний!',
                    'Твоя искренность и открытость — редкие качества. Ты заслуживаешь всего самого прекрасного в этот день и всегда!'
                ]
            },
            {
                surname: 'Ефремова',
                name: 'Валерия',
                avatar: '💎',
                compliments: [
                    'Валерия, ты как драгоценный камень — сияешь изнутри и притягиваешь взгляды своей неповторимой красотой!',
                    'Твоя сила духа и женственность вызывают восхищение. Ты умеешь быть мягкой и твёрдой одновременно.',
                    'Пусть этот день будет полон сюрпризов, а весна подарит новые мечты и их исполнение!'
                ]
            },
            {
                surname: 'Герасимова',
                name: 'Мария',
                avatar: '🌟',
                compliments: [
                    'Мария, ты как звезда — светишь ярко и ведёшь за собой. Твоё присутствие делает любой день особенным!',
                    'В тебе столько тепла и заботы, что хватает на всех вокруг. Пусть тебе возвращается сторицей всё добро, что ты даришь!',
                    'Ты вдохновляешь быть лучше. Оставайся такой же светлой и прекрасной!'
                ]
            },
            {
                surname: 'Жиркова',
                name: 'Александра',
                avatar: '⚡',
                compliments: [
                    'Александра, ты как молния — яркая, энергичная и незабываемая! Твоя энергия заряжает всех вокруг.',
                    'Ты умеешь брать от жизни всё и при этом оставаться искренней и доброй. Это настоящий талант!',
                    'Пусть этот день будет полон ярких эмоций, а весна подарит новые возможности для счастья!'
                ]
            },
            {
                surname: 'Керемясова',
                name: 'Диана',
                avatar: '🦋',
                compliments: [
                    'Диана, ты как бабочка — лёгкая, изящная и прекрасная! Твоя трансформация вдохновляет.',
                    'Ты приносишь в жизнь лёгкость и радость. Пусть этот день будет полон волшебных моментов!',
                    'Твоя душа прекрасна, как весеннее утро. Желаю тебе летать к своим мечтам без страха!'
                ]
            },
            {
                surname: 'Осипова',
                name: 'София',
                avatar: '📚',
                compliments: [
                    'София, в тебе сочетаются мудрость и молодость души. Ты как весна — обновляешь всё вокруг!',
                    'Твой ум и красота создают идеальную гармонию. Пусть этот день подарит тебе новые знания и открытия!',
                    'Ты умеешь видеть глубину в простых вещах. Оставайся такой же глубокой и интересной!'
                ]
            },
            {
                surname: 'Попова',
                name: 'Аделина',
                avatar: '🎭',
                compliments: [
                    'Аделина, ты как искусство — многогранная, глубокая и восхитительная! Твоя креативность знает границ.',
                    'Ты умеешь превращать обычные моменты в особенные. Пусть этот день будет шедевром!',
                    'Твоя индивидуальность — твой главный козырь. Никогда не переставай удивлять мир!'
                ]
            },
            {
                surname: 'Реева',
                name: 'София',
                avatar: '🌊',
                compliments: [
                    'София, ты как океан — глубокая, таинственная и бесконечно прекрасная! Твоя душа бездонна.',
                    'Ты умеешь успокаивать и вдохновлять одновременно. Пусть этот день принесёт тебе внутренний покой и радость!',
                    'Твоя интуиция и мудрость поражают. Доверяй себе — ты на правильном пути!'
                ]
            },
            {
                surname: 'Слепцова',
                name: 'Александра',
                avatar: '🎯',
                compliments: [
                    'Александра, ты как меткий выстрел — точная, уверенная и неотразимая! Ты знаешь, чего хочешь.',
                    'Твоя целеустремлённость восхищает. Пусть все твои цели в этом году сбудутся!',
                    'Ты умеешь быть сильной и нежной одновременно. Это редкий и ценный дар!'
                ]
            },
            {
                surname: 'Соловьева',
                name: 'Июлиана',
                avatar: '🎵',
                compliments: [
                    'Июлиана, твоё имя звучит как песня, и ты сама поёшь сердцами людей! Ты приносишь мелодию в жизнь.',
                    'Ты как летний день — тёплая, яркая и незабываемая. Пусть этот день будет полон музыки счастья!',
                    'Твоя уникальность делает мир разнообразнее. Никогда не меняйся!'
                ]
            },
            {
                surname: 'Шепелева',
                name: 'Арина',
                avatar: '🔥',
                compliments: [
                    'Арина, в тебе огонь и страсть, которые зажигают сердца! Ты невероятно харизматична.',
                    'Твоя энергия заразительна. Пусть этот день будет горячим и незабываемым!',
                    'Ты умеешь быть центром внимания и при этом оставаться искренней. Это настоящее мастерство!'
                ]
            }
        ];

        // Create particles
        function createParticles() {
            const container = document.getElementById('particles');
            for (let i = 0; i < 20; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 15 + 's';
                particle.style.animationDuration = (10 + Math.random() * 10) + 's';
                container.appendChild(particle);
            }
        }

        // Render girls grid
        function renderGirls() {
            const grid = document.getElementById('girlsGrid');
            
            girls.forEach((girl, index) => {
                const card = document.createElement('div');
                card.className = 'girl-card glass liquid-hover';
                card.onclick = () => openModal(index);
                
                card.innerHTML = `
                    <div class="girl-avatar">${girl.avatar}</div>
                    <div class="girl-name">${girl.name}</div>
                    <div class="girl-surname">${girl.surname}</div>
                `;
                
                grid.appendChild(card);
            });
        }

        // Open modal
        function openModal(index) {
            const girl = girls[index];
            const modal = document.getElementById('modal');
            const avatar = document.getElementById('modalAvatar');
            const name = document.getElementById('modalName');
            const surname = document.getElementById('modalSurname');
            const list = document.getElementById('complimentsList');
            
            avatar.textContent = girl.avatar;
            name.textContent = girl.name;
            surname.textContent = girl.surname;
            
            list.innerHTML = '';
            girl.compliments.forEach(compliment => {
                const item = document.createElement('div');
                item.className = 'compliment-item';
                item.textContent = compliment;
                list.appendChild(item);
            });
            
            modal.classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        // Close modal
        function closeModal() {
            const modal = document.getElementById('modal');
            modal.classList.remove('active');
            document.body.style.overflow = '';
        }

        // Close modal on outside click
        document.getElementById('modal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeModal();
            }
        });

        // Close on Escape key
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                closeModal();
            }
        });

        // Initialize
        window.addEventListener('load', () => {
            createParticles();
            renderGirls();
            
            // Hide loading screen
            setTimeout(() => {
                document.getElementById('loading').classList.add('hidden');
            }, 500);
        });

        // Add 3D tilt effect to cards
        document.addEventListener('mousemove', (e) => {
            const cards = document.querySelectorAll('.girl-card');
            const mouseX = e.clientX / window.innerWidth - 0.5;
            const mouseY = e.clientY / window.innerHeight - 0.5;
            
            cards.forEach((card, index) => {
                const rect = card.getBoundingClientRect();
                const cardX = rect.left + rect.width / 2;
                const cardY = rect.top + rect.height / 2;
                const distX = e.clientX - cardX;
                const distY = e.clientY - cardY;
                const distance = Math.sqrt(distX * distX + distY * distY);
                
                if (distance < 200) {
                    const intensity = (200 - distance) / 200;
                    const rotateX = (distY / 200) * intensity * 10;
                    const rotateY = -(distX / 200) * intensity * 10;
                    card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale(1.02)`;
                } else {
                    card.style.transform = '';
                }
            });
        });
    </script>
</body>
</html>
