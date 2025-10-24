        .intro {
            text-align: center;
            padding: 3rem 1rem;
            margin-bottom: 2rem;
            position: relative;
            overflow: hidden;
        }

        .intro::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(56, 189, 248, 0.1) 0%, transparent 70%);
            animation: float 6s ease-in-out infinite;
            z-index: -1;
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid #38bdf8;
            margin: 0 auto 1.5rem;
            overflow: hidden;
            position: relative;
            box-shadow: 0 0 30px rgba(56, 189, 248, 0.3);
            animation: pulse 2s infinite;
        }

        .profile-img::after {
            content: '';
            position: absolute;
            top: -10px;
            left: -10px;
            right: -10px;
            bottom: -10px;
            border: 2px solid #38bdf8;
            border-radius: 50%;
            animation: rotate 3s linear infinite;
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #38bdf8, #818cf8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .intro p {
            font-size: 1.3rem;
            max-width: 600px;
            margin: 0 auto 2rem;
            color: #94a3b8;
        }

        .typing-text {
            font-size: 1.2rem;
            color: #38bdf8;
            border-right: 2px solid #38bdf8;
            padding-right: 5px;
            animation: blink 1s infinite;
        }

        /* Skills Section */
        .skills-section {
            margin: 4rem 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 25%;
            width: 50%;
            height: 3px;
            background: linear-gradient(90deg, transparent, #38bdf8, transparent);
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .skill-card {
            background: rgba(30, 41, 59, 0.7);
            border-radius: 15px;
            padding: 1.5rem 1rem;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(56, 189, 248, 0.1);
            position: relative;
            overflow: hidden;
        }

        .skill-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(56, 189, 248, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .skill-card:hover::before {
            left: 100%;
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(56, 189, 248, 0.2);
            border-color: #38bdf8;
        }

        .skill-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
            transition: all 0.3s ease;
        }

        .skill-card:hover .skill-icon {
            transform: scale(1.2);
            color: #38bdf8;
        }

        .skill-name {
            font-weight: 600;
            color: #e2e8f0;
        }

        /* Specific icon animations */
        .react-icon { animation: float 3s ease-in-out infinite; }
        .nextjs-icon { animation: pulse 2s infinite; }
        .js-icon { animation: bounce 2s infinite; }
        .ts-icon { animation: spin 3s linear infinite; }
        .tailwind-icon { animation: wave 2s ease-in-out infinite; }
        .html-icon { animation: shake 2s infinite; }
        .css-icon { animation: colorChange 4s infinite; }
        .git-icon { animation: rotate 3s linear infinite; }

        /* Contact Section */
        .contact-section {
            margin: 4rem 0;
            text-align: center;
        }

        .contact-badges {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
            margin-top: 2rem;
        }

        .contact-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.8rem 1.5rem;
            background: rgba(30, 41, 59, 0.7);
            border-radius: 25px;
            text-decoration: none;
            color: #e2e8f0;
            transition: all 0.3s ease;
            border: 1px solid rgba(56, 189, 248, 0.2);
            position: relative;
            overflow: hidden;
        }

        .contact-badge::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(56, 189, 248, 0.2), transparent);
            transition: left 0.5s ease;
        }

        .contact-badge:hover::before {
            left: 100%;
        }

        .contact-badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 20px rgba(56, 189, 248, 0.3);
            border-color: #38bdf8;
        }

        /* Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.05); opacity: 0.8; }
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(5deg); }
            75% { transform: rotate(-5deg); }
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-2px); }
            75% { transform: translateX(2px); }
        }

        @keyframes colorChange {
            0% { color: #38bdf8; }
            25% { color: #818cf8; }
            50% { color: #f472b6; }
            75% { color: #34d399; }
            100% { color: #38bdf8; }
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes blink {
            0%, 100% { border-color: #38bdf8; }
            50% { border-color: transparent; }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 { font-size: 2.2rem; }
            .intro p { font-size: 1.1rem; }
            .skills-grid { grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); }
            .contact-badges { flex-direction: column; align-items: center; }
            .contact-badge { width: 250px; justify-content: center; }
        }

        @media (max-width: 480px) {
            h1 { font-size: 1.8rem; }
            .section-title { font-size: 2rem; }
            .skills-grid { grid-template-columns: repeat(3, 1fr); gap: 1rem; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 👨‍💻 Intro Section -->
        <section class="intro">
            <div class="profile-img">
                <!-- يمكنك إضافة صورتك هنا -->
            </div>
            <h1>Hi, I'm <strong>Michael Soliman</strong> 👋</h1>
            <p>Front-End Developer crafting clean, fast, and user-friendly web experiences.</p>
            <div class="typing-text">Passionate about creating amazing digital experiences</div>
        </section>

        <!-- 🛠️ Skills Section -->
        <section class="skills-section">
            <h2 class="section-title">My Favorite Tools & Technologies</h2>
            
            <div class="skills-grid">
                <!-- Row 1 -->
                <div class="skill-card">
                    <i class="skill-icon react-icon fab fa-react"></i>
                    <span class="skill-name">React</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon nextjs-icon">▲</i>
                    <span class="skill-name">Next.js</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon redux-icon">⚛️</i>
                    <span class="skill-name">Redux</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon tailwind-icon">🌊</i>
                    <span class="skill-name">Tailwind</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon ts-icon fab fa-js-square"></i>
                    <span class="skill-name">TypeScript</span>
                </div>

                <!-- Row 2 -->
                <div class="skill-card">
                    <i class="skill-icon js-icon fab fa-js"></i>
                    <span class="skill-name">JavaScript</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon html-icon fab fa-html5"></i>
                    <span class="skill-name">HTML5</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon css-icon fab fa-css3-alt"></i>
                    <span class="skill-name">CSS3</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon bootstrap-icon fab fa-bootstrap"></i>
                    <span class="skill-name">Bootstrap</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon material-icon">📱</i>
                    <span class="skill-name">Material UI</span>
                </div>

                <!-- Row 3 -->
                <div class="skill-card">
                    <i class="skill-icon vite-icon">⚡</i>
                    <span class="skill-name">Vite</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon webpack-icon">📦</i>
                    <span class="skill-name">Webpack</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon git-icon fab fa-git-alt"></i>
                    <span class="skill-name">Git</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon github-icon fab fa-github"></i>
                    <span class="skill-name">GitHub</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon figma-icon fab fa-figma"></i>
                    <span class="skill-name">Figma</span>
                </div>

                <!-- Row 4 -->
                <div class="skill-card">
                    <i class="skill-icon vscode-icon">💻</i>
                    <span class="skill-name">VS Code</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon vercel-icon">▲</i>
                    <span class="skill-name">Vercel</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon netlify-icon">🌐</i>
                    <span class="skill-name">Netlify</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon npm-icon fab fa-npm"></i>
                    <span class="skill-name">NPM</span>
                </div>
                <div class="skill-card">
                    <i class="skill-icon yarn-icon">🐱</i>
                    <span class="skill-name">Yarn</span>
                </div>
            </div>
        </section>

        <!-- 🌐 Contact Section -->
        <section class="contact-section">
            <h2 class="section-title">Connect With Me</h2>
            <div class="contact-badges">
                <a href="https://www.facebook.com/share/1N4HEWCGNt/" target="_blank" class="contact-badge">
                    <i class="fab fa-facebook"></i>
                    Facebook
                </a>
                <a href="https://www.linkedin.com/in/michael-soliman-82aa1524a" target="_blank" class="contact-badge">
                    <i class="fab fa-linkedin"></i>
                    LinkedIn
                </a>
                <a href="https://portfolio-dusky-two-0ts2c83ebf.vercel.app/" target="_blank" class="contact-badge">
                    <i class="fas fa-briefcase"></i>
                    Portfolio
                </a>
                <a href="https://github.com/yourusername" target="_blank" class="contact-badge">
                    <i class="fab fa-github"></i>
                    GitHub
                </a>
            </div>
        </section>
    </div>

    <script>
        // تأثير الكتابة للنص
        const typingText = document.querySelector('.typing-text');
        const texts = [
            "Passionate about creating amazing digital experiences",
            "Frontend Developer specializing in React & Next.js",
            "Love building fast and responsive web applications",
            "Always learning new technologies and best practices"
        ];
        
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        
        function type() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingText.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingText.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }
            
            if (!isDeleting && charIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }
            
            setTimeout(type, isDeleting ? 50 : 100);
        }
        
        // بدء تأثير الكتابة بعد تحميل الصفحة
        setTimeout(type, 1000);
        
        // تأثيرات إضافية عند التمرير
        const skillCards = document.querySelectorAll('.skill-card');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationDelay = `${Math.random() * 0.5}s`;
                    entry.target.classList.add('animate-in');
                }
            });
        }, { threshold: 0.1 });
        
        skillCards.forEach(card => observer.observe(card));
    </script>
</body>
</html>
