<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fongasik | Creative Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #0f0f1b;
            --bg-secondary: #161625;
            --bg-tertiary: #1e1e30;
            --text-primary: #e8e8ff;
            --text-secondary: #b0b0d0;
            --accent-primary: #8b5cf6;
            --accent-secondary: #a78bfa;
            --accent-tertiary: #c4b5fd;
            --border-color: #2d2d45;
            --card-bg: #1a1a28;
            --python-color: #3776ab;
            --html-color: #e34c26;
            --vscode-color: #007acc;
            --capcut-color: #fe2d55;
            --minecraft-color: #70c145;
        }

        body {
            font-family: 'Space Grotesk', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, var(--bg-primary) 0%, var(--bg-tertiary) 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            color: var(--text-primary);
            line-height: 1.6;
            position: relative;
            overflow-x: hidden;
        }

        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 15% 25%, rgba(139, 92, 246, 0.08) 0%, transparent 25%),
                radial-gradient(circle at 85% 75%, rgba(167, 139, 250, 0.08) 0%, transparent 25%),
                radial-gradient(circle at 50% 10%, rgba(196, 181, 253, 0.05) 0%, transparent 30%);
            pointer-events: none;
        }

        .container {
            max-width: 800px;
            width: 100%;
            background: var(--card-bg);
            border-radius: 28px;
            box-shadow: 0 30px 60px -15px rgba(0, 0, 0, 0.6);
            overflow: hidden;
            border: 1px solid var(--border-color);
            backdrop-filter: blur(12px);
            position: relative;
            animation: fadeInUp 0.8s ease-out;
        }

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

        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-primary), var(--accent-secondary), var(--accent-tertiary));
        }

        .header {
            background: linear-gradient(135deg, #251b4d 0%, #1c153a 100%);
            color: white;
            text-align: center;
            padding: 55px 20px 45px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(139, 92, 246, 0.15) 0%, transparent 70%);
            transform: rotate(30deg);
        }

        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 3px solid rgba(255, 255, 255, 0.15);
            background: linear-gradient(135deg, #2a205a, #1f1845);
            margin: 0 auto 28px;
            background-image: url('https://placehold.co/150x150/8b5cf6/ffffff?text=F0');
            background-size: cover;
            background-position: center;
            box-shadow: 0 12px 35px rgba(0, 0, 0, 0.45);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
        }

        .avatar:hover {
            transform: scale(1.06) rotate(3deg);
            box-shadow: 0 18px 45px rgba(139, 92, 246, 0.35);
        }

        .avatar::after {
            content: '🖥️';
            position: absolute;
            bottom: -12px;
            right: -12px;
            width: 35px;
            height: 35px;
            background: var(--accent-primary);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 16px;
            box-shadow: 0 5px 15px rgba(139, 92, 246, 0.4);
            border: 2px solid var(--card-bg);
        }

        .name {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #ffffff, var(--accent-tertiary), #ff9ff3);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 3px 12px rgba(255, 255, 255, 0.15);
            letter-spacing: -0.5px;
        }

        .title {
            font-size: 1.35rem;
            opacity: 0.9;
            font-weight: 400;
            color: #d8d8ff;
            margin-bottom: 22px;
            font-family: 'JetBrains Mono', monospace;
            letter-spacing: 0.5px;
        }

        .stats {
            display: flex;
            justify-content: center;
            gap: 28px;
            margin-top: 18px;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 1.45rem;
            font-weight: 700;
            color: var(--accent-secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }

        .stat-label {
            font-size: 0.88rem;
            opacity: 0.75;
            margin-top: 2px;
        }

        .content {
            padding: 50px;
        }

        .section {
            margin-bottom: 40px;
            position: relative;
            padding-left: 8px;
            opacity: 0;
            transform: translateY(20px);
            animation: slideIn 0.6s ease-out forwards;
        }

        .section:nth-child(1) { animation-delay: 0.2s; }
        .section:nth-child(2) { animation-delay: 0.4s; }
        .section:nth-child(3) { animation-delay: 0.6s; }
        .section:nth-child(4) { animation-delay: 0.8s; }

        @keyframes slideIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .section:not(:last-child)::after {
            content: '';
            position: absolute;
            bottom: -18px;
            left: 0;
            width: 45px;
            height: 2px;
            background: linear-gradient(90deg, var(--accent-primary), transparent);
        }

        .section-title {
            font-size: 1.65rem;
            color: var(--accent-secondary);
            margin-bottom: 20px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .section-title i {
            font-size: 1.3rem;
            background: rgba(139, 92, 246, 0.15);
            width: 38px;
            height: 38px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: var(--accent-primary);
        }

        .bio-text {
            line-height: 1.75;
            color: var(--text-secondary);
            font-size: 1.08rem;
            font-weight: 300;
            margin-bottom: 18px;
        }

        .interests {
            display: flex;
            flex-wrap: wrap;
            gap: 14px;
            margin-top: 12px;
        }

        .interest-item {
            display: flex;
            align-items: center;
            gap: 8px;
            background: rgba(139, 92, 246, 0.1);
            color: var(--accent-secondary);
            padding: 8px 16px;
            border-radius: 16px;
            font-size: 0.95rem;
            font-weight: 500;
            border: 1px solid rgba(139, 92, 246, 0.2);
            transition: all 0.3s ease;
        }

        .interest-item:hover {
            background: rgba(139, 92, 246, 0.2);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(139, 92, 246, 0.2);
        }

        .interest-item.python { color: var(--python-color); border-color: rgba(55, 118, 171, 0.3); background: rgba(55, 118, 171, 0.1); }
        .interest-item.html { color: var(--html-color); border-color: rgba(227, 76, 38, 0.3); background: rgba(227, 76, 38, 0.1); }
        .interest-item.vscode { color: var(--vscode-color); border-color: rgba(0, 122, 204, 0.3); background: rgba(0, 122, 204, 0.1); }
        .interest-item.capcut { color: var(--capcut-color); border-color: rgba(254, 45, 85, 0.3); background: rgba(254, 45, 85, 0.1); }
        .interest-item.minecraft { color: var(--minecraft-color); border-color: rgba(112, 193, 69, 0.3); background: rgba(112, 193, 69, 0.1); }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 14px;
            margin-top: 18px;
        }

        .skill {
            background: rgba(139, 92, 246, 0.1);
            color: var(--accent-secondary);
            padding: 11px 20px;
            border-radius: 50px;
            font-size: 0.92rem;
            font-weight: 500;
            border: 1px solid rgba(139, 92, 246, 0.25);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill::before {
            content: '';
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: var(--accent-primary);
        }

        .skill:hover {
            background: rgba(139, 92, 246, 0.25);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(139, 92, 246, 0.25);
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 20px;
            padding: 14px 0;
            transition: transform 0.25s ease;
            cursor: pointer;
        }

        .contact-item:hover {
            transform: translateX(6px);
        }

        .contact-icon {
            width: 48px;
            height: 48px;
            background: linear-gradient(135deg, var(--accent-primary), var(--accent-secondary));
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 20px;
            flex-shrink: 0;
            box-shadow: 0 5px 18px rgba(139, 92, 246, 0.35);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .contact-item:hover .contact-icon {
            transform: rotate(12deg) scale(1.15);
            box-shadow: 0 8px 25px rgba(139, 92, 246, 0.45);
        }

        .contact-text {
            font-size: 1.12rem;
            color: var(--text-primary);
            font-weight: 400;
            word-break: break-word;
            position: relative;
        }

        .contact-text::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 0;
            height: 1.5px;
            background: var(--accent-primary);
            transition: width 0.3s ease;
        }

        .contact-item:hover .contact-text::after {
            width: 100%;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-top: 30px;
            padding-top: 30px;
            border-top: 1px solid var(--border-color);
        }

        .social-link {
            width: 52px;
            height: 52px;
            border-radius: 50%;
            background: var(--bg-secondary);
            display: flex;
            justify-content: center;
            align-items: center;
            color: var(--accent-secondary);
            font-size: 23px;
            text-decoration: none;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            border: 2px solid var(--border-color);
            position: relative;
            overflow: hidden;
        }

        .social-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, var(--accent-primary), var(--accent-secondary));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .social-link:hover::before {
            opacity: 1;
        }

        .social-link:hover {
            transform: translateY(-5px) scale(1.12);
            box-shadow: 0 10px 30px rgba(139, 92, 246, 0.5);
        }

        .social-link:hover i {
            color: white;
            transform: scale(1.15);
        }

        .social-link i {
            position: relative;
            z-index: 1;
            transition: all 0.3s ease;
        }

        .quote {
            font-style: italic;
            color: var(--text-secondary);
            margin-top: 15px;
            padding-left: 25px;
            border-left: 3px solid var(--accent-primary);
            font-size: 1.15rem;
            position: relative;
            font-family: 'JetBrains Mono', monospace;
        }

        .quote::before {
            content: '"';
            position: absolute;
            left: -20px;
            top: -8px;
            font-size: 2.2rem;
            color: var(--accent-primary);
            opacity: 0.35;
            font-family: serif;
        }

        .footer-note {
            text-align: center;
            margin-top: 35px;
            color: var(--text-secondary);
            font-size: 0.95rem;
            opacity: 0.8;
            font-family: 'JetBrains Mono', monospace;
            letter-spacing: 0.5px;
        }

        .tools-showcase {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 15px;
        }

        .tool {
            background: var(--bg-secondary);
            padding: 6px 14px;
            border-radius: 12px;
            font-size: 0.88rem;
            display: flex;
            align-items: center;
            gap: 6px;
            border: 1px solid var(--border-color);
        }

        .tool i {
            font-size: 0.9rem;
        }

        @media (max-width: 600px) {
            .name {
                font-size: 2.3rem;
            }
            
            .content {
                padding: 35px 25px;
            }
            
            .section-title {
                font-size: 1.45rem;
            }
            
            .stats {
                gap: 20px;
                flex-wrap: wrap;
            }
            
            .avatar {
                width: 130px;
                height: 130px;
            }
            
            .interests, .skills {
                justify-content: center;
            }
        }

        @media (max-width: 480px) {
            .name {
                font-size: 1.9rem;
            }
            
            .title {
                font-size: 1.15rem;
            }
            
            .social-link {
                width: 48px;
                height: 48px;
                font-size: 21px;
            }
            
            .stat-number {
                font-size: 1.25rem;
            }
            
            .content {
                padding: 30px 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="avatar"></div>
            <h1 class="name">Fongasik</h1>
            <p class="title">HTML/Python Developer • Content Creator • Gamer</p>
            <div class="stats">
                <div class="stat-item">
                    <div class="stat-number"><i class="fas fa-code"></i> 2+</div>
                    <div class="stat-label">лет кодинга</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number"><i class="fas fa-video"></i>18</div>
                    <div class="stat-label">видео</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number"><i class="fas fa-cube"></i> 7500+</div>
                    <div class="stat-label">часов в MC</div>
                </div>
            </div>
        </div>
        
        <div class="content">
            <div class="section">
                <h2 class="section-title"><i class="fas fa-user-astronaut"></i> Обо мне</h2>
                <p class="bio-text">
                    Привет! Я Fongasik — обычный игрок «Майнкрафта», который начинает учиться кодить.
                     Я контентмейкер, который иногда, но выпускает видео. 
                     Сейчас я создал этот сайт со своим другом aLix59ru!
                     На данный момент у меня два ника: Fongasik,Deprawed.
                </p>
                <p class="bio-text">
                    Люблю играть в игры и искать идеи в них.
                </p>
                <div class="interests">
                    <span class="interest-item python"><i class="fab fa-python"></i> Python</span>
                    <span class="interest-item html"><i class="fab fa-html5"></i> HTML/CSS</span>
                    <span class="interest-item vscode"><i class="fab fa-microsoft"></i> VS Code</span>
                    <span class="interest-item capcut"><i class="fas fa-cut"></i> CapCut</span>
                    <span class="interest-item minecraft"><i class="fas fa-cube"></i> Minecraft</span>
					<span class="interest-item HA"><i class="fas fa-home"></i> Home Assistant</span>
                </div>
                <p class="quote">"Minecraft это начало, а кодинг конец"</p>
            </div>
            
            <div class="section">
                <h2 class="section-title"><i class="fas fa-laptop-code"></i> Технологии & Инструменты</h2>
                <div class="skills">
                    <span class="skill">Python</span>
                    <span class="skill">HTML5</span>
                    <span class="skill">Git & GitHub</span>
                    <span class="skill">VS Code</span>
                    <span class="skill">CapCut</span>
                    <span class="skill">Minecraft Redstone</span>
                    <span class="skill">Linux</span>
					<span class="skill">Home Assistant</span>
                </div>
                <div class="tools-showcase">
                    <span class="tool"><i class="fab fa-python"></i> Python 3.11+</span>
                    <span class="tool"><i class="fab fa-html5"></i> HTML5/CSS3</span>
                    <span class="tool"><i class="fab fa-microsoft"></i> VS Code</span>
                    <span class="tool"><i class="fas fa-cut"></i> CapCut</span>
					<span class="tool"><i class="fas fa-home"></i> Home Assistant</span>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title"><i class="fas fa-paper-plane"></i> Контакты</h2>
                <div class="contact-info">
                    <a href="https://t.me/Deprawed" class="contact-item" target="_blank" rel="noopener noreferrer">
                        <div class="contact-icon">
                            <i class="fab fa-telegram"></i>
                        </div>
                        <div class="contact-text">@Deprawed</div>
                    </a>
                    <a href="https://github.com/deprawed" class="contact-item" target="_blank" rel="noopener noreferrer">
                        <div class="contact-icon">
                            <i class="fab fa-github"></i>
                        </div>
                        <div class="contact-text">Deprawed</div>
                    </a>
                    <a href="fongasik07@gmail.com" class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">fongasik07@gmail.com</div>
                    </a>
					
                    <a href="https://Vyitaknasaite.ru" class="contact-item" target="_blank" rel="noopener noreferrer">
                        <div class="contact-icon">
                            <i class="fas fa-globe"></i>
                        </div>
                        <div class="contact-text">Сайт</div>
					</a>
					<a href="https://www.youtube.com/@Fongasik" class="contact-item" target="_blank" rel="noopener noreferrer">
                        <div class="contact-icon">
                            <i class="fab fa-youtube"></i>
                        </div>
                        <div class="contact-text">@Fongasik</div>
					</a>

                </div>
            </div>
            
            <div class="social-links">
                <a href="https://github.com/deprawed" class="social-link" title="GitHub" target="_blank" rel="noopener noreferrer">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://t.me/Derlaught" class="social-link" title="Telegram" target="_blank" rel="noopener noreferrer">
                    <i class="fab fa-telegram-plane"></i>
                </a>
                <a href="https://youtube.com/@fongasik" class="social-link" title="YouTube">
                    <i class="fab fa-youtube"></i>
                </a>
                <a href="https://discord.com/f0ngasik" class="social-link" title="Discord">
                    <i class="fab fa-discord"></i>
                </a>
            </div>
            
            <div class="footer-note">
                <p>Создано aLix59ru, Fongasik и Qwen-3 MAX Ai | 2025-2026 | Python • HTML • Minecraft</p>
				<p>Скоро хэллоувин кста!🎃🎃🎃</p>

<a href="http://madebydimas.top/" target="_blank"><img src="http://madebydimas.top/button.gif" alt="madebydimas" border="0" width="88" height="31"></a>
<a href="http://minako9667.w10.site/" title="Личный сайт Неру Асано"><img border="0" src="http://minako9667.w10.site/res/buttons/my_own.gif" alt="Личный сайт Неру Асано"></a>
<a href="http://veselcraft.cc/" title="" target="_black"> <img src="http://veselcraft.cc/images/vc.gif" alt="veselcraft"> </a>
<a href="https://eversiege.network"><img src="https://eversiege.network/media/image/everseige.png" alt="eversiege.network" width="88" height="31"></a>
<a href="http://myslivets.com" title="Daniel Myslivets" target="_blank" rel="noopener noreferrer">
<a href="http://myslivets.com" title="Daniel Myslivets" target="_blank" rel="noopener noreferrer">
<img src="http://myslivets.com/img/button.png" alt="Daniel Myslivets" border="0" width="88" height="31"></a>
<a href="http://faero.top/" target="_blank">
<img src="http://faero.top/ad/button.gif" alt="faero.top" border="0" width="88" height="31"></a>
<a href="http://fm.faero.top/" target="_blank">
<img src="http://fm.faero.top/button.gif" alt="FaeroFM" border="0" width="88" height="31"></a>
<a href="http://inori.faero.top/" target="_blank">
<img src="http://inori.faero.top/button.gif" alt="Inori" border="0" width="88" height="31"></a>
<a href="http://web1.0hosting.net" title="Web1.0 Hosting" target="_blank" rel="noopener noreferrer">
<img src="http://web1.0hosting.net/b.gif" alt="Web1.0 Hosting"></a>
<a href="https://senko.digital/" target="_blank" rel="noopener noreferrer">
<img src="http://senko.digital/images/88x31/hosted_on.png" alt="senko.digital"></a>
<a href="http://l-lacker.ru/blackhole/ryzhik/"><img src="https://l-lacker.ru/blackhole/ryzhik/img/banner88x31.gif" width="88" height="31" alt="Рыжик.su" border="0"></a>


                    <a href="https://github.com/aLix159ru" class="contact-item" target="_blank" rel="noopener noreferrer">
                        <div class="contact-icon">
                            <i class="fab fa-github"></i>
                        </div>
                        <div class="contact-text">Создатель сайта</div>
                    </a>
            </div>
        </div>
    </div>
</body>
</html>
