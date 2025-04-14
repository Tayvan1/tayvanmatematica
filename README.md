<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MathMaster - Domine a Matemática</title>
    <style>
        :root {
            --primary-black: #111111;
            --secondary-black: #1a1a1a;
            --gold-primary: #FFD700;
            --gold-secondary: #D4AF37;
            --gold-light: #FFECB3;
            --text-light: #f5f5f5;
            --text-gray: #cccccc;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--primary-black);
            color: var(--text-light);
            margin: 0;
            padding: 0;
        }
        
        /* Header Styles */
        header {
            background-color: var(--primary-black);
            padding: 1rem 2rem;
            border-bottom: 2px solid var(--gold-primary);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            color: var(--gold-primary);
            font-size: 2rem;
            font-weight: bold;
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo span {
            margin-left: 0.5rem;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 0.5rem 1rem;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            color: var(--gold-primary);
            background-color: rgba(255, 215, 0, 0.1);
        }
        
        .cta-button {
            background-color: var(--gold-primary);
            color: var(--primary-black);
            padding: 0.7rem 1.5rem;
            border-radius: 4px;
            font-weight: bold;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .cta-button:hover {
            background-color: var(--gold-light);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(255, 215, 0, 0.3);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('math-background.jpg');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: var(--gold-primary);
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin-bottom: 2rem;
            color: var(--text-gray);
        }
        
        /* Features Section */
        .features {
            padding: 4rem 2rem;
            background-color: var(--secondary-black);
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--gold-primary);
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background-color: var(--gold-primary);
            margin: 1rem auto;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .feature-card {
            background-color: var(--primary-black);
            border: 1px solid rgba(255, 215, 0, 0.2);
            border-radius: 8px;
            padding: 2rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(255, 215, 0, 0.1);
            border-color: var(--gold-primary);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--gold-primary);
            margin-bottom: 1rem;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--gold-light);
        }
        
        /* Dashboard Section */
        .dashboard {
            padding: 4rem 2rem;
        }
        
        .study-tracks {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .track {
            background-color: var(--secondary-black);
            border-radius: 8px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            border-left: 4px solid var(--gold-primary);
        }
        
        .track-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .track-title {
            font-size: 1.5rem;
            color: var(--gold-primary);
        }
        
        .progress-bar {
            height: 10px;
            background-color: #333;
            border-radius: 5px;
            margin-top: 0.5rem;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background-color: var(--gold-primary);
            width: 0%;
            transition: width 1s ease-in-out;
        }
        
        .topics {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 1rem;
        }
        
        .topic {
            background-color: rgba(255, 215, 0, 0.1);
            padding: 1rem;
            border-radius: 4px;
            transition: background-color 0.3s;
        }
        
        .topic:hover {
            background-color: rgba(255, 215, 0, 0.2);
        }
        
        .topic h4 {
            margin-top: 0;
            color: var(--text-light);
        }
        
        .topic-status {
            display: flex;
            align-items: center;
            font-size: 0.9rem;
            color: var(--text-gray);
        }
        
        .status-dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            margin-right: 0.5rem;
        }
        
        .completed {
            background-color: var(--gold-primary);
        }
        
        .in-progress {
            background-color: #FFA500;
        }
        
        .not-started {
            background-color: #666;
        }
        
        /* Community Section */
        .community {
            padding: 4rem 2rem;
            background-color: var(--secondary-black);
        }
        
        .forum-container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .forum-categories {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .category {
            background-color: var(--primary-black);
            border-radius: 8px;
            padding: 1.5rem;
            transition: transform 0.3s;
        }
        
        .category:hover {
            transform: translateY(-5px);
        }
        
        .category h3 {
            color: var(--gold-light);
            border-bottom: 1px solid rgba(255, 215, 0, 0.3);
            padding-bottom: 0.5rem;
            margin-bottom: 1rem;
        }
        
        .topics-list {
            list-style: none;
            padding: 0;
        }
        
        .topics-list li {
            margin-bottom: 0.8rem;
        }
        
        .topics-list a {
            color: var(--text-light);
            text-decoration: none;
            transition: color 0.3s;
            display: flex;
            align-items: center;
        }
        
        .topics-list a:before {
            content: '➔';
            color: var(--gold-primary);
            margin-right: 0.5rem;
        }
        
        .topics-list a:hover {
            color: var(--gold-primary);
        }
        
        /* Doubt Section */
        .doubt-section {
            padding: 4rem 2rem;
        }
        
        .doubt-container {
            max-width: 800px;
            margin: 0 auto;
            background-color: var(--secondary-black);
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .doubt-tabs {
            display: flex;
            margin-bottom: 1.5rem;
            border-bottom: 1px solid rgba(255, 215, 0, 0.3);
        }
        
        .doubt-tab {
            padding: 0.8rem 1.5rem;
            cursor: pointer;
            color: var(--text-gray);
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .doubt-tab.active {
            color: var(--gold-primary);
            border-bottom: 2px solid var(--gold-primary);
            margin-bottom: -1px;
        }
        
        .doubt-tab:hover:not(.active) {
            color: var(--text-light);
        }
        
        .doubt-content {
            display: none;
        }
        
        .doubt-content.active {
            display: block;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--text-light);
        }
        
        .form-group input,
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 0.8rem;
            background-color: var(--primary-black);
            border: 1px solid #333;
            border-radius: 4px;
            color: var(--text-light);
        }
        
        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        .submit-btn {
            background-color: var(--gold-primary);
            color: var(--primary-black);
            border: none;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            font-weight: bold;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .submit-btn:hover {
            background-color: var(--gold-light);
        }
        
        /* Footer */
        footer {
            background-color: var(--primary-black);
            padding: 3rem 2rem;
            border-top: 1px solid rgba(255, 215, 0, 0.2);
            text-align: center;
        }
        
        .footer-logo {
            color: var(--gold-primary);
            font-size: 1.8rem;
            font-weight: bold;
            margin-bottom: 1.5rem;
            display: inline-block;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 1.5rem;
        }
        
        .footer-links a {
            color: var(--text-gray);
            margin: 0 1rem;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--gold-primary);
        }
        
        .social-icons {
            margin-bottom: 1.5rem;
        }
        
        .social-icons a {
            color: var(--text-light);
            margin: 0 0.5rem;
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        
        .social-icons a:hover {
            color: var(--gold-primary);
        }
        
        .copyright {
            color: var(--text-gray);
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            header {
                flex-direction: column;
                padding: 1rem;
            }
            
            nav ul {
                margin-top: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0.5rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <a href="index.html" class="logo">
            <svg width="30" height="30" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M12 2L3 7L12 12L21 7L12 2Z" fill="#FFD700"/>
                <path d="M3 11L12 16L21 11" stroke="#FFD700" stroke-width="2"/>
                <path d="M3 15L12 20L21 15" stroke="#FFD700" stroke-width="2"/>
            </svg>
            <span>MathMaster</span>
        </a>
        <nav>
            <ul>
                <li><a href="#trilhas">Trilhas de Estudo</a></li>
                <li><a href="#comunidade">Comunidade</a></li>
                <li><a href="#duvidas">Tira-Dúvidas</a></li>
                <li><a href="#" class="cta-button">Login</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Domine a Matemática</h1>
        <p>Aprenda de forma estruturada, tire dúvidas com especialistas e faça parte de uma comunidade de estudantes apaixonados por matemática.</p>
        <a href="#" class="cta-button">Comece Agora</a>
    </section>

    <!-- Features Section -->
    <section class="features">
        <h2 class="section-title">Como Funciona</h2>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">📊</div>
                <h3>Trilhas Personalizadas</h3>
                <p>Caminhos de aprendizado adaptados ao seu nível e objetivos, com progresso visualizado em tempo real.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">👥</div>
                <h3>Comunidade Ativa</h3>
                <p>Conecte-se com outros estudantes, participe de discussões e resolva problemas em grupo.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">💡</div>
                <h3>Tira-Dúvidas</h3>
                <p>Esclareça suas questões com especialistas e acesse um banco de respostas organizado.</p>
            </div>
        </div>
    </section>

    <!-- Dashboard/Study Tracks Section -->
    <section class="dashboard" id="trilhas">
        <h2 class="section-title">Trilhas de Estudo</h2>
        <div class="study-tracks">
            <div class="track">
                <div class="track-header">
                    <h3 class="track-title">Matemática Básica</h3>
                    <span>25% completo</span>
                </div>
                <div class="progress-bar">
                    <div class="progress" style="width: 25%"></div>
                </div>
                <div class="topics">
                    <div class="topic">
                        <h4>Operações Fundamentais</h4>
                        <div class="topic-status">
                            <span class="status-dot completed"></span>
                            <span>Completo</span>
                        </div>
                    </div>
                    <div class="topic">
                        <h4>Frações e Decimais</h4>
                        <div class="topic-status">
                            <span class="status-dot in-progress"></span>
                            <span>Em Progresso</span>
                        </div>
                    </div>
                    <div class="topic">
                        <h4>Porcentagem</h4>
                        <div class="topic-status">
                            <span class="status-dot not-started"></span>
                            <span>Não Iniciado</span>
                        </div>
                    </div>
                    <div class="topic">
                        <h4>Expressões Algébricas</h4>
                        <div class="topic-status">
                            <span class="status-dot not-started"></span>
                            <span>Não Iniciado</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="track">
                <div class="track-header">
                    <h3 class="track-title">Álgebra</h3>
                    <span>10% completo</span>
                </div>
                <div class="progress-bar">
                    <div class="progress" style="width: 10%"></div>
                </div>
                <div class="topics">
                    <div class="topic">
                        <h4>Equações Lineares</h4>
                        <div class="topic-status">
                            <span class="status-dot completed"></span>
                            <span>Completo</span>
                        </div>
                    </div>
                    <div class="topic">
                        <h4>Sistemas de Equações</h4>
                        <div class="topic-status">
                            <span class="status-dot not-started"></span>
                            <span>Não Iniciado</span>
                        </div>
                    </div>
                    <div class="topic">
                        <h4>Polinômios</h4>
                        <div class="topic-status">
                            <span class="status-dot not-started"></span>
                            <span>Não Iniciado</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Community Section -->
    <section class="community" id="comunidade">
        <h2 class="section-title">Comunidade</h2>
        <div class="forum-container">
            <div class="forum-categories">
                <div class="category">
                    <h3>Dúvidas Gerais</h3>
                    <ul class="topics-list">
                        <li><a href="#">Como resolver equações quadráticas?</a></li>
                        <li><a href="#">Melhor método para fatoração</a></li>
                        <li><a href="#">Dúvida sobre progressões aritméticas</a></li>
                        <li><a href="#">Ver todos os tópicos</a></li>
                    </ul>
                </div>
                <div class="category">
                    <h3>Desafios Matemáticos</h3>
                    <ul class="topics-list">
                        <li><a href="#">Desafio da semana: Problema de lógica</a></li>
                        <li><a href="#">Soluções do desafio anterior</a></li>
                        <li><a href="#">Competições matemáticas</a></li>
                        <li><a href="#">Ver todos os tópicos</a></li>
                    </ul>
                </div>
                <div class="category">
                    <h3>Material de Estudo</h3>
                    <ul class="topics-list">
                        <li><a href="#">Livros recomendados para cálculo</a></li>
                        <li><a href="#">Resumos de geometria analítica</a></li>
                        <li><a href="#">Listas de exercícios resolvidos</a></li>
                        <li><a href="#">Ver todos os tópicos</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Doubt Section -->
    <section class="doubt-section" id="duvidas">
        <h2 class="section-title">Tira-Dúvidas</h2>
        <div class="doubt-container">
            <div class="doubt-tabs">
                <div class="doubt-tab active" data-tab="ask">Enviar Dúvida</div>
                <div class="doubt-tab" data-tab="answers">Minhas Dúvidas</div>
                <div class="doubt-tab" data-tab="faq">Dúvidas Frequentes</div>
            </div>
            
            <div class="doubt-content active" id="ask-content">
                <form>
                    <div class="form-group">
                        <label for="subject">Assunto</label>
                        <input type="text" id="subject" placeholder="Ex: Como resolver equações do segundo grau">
                    </div>
                    <div class="form-group">
                        <label for="category">Categoria</label>
                        <select id="category">
                            <option>Álgebra</option>
                            <option>Geometria</option>
                            <option>Trigonometria</option>
                            <option>Cálculo</option>
                            <option>Estatística</option>
                            <option>Outro</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="question">Sua Dúvida</label>
                        <textarea id="question" placeholder="Descreva sua dúvida com detalhes. Você pode incluir fórmulas usando a notação matemática (ex: x^2 + 3x - 4 = 0)"></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Enviar Dúvida</button>
                </form>
            </div>
            
            <div class="doubt-content" id="answers-content">
                <p>Aqui aparecerão suas dúvidas enviadas e as respostas dos especialistas.</p>
            </div>
            
            <div class="doubt-content" id="faq-content">
                <p>Busque nas dúvidas frequentes da comunidade.</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <a href="index.html" class="footer-logo">MathMaster</a>
        <div class="footer-links">
            <a href="#">Sobre</a>
            <a href="#">Termos de Uso</a>
            <a href="#">Política de Privacidade</a>
            <a href="#">Contato</a>
        </div>
        <div class="social-icons">
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
        </div>
        <p class="copyright">© 2023 MathMaster. Todos os direitos reservados.</p>
    </footer>

    <script>
        // Tab functionality for doubt section
        document.addEventListener('DOMContentLoaded', function() {
            const tabs = document.querySelectorAll('.doubt-tab');
            const contents = document.querySelectorAll('.doubt-content');
            
            tabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    // Remove active class from all tabs and contents
                    tabs.forEach(t => t.classList.remove('active'));
                    contents.forEach(c => c.classList.remove('active'));
                    
                    // Add active class to clicked tab and corresponding content
                    tab.classList.add('active');
                    const tabId = tab.getAttribute('data-tab');
                    document.getElementById(`${tabId}-content`).classList.add('active');
                });
            });
            
            // Animate progress bars on scroll
            const progressBars = document.querySelectorAll('.progress');
            
            function animateProgressBars() {
                progressBars.forEach(bar => {
                    const targetWidth = bar.style.width;
                    bar.style.width = '0%';
                    
                    setTimeout(() => {
                        bar.style.width = targetWidth;
                    }, 300);
                });
            }
            
            // Simple intersection observer to trigger animations
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        animateProgressBars();
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });
            
            document.querySelectorAll('.study-tracks').forEach(section => {
                observer.observe(section);
            });
        });
    </script>
    
    <!-- Font Awesome for icons (optional) -->
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</body>
</html>
