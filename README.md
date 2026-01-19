<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🔐 Blue Team & Programación | GitHub Profile</title>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Animate.css -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@300;400;600;700&family=Orbitron:wght@400;700;900&family=Share+Tech+Mono&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #00ff00;
            --primary-dark: #00cc00;
            --secondary: #0088ff;
            --secondary-dark: #0066cc;
            --dark-bg: #0d1117;
            --darker-bg: #090c10;
            --card-bg: #161b22;
            --text: #c9d1d9;
            --text-muted: #8b949e;
            --terminal: #00ff41;
            --neon-blue: #00e5ff;
            --neon-purple: #b967ff;
            --cyber-yellow: #ffd300;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Roboto Mono', monospace;
            background-color: var(--dark-bg);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 15% 50%, rgba(0, 255, 0, 0.05) 0%, transparent 20%),
                radial-gradient(circle at 85% 30%, rgba(0, 136, 255, 0.05) 0%, transparent 20%),
                radial-gradient(circle at 50% 80%, rgba(179, 103, 255, 0.05) 0%, transparent 20%);
        }
        
        .cyber-grid {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(0, 255, 0, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 255, 0, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: -1;
            pointer-events: none;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header y Banner */
        .header {
            position: relative;
            margin-bottom: 40px;
            overflow: hidden;
            border-radius: 15px;
            border: 1px solid rgba(0, 255, 0, 0.2);
            box-shadow: 0 0 30px rgba(0, 255, 0, 0.1);
        }
        
        .animated-banner {
            position: relative;
            height: 300px;
            background: linear-gradient(135deg, 
                rgba(13, 17, 23, 0.9) 0%, 
                rgba(9, 12, 16, 0.95) 100%),
                url('https://images.unsplash.com/photo-1550751827-4bd374c3f58b?auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        
        .scan-line {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, 
                transparent, 
                var(--primary), 
                transparent);
            animation: scan 3s linear infinite;
            z-index: 2;
        }
        
        @keyframes scan {
            0% { top: 0; }
            100% { top: 100%; }
        }
        
        .banner-content {
            text-align: center;
            z-index: 1;
            padding: 20px;
        }
        
        .hacker-text {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.8rem;
            font-weight: 900;
            background: linear-gradient(90deg, var(--primary), var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 15px rgba(0, 255, 0, 0.5);
            margin-bottom: 10px;
            animation: glitch 5s infinite;
        }
        
        @keyframes glitch {
            0%, 100% { transform: translate(0); }
            1% { transform: translate(-2px, 2px); }
            2% { transform: translate(-2px, -2px); }
            3% { transform: translate(2px, 2px); }
            4% { transform: translate(2px, -2px); }
            5% { transform: translate(0); }
        }
        
        .subtitle {
            font-family: 'Share Tech Mono', monospace;
            font-size: 1.3rem;
            color: var(--text);
            margin-bottom: 20px;
        }
        
        .typed-text {
            color: var(--terminal);
            font-weight: bold;
            border-right: 3px solid var(--terminal);
            padding-right: 5px;
            animation: blink 0.7s infinite;
        }
        
        @keyframes blink {
            0%, 100% { border-color: var(--terminal); }
            50% { border-color: transparent; }
        }
        
        /* Tarjetas */
        .card {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 25px;
            margin-bottom: 25px;
            border: 1px solid rgba(0, 255, 0, 0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--primary), transparent);
            transition: left 0.5s ease;
        }
        
        .card:hover::before {
            left: 100%;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 255, 0, 0.1);
            border-color: rgba(0, 255, 0, 0.3);
        }
        
        .card-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        /* Botones animados */
        .btn-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .cyber-btn {
            position: relative;
            background: transparent;
            color: var(--text);
            border: 2px solid var(--primary);
            padding: 12px 20px;
            font-family: 'Share Tech Mono', monospace;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            overflow: hidden;
            transition: all 0.3s ease;
            border-radius: 5px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            text-decoration: none;
        }
        
        .cyber-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 0, 0.2), transparent);
            transition: left 0.5s ease;
        }
        
        .cyber-btn:hover::before {
            left: 100%;
        }
        
        .cyber-btn:hover {
            background-color: rgba(0, 255, 0, 0.1);
            color: var(--primary);
            box-shadow: 0 0 15px rgba(0, 255, 0, 0.3);
            transform: scale(1.05);
        }
        
        .btn-blue {
            border-color: var(--secondary);
            color: var(--secondary);
        }
        
        .btn-blue:hover {
            background-color: rgba(0, 136, 255, 0.1);
            color: var(--secondary);
            box-shadow: 0 0 15px rgba(0, 136, 255, 0.3);
        }
        
        .btn-purple {
            border-color: var(--neon-purple);
            color: var(--neon-purple);
        }
        
        .btn-purple:hover {
            background-color: rgba(185, 103, 255, 0.1);
            color: var(--neon-purple);
            box-shadow: 0 0 15px rgba(185, 103, 255, 0.3);
        }
        
        /* Badges animados */
        .badge-container {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 15px 0;
        }
        
        .cyber-badge {
            display: inline-flex;
            align-items: center;
            background-color: rgba(22, 27, 34, 0.8);
            border: 1px solid rgba(0, 255, 0, 0.3);
            border-radius: 20px;
            padding: 6px 15px;
            font-size: 0.8rem;
            color: var(--text);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .cyber-badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 255, 0, 0.2);
            border-color: var(--primary);
            color: var(--primary);
        }
        
        .badge-icon {
            margin-right: 8px;
            font-size: 0.9rem;
        }
        
        /* Tarjetas de habilidades */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .skill-category {
            background-color: rgba(22, 27, 34, 0.6);
            border-radius: 10px;
            padding: 20px;
            border-left: 4px solid var(--primary);
        }
        
        .skill-category.blue {
            border-left-color: var(--secondary);
        }
        
        .skill-category.purple {
            border-left-color: var(--neon-purple);
        }
        
        .skill-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            padding-bottom: 8px;
            border-bottom: 1px dashed rgba(0, 255, 0, 0.2);
        }
        
        .skill-name {
            color: var(--text);
        }
        
        .skill-bar {
            height: 6px;
            background-color: rgba(0, 255, 0, 0.1);
            border-radius: 3px;
            margin-top: 5px;
            overflow: hidden;
        }
        
        .skill-level {
            height: 100%;
            background: linear-gradient(90deg, var(--primary), var(--neon-blue));
            border-radius: 3px;
            position: relative;
            animation: fillBar 2s ease-out;
        }
        
        @keyframes fillBar {
            0% { width: 0%; }
            100% { width: attr(data-level); }
        }
        
        /* Proyectos */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }
        
        .project-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            border: 1px solid rgba(0, 255, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 255, 0, 0.15);
            border-color: rgba(0, 255, 0, 0.4);
        }
        
        .project-header {
            padding: 20px;
            background-color: rgba(0, 20, 0, 0.3);
            border-bottom: 1px solid rgba(0, 255, 0, 0.2);
        }
        
        .project-title {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.3rem;
            color: var(--primary);
            margin-bottom: 8px;
        }
        
        .project-desc {
            color: var(--text-muted);
            font-size: 0.9rem;
        }
        
        .project-body {
            padding: 20px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin: 15px 0;
        }
        
        .tech-tag {
            background-color: rgba(0, 50, 0, 0.3);
            color: var(--primary);
            padding: 4px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
            border: 1px solid rgba(0, 255, 0, 0.2);
        }
        
        /* Estadísticas */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            border: 1px solid rgba(0, 255, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
            box-shadow: 0 10px 20px rgba(0, 255, 0, 0.1);
        }
        
        .stat-number {
            font-family: 'Orbitron', sans-serif;
            font-size: 2.5rem;
            color: var(--primary);
            margin: 10px 0;
            text-shadow: 0 0 10px rgba(0, 255, 0, 0.5);
        }
        
        /* Footer */
        .footer {
            text-align: center;
            padding: 30px;
            margin-top: 50px;
            border-top: 1px solid rgba(0, 255, 0, 0.2);
            color: var(--text-muted);
            font-size: 0.9rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        
        .social-icon {
            color: var(--text);
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-icon:hover {
            color: var(--primary);
            transform: scale(1.2);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .btn-grid {
                grid-template-columns: 1fr;
            }
            
            .hacker-text {
                font-size: 2rem;
            }
            
            .skills-grid, .project-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Fondo con grid -->
    <div class="cyber-grid"></div>
    
    <div class="container">
        <!-- Header con banner animado -->
        <header class="header">
            <div class="animated-banner">
                <div class="scan-line"></div>
                <div class="banner-content">
                    <h1 class="hacker-text animate__animated animate__fadeInDown">CYBER_DEFENDER</h1>
                    <p class="subtitle animate__animated animate__fadeInUp">Especialista en <span class="typed-text">Blue Team & Desarrollo Seguro</span></p>
                    
                    <div class="btn-grid animate__animated animate__fadeInUp" style="animation-delay: 0.5s;">
                        <a href="#about" class="cyber-btn">
                            <i class="fas fa-user-secret"></i> Sobre Mí
                        </a>
                        <a href="#skills" class="cyber-btn btn-blue">
                            <i class="fas fa-shield-alt"></i> Habilidades
                        </a>
                        <a href="#projects" class="cyber-btn btn-purple">
                            <i class="fas fa-code"></i> Proyectos
                        </a>
                        <a href="#contact" class="cyber-btn">
                            <i class="fas fa-terminal"></i> Contacto
                        </a>
                    </div>
                </div>
            </div>
        </header>
        
        <!-- Sección Sobre Mí -->
        <section class="card animate__animated animate__fadeIn" id="about">
            <h2 class="card-title">
                <i class="fas fa-terminal"></i> [root@cyberdefender:~]# whoami
            </h2>
            <p>Profesional de ciberseguridad con enfoque en defensa (Blue Team) y más de 5 años de experiencia en protección de infraestructuras críticas. Combino conocimientos avanzados de seguridad con habilidades de desarrollo para implementar soluciones defensivas proactivas.</p>
            
            <div class="badge-container">
                <span class="cyber-badge">
                    <i class="fas fa-shield-alt badge-icon"></i> Blue Team Specialist
                </span>
                <span class="cyber-badge">
                    <i class="fas fa-bug badge-icon"></i> Security Researcher
                </span>
                <span class="cyber-badge">
                    <i class="fas fa-code badge-icon"></i> Secure Developer
                </span>
                <span class="cyber-badge">
                    <i class="fas fa-network-wired badge-icon"></i> Network Defender
                </span>
                <span class="cyber-badge">
                    <i class="fas fa-brain badge-icon"></i> Threat Hunter
                </span>
            </div>
        </section>
        
        <!-- Sección Habilidades -->
        <section class="card animate__animated animate__fadeIn" id="skills" style="animation-delay: 0.2s;">
            <h2 class="card-title">
                <i class="fas fa-cogs"></i> Habilidades Técnicas
            </h2>
            
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fas fa-shield-alt" style="color: var(--primary);"></i> Blue Team</h3>
                    <div class="skill-item">
                        <span class="skill-name">SIEM & Log Management</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 95%;"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">Threat Hunting & DFIR</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 90%;"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">Network Security Monitoring</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 88%;"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">Vulnerability Management</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 85%;"></div>
                    </div>
                </div>
                
                <div class="skill-category blue">
                    <h3><i class="fas fa-code" style="color: var(--secondary);"></i> Desarrollo</h3>
                    <div class="skill-item">
                        <span class="skill-name">Python Security Automation</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 92%; background: linear-gradient(90deg, var(--secondary), var(--neon-blue));"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">Bash/PowerShell Scripting</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 90%; background: linear-gradient(90deg, var(--secondary), var(--neon-blue));"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">DevSecOps & CI/CD Security</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 85%; background: linear-gradient(90deg, var(--secondary), var(--neon-blue));"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">Web App Security</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 88%; background: linear-gradient(90deg, var(--secondary), var(--neon-blue));"></div>
                    </div>
                </div>
                
                <div class="skill-category purple">
                    <h3><i class="fas fa-tools" style="color: var(--neon-purple);"></i> Herramientas</h3>
                    <div class="skill-item">
                        <span class="skill-name">Splunk/ELK Stack</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 94%; background: linear-gradient(90deg, var(--neon-purple), #ff6b9d);"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">Wireshark & Network Analysis</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 91%; background: linear-gradient(90deg, var(--neon-purple), #ff6b9d);"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">Docker & Kubernetes Security</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 82%; background: linear-gradient(90deg, var(--neon-purple), #ff6b9d);"></div>
                    </div>
                    
                    <div class="skill-item">
                        <span class="skill-name">MITRE ATT&CK Framework</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 93%; background: linear-gradient(90deg, var(--neon-purple), #ff6b9d);"></div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Sección Proyectos -->
        <section class="card animate__animated animate__fadeIn" id="projects" style="animation-delay: 0.4s;">
            <h2 class="card-title">
                <i class="fas fa-project-diagram"></i> Proyectos Destacados
            </h2>
            
            <div class="project-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">SIEM Dashboard Avanzado</h3>
                        <p class="project-desc">Dashboard interactivo para monitorización de seguridad en tiempo real</p>
                    </div>
                    <div class="project-body">
                        <p>Plataforma personalizada de análisis de logs con detección de anomalías y correlación de eventos de seguridad.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">Elasticsearch</span>
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">Docker</span>
                        </div>
                        <div class="btn-grid" style="grid-template-columns: 1fr;">
                            <a href="#" class="cyber-btn">
                                <i class="fab fa-github"></i> Ver Código
                            </a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">Auto-IR Framework</h3>
                        <p class="project-desc">Framework de automatización para respuesta a incidentes</p>
                    </div>
                    <div class="project-body">
                        <p>Sistema automatizado de playbooks para respuesta a incidentes de seguridad con integración de múltiples herramientas.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Python</span>
                            <span class="tech-tag">PowerShell</span>
                            <span class="tech-tag">REST API</span>
                            <span class="tech-tag">MITRE ATT&CK</span>
                        </div>
                        <div class="btn-grid" style="grid-template-columns: 1fr;">
                            <a href="#" class="cyber-btn">
                                <i class="fab fa-github"></i> Ver Código
                            </a>
                        </div>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-header">
                        <h3 class="project-title">Threat Intelligence Platform</h3>
                        <p class="project-desc">Agregador de fuentes de inteligencia de amenazas</p>
                    </div>
                    <div class="project-body">
                        <p>Plataforma centralizada para recopilación, normalización y análisis de fuentes de threat intelligence.</p>
                        <div class="project-tech">
                            <span class="tech-tag">Go</span>
                            <span class="tech-tag">MongoDB</span>
                            <span class="tech-tag">Redis</span>
                            <span class="tech-tag">Docker</span>
                        </div>
                        <div class="btn-grid" style="grid-template-columns: 1fr;">
                            <a href="#" class="cyber-btn">
                                <i class="fab fa-github"></i> Ver Código
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Sección Estadísticas -->
        <section class="card animate__animated animate__fadeIn" style="animation-delay: 0.6s;">
            <h2 class="card-title">
                <i class="fas fa-chart-line"></i> Estadísticas & Logros
            </h2>
            
            <div class="stats-container">
                <div class="stat-card">
                    <i class="fas fa-code-branch" style="font-size: 2rem; color: var(--primary);"></i>
                    <div class="stat-number">50+</div>
                    <p>Proyectos de Seguridad</p>
                </div>
                
                <div class="stat-card">
                    <i class="fas fa-bug" style="font-size: 2rem; color: var(--secondary);"></i>
                    <div class="stat-number">200+</div>
                    <p>Vulnerabilidades Identificadas</p>
                </div>
                
                <div class="stat-card">
                    <i class="fas fa-shield-alt" style="font-size: 2rem; color: var(--neon-purple);"></i>
                    <div class="stat-number">15+</div>
                    <p>Incidentes Contenidos</p>
                </div>
                
                <div class="stat-card">
                    <i class="fas fa-certificate" style="font-size: 2rem; color: var(--cyber-yellow);"></i>
                    <div class="stat-number">8</div>
                    <p>Certificaciones Obtenidas</p>
                </div>
            </div>
        </section>
        
        <!-- Sección Contacto -->
        <section class="card animate__animated animate__fadeIn" id="contact" style="animation-delay: 0.8s;">
            <h2 class="card-title">
                <i class="fas fa-network-wired"></i> Conecta Conmigo
            </h2>
            
            <p>¿Interesado en colaborar en proyectos de ciberseguridad, discutir técnicas de blue team o intercambiar conocimientos sobre desarrollo seguro?</p>
            
            <div class="btn-grid">
                <a href="mailto:security@cyberdefender.dev" class="cyber-btn">
                    <i class="fas fa-envelope"></i> Email
                </a>
                <a href="https://linkedin.com/in/cyberdefender" class="cyber-btn btn-blue">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
                <a href="https://github.com/cyberdefender" class="cyber-btn">
                    <i class="fab fa-github"></i> GitHub
                </a>
                <a href="https://twitter.com/cyber_defender" class="cyber-btn btn-purple">
                    <i class="fab fa-twitter"></i> Twitter
                </a>
                <a href="https://tryhackme.com/r/p/cyberdefender" class="cyber-btn">
                    <i class="fas fa-flag"></i> TryHackMe
                </a>
                <a href="https://app.hackthebox.com/profile/cyberdefender" class="cyber-btn">
                    <i class="fas fa-cube"></i> HackTheBox
                </a>
            </div>
            
            <div class="social-links">
                <a href="#" class="social-icon"><i class="fab fa-discord"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-medium"></i></a>
                <a href="#" class="social-icon"><i class="fab fa-youtube"></i></a>
                <a href="#" class="social-icon"><i class="fas fa-blog"></i></a>
            </div>
        </section>
        
        <!-- Footer -->
        <footer class="footer">
            <p>« La seguridad es un proceso, no un producto » — Bruce Schneier</p>
            <p style="margin-top: 10px; font-size: 0.8rem;">
                <i class="fas fa-lock"></i> Este perfil fue protegido con 
                <span style="color: var(--primary);">Blue Team</span> 
                y desarrollado con 
                <span style="color: var(--secondary);">código seguro</span>
            </p>
            <p style="margin-top: 5px; font-size: 0.7rem; color: var(--text-muted);">
                Última actualización: <span id="current-date"></span>
            </p>
        </footer>
    </div>

    <script>
        // Actualizar fecha automáticamente
        document.getElementById('current-date').textContent = new Date().toLocaleDateString('es-ES', {
            year: 'numeric',
            month: 'long',
            day: 'numeric'
        });
        
        // Efecto de escritura para el texto typed
        const typedTextSpan = document.querySelector('.typed-text');
        const texts = ['Blue Team', 'DFIR', 'Threat Hunting', 'Security Automation', 'DevSecOps'];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        
        function typeEffect() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typedTextSpan.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typedTextSpan.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }
            
            if (!isDeleting && charIndex === currentText.length) {
                isDeleting = true;
                setTimeout(typeEffect, 1500);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
                setTimeout(typeEffect, 500);
            } else {
                setTimeout(typeEffect, isDeleting ? 50 : 100);
            }
        }
        
        // Iniciar efecto de escritura
        document.addEventListener('DOMContentLoaded', () => {
            setTimeout(typeEffect, 1000);
            
            // Animación al hacer scroll
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('animate__animated', 'animate__fadeInUp');
                    }
                });
            }, observerOptions);
            
            // Observar todas las tarjetas
            document.querySelectorAll('.card').forEach(card => {
                observer.observe(card);
            });
        });
        
        // Efecto de sonido para botones (simulado con consola)
        document.querySelectorAll('.cyber-btn').forEach(button => {
            button.addEventListener('click', function(e) {
                console.log(`[CYBER] Navegando a: ${this.textContent}`);
                
                // Efecto visual adicional
                this.style.transform = 'scale(0.95)';
                setTimeout(() => {
                    this.style.transform = '';
                }, 150);
            });
        });
        
        // Efecto de parpadeo aleatorio en título
        const hackerText = document.querySelector('.hacker-text');
        setInterval(() => {
            if (Math.random() > 0.7) {
                hackerText.style.textShadow = '0 0 20px rgba(255, 0, 0, 0.8)';
                setTimeout(() => {
                    hackerText.style.textShadow = '0 0 15px rgba(0, 255, 0, 0.5)';
                }, 100);
            }
        }, 3000);
    </script>
</body>
</html>
