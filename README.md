<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CV - Francis Jefferson Chingal Hernández</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --accent-color: #e74c3c;
            --light-color: #ecf0f1;
            --dark-color: #34495e;
            --text-color: #333;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: var(--text-color);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: white;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
        }
        
        header {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 30px 0;
            background-color: var(--primary-color);
            color: white;
            border-radius: 5px 5px 0 0;
            position: relative;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            margin-bottom: 20px;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: var(--light-color);
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            transition: var(--transition);
        }
        
        .contact-item:hover {
            transform: translateY(-3px);
            color: var(--secondary-color);
        }
        
        .contact-item i {
            font-size: 1.2rem;
        }
        
        main {
            padding: 30px;
        }
        
        .section {
            margin-bottom: 40px;
        }
        
        .section-title {
            font-size: 1.5rem;
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 10px;
            margin-bottom: 20px;
            color: var(--primary-color);
            position: relative;
            cursor: pointer;
        }
        
        .section-title::after {
            content: '\f077';
            font-family: 'Font Awesome 5 Free';
            font-weight: 900;
            position: absolute;
            right: 10px;
            transition: var(--transition);
        }
        
        .section-title.collapsed::after {
            transform: rotate(180deg);
        }
        
        .section-content {
            max-height: 1000px;
            overflow: hidden;
            transition: max-height 0.5s ease;
        }
        
        .collapsed + .section-content {
            max-height: 0;
        }
        
        .profile-text {
            text-align: justify;
            margin-bottom: 20px;
        }
        
        .experience-item, .education-item, .formacion-item {
            margin-bottom: 25px;
            padding-left: 20px;
            border-left: 3px solid var(--secondary-color);
            position: relative;
        }
        
        .experience-item::before, .education-item::before, .formacion-item::before {
            content: '';
            position: absolute;
            width: 15px;
            height: 15px;
            background-color: var(--secondary-color);
            border-radius: 50%;
            left: -9px;
            top: 5px;
        }
        
        .experience-date, .education-date, .formacion-date {
            font-weight: bold;
            color: var(--accent-color);
            margin-bottom: 5px;
        }
        
        .experience-title, .education-title, .formacion-title {
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .experience-description, .education-description, .formacion-description {
            color: #555;
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .skill-item {
            background-color: var(--light-color);
            padding: 10px 15px;
            border-radius: 20px;
            cursor: pointer;
            transition: var(--transition);
            position: relative;
        }
        
        .skill-item:hover {
            background-color: var(--secondary-color);
            color: white;
            transform: translateY(-3px);
        }
        
        .skill-level {
            position: absolute;
            bottom: -20px;
            left: 0;
            width: 100%;
            background-color: white;
            padding: 5px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            opacity: 0;
            transition: var(--transition);
            transform: translateY(-10px);
            z-index: 1;
            text-align: center;
        }
        
        .skill-item:hover .skill-level {
            opacity: 1;
            transform: translateY(0);
        }
        
        .language-container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .language-item {
            flex: 1;
            min-width: 200px;
            padding: 15px;
            background-color: var(--light-color);
            border-radius: 5px;
            transition: var(--transition);
        }
        
        .language-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .language-name {
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .progress-bar {
            width: 100%;
            height: 10px;
            background-color: #ddd;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            background-color: var(--secondary-color);
        }
        
        .links-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .link-item {
            padding: 10px 15px;
            background-color: var(--light-color);
            border-radius: 5px;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: var(--transition);
            text-decoration: none;
            color: var(--text-color);
        }
        
        .link-item:hover {
            background-color: var(--secondary-color);
            color: white;
            transform: translateY(-3px);
        }
        
        .references-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        
        .reference-item {
            padding: 20px;
            background-color: var(--light-color);
            border-radius: 5px;
            transition: var(--transition);
        }
        
        .reference-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .reference-name {
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .reference-position {
            font-style: italic;
            color: var(--secondary-color);
            margin-bottom: 10px;
        }
        
        .reference-contact {
            display: flex;
            align-items: center;
            gap: 8px;
            margin-top: 5px;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            background-color: var(--primary-color);
            color: white;
            border-radius: 0 0 5px 5px;
        }
        
        .download-btn {
            display: inline-block;
            padding: 10px 20px;
            background-color: var(--secondary-color);
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: var(--transition);
            margin-top: 10px;
        }
        
        .download-btn:hover {
            background-color: var(--accent-color);
            transform: translateY(-3px);
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            
            header {
                padding: 20px 0;
            }
            
            .profile-img {
                width: 120px;
                height: 120px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            main {
                padding: 20px;
            }
            
            .references-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <img src="francis-perfil.jpg" alt="Francis Jefferson Chingal Hernández" class="profile-img">
            <h1>Francis Jefferson Chingal Hernández</h1>
            <p class="subtitle">Ingeniero en Logística y Transporte</p>
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span>+593 989 77 2019</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>jeffersonchingal@gmail.com</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>Tulcán, Ecuador</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-calendar"></i>
                    <span>Octubre 04, 1997</span>
                </div>
            </div>
        </header>
        
        <main>
            <div class="section">
                <h2 class="section-title">Perfil Profesional</h2>
                <div class="section-content">
                    <p class="profile-text">
                        Nacido en Tulcán, Ecuador, en 1997. Obtuve mi título de Ingeniero en Logística y Transporte de la
                        Universidad Politécnica Estatal del Carchi, en el 2025. Apasionado por la eficiencia y la innovación en
                        la gestión logística, me especializo en desarrollar estrategias que optimicen procesos y generen valor.
                        Además busco contribuir al crecimiento y competitividad de las organizaciones a través de soluciones
                        innovadoras y eficientes.
                    </p>
                    <p class="profile-text">
                        A nivel de relaciones interpersonales, en términos generales puedo decir que cuento con amplios
                        conocimientos en técnicas aduaneras, administración logística, ingeniería de la calidad y tráfico y transporte, 
                        lo que me permite optimizar procesos, mejorar la eficiencia operativa y aportar soluciones estratégicas 
                        a la industria. Mi experiencia en planificación, liderazgo de equipos y gestión de proyectos me
                        ha permitido desarrollar iniciativas de alto impacto en el sector logístico.
                    </p>
                    <p class="profile-text">
                        Actualmente lidero FC Concerts, empresa especializada en producción de eventos y manejo de artistas,
                        con trayectoria en la organización de conciertos de alto impacto. He gestionado giras y presentaciones
                        de artistas nacionales e internacionales, destacando mi rol en booking, promoción y dirección de
                        espectáculos en vivo.
                    </p>
                    <p class="profile-text">
                        Me caracterizo por ser una persona creativa, proactiva y con grandes habilidades de comunicación.
                        Mi capacidad de liderazgo y pasión por la actualización continua en logística, producción de eventos y
                        gestión de negocios me impulsan a seguir innovando en cada uno de mis proyectos.
                    </p>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Experiencia Profesional</h2>
                <div class="section-content">
                    <div class="experience-item">
                        <div class="experience-date">2025 - Actual</div>
                        <div class="experience-title">FC Concerts - Ecuador</div>
                        <div class="experience-description">
                            Gestión y producción de eventos, booking de artistas y planificación logística para espectáculos en
                            todo el país.
                        </div>
                    </div>
                    <div class="experience-item">
                        <div class="experience-date">2023 - 2024</div>
                        <div class="experience-title">Universidad Politécnica Estatal del Carchi - Tulcán</div>
                        <div class="experience-description">
                            Analista de Procesos / Pasante
                        </div>
                    </div>
                    <div class="experience-item">
                        <div class="experience-date">2023 - 2024</div>
                        <div class="experience-title">Universidad Politécnica Estatal del Carchi - Tulcán</div>
                        <div class="experience-description">
                            Proyecto de Factibilidad / Montaje de una Planta de Cárnicos en la Finca San Francisco
                            <a href="https://acortar.link/uXg0Vq" target="_blank" class="link-item" style="display: inline-block; margin-top: 10px;">
                                <i class="fas fa-link"></i>
                                <span>Ver proyecto</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Formación Académica</h2>
                <div class="section-content">
                    <div class="education-item">
                        <div class="education-date">2025</div>
                        <div class="education-title">Ingeniería en Logística y Transporte</div>
                        <div class="education-description">
                            Facultad Comercio Internacional, Administración y Economía Empresarial<br>
                            Universidad Politécnica Estatal del Carchi
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Formación Complementaria</h2>
                <div class="section-content">
                    <div class="formacion-item">
                        <div class="formacion-date">Julio 2024</div>
                        <div class="formacion-title">Curso de Importación y Exportación</div>
                        <div class="formacion-description">
                            Cámara de Comercio Ecuador/Shanghai<br>
                            40 horas. 17-30 Julio, 2024
                        </div>
                    </div>
                    <div class="formacion-item">
                        <div class="formacion-date">Noviembre 2024</div>
                        <div class="formacion-title">Curso de Llenado de Declaraciones Aduaneras en el Sistema Aduanero</div>
                        <div class="formacion-description">
                            My Intelecto. Guayaquil, Ecuador<br>
                            10 horas. 12-16 Noviembre, 2024
                            <a href="https://acortar.link/E0oaQv" target="_blank" class="link-item" style="display: inline-block; margin-top: 10px;">
                                <i class="fas fa-link"></i>
                                <span>Ver certificado</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Áreas de Actuación</h2>
                <div class="section-content">
                    <div class="experience-item">
                        <div class="experience-date">2025 - Actual</div>
                        <div class="experience-title">Gestión de almacenes e inventarios</div>
                    </div>
                    <div class="experience-item">
                        <div class="experience-date">2023 - 2024</div>
                        <div class="experience-title">Simulación y optimización de procesos</div>
                    </div>
                    <div class="experience-item">
                        <div class="experience-date">2023 - 2024</div>
                        <div class="experience-title">Creación de contenido y marketing digital</div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Habilidades y Software</h2>
                <div class="section-content">
                    <div class="skills-container">
                        <div class="skill-item">
                            Argis
                            <div class="skill-level">Nivel: Intermedio</div>
                        </div>
                        <div class="skill-item">
                            Python
                            <div class="skill-level">Nivel: Básico</div>
                        </div>
                        <div class="skill-item">
                            MySQL
                            <div class="skill-level">Nivel: Intermedio</div>
                        </div>
                        <div class="skill-item">
                            FlexSim
                            <div class="skill-level">Nivel: Intermedio</div>
                        </div>
                        <div class="skill-item">
                            Excel
                            <div class="skill-level">Nivel: Intermedio</div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Idiomas</h2>
                <div class="section-content">
                    <div class="language-container">
                        <div class="language-item">
                            <div class="language-name">Español</div>
                            <div class="progress-bar">
                                <div class="progress" style="width: 100%"></div>
                            </div>
                            <p>Nativo</p>
                        </div>
                        <div class="language-item">
                            <div class="language-name">Inglés</div>
                            <div class="progress-bar">
                                <div class="progress" style="width: 85%"></div>
                            </div>
                            <p>Avanzado (C1)</p>
                            <a href="https://acortar.link/zaKlF2" target="_blank" class="link-item" style="display: inline-block; margin-top: 10px;">
                                <i class="fas fa-link"></i>
                                <span>Ver certificado</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Distinciones y Premios</h2>
                <div class="section-content">
                    <div class="experience-item">
                        <div class="experience-date">2024 - 2025</div>
                        <div class="experience-title">Reconocimiento por liderazgo / Presidente de la carrera de Logística y Transporte</div>
                        <div class="experience-description">
                            Universidad Politécnica Estatal del Carchi
                            <a href="https://acortar.link/CTZn67" target="_blank" class="link-item" style="display: inline-block; margin-top: 10px;">
                                <i class="fas fa-link"></i>
                                <span>Ver reconocimiento</span>
                            </a>
                        </div>
                    </div>
                    <div class="experience-item">
                        <div class="experience-date">2024</div>
                        <div class="experience-title">Tercer lugar en el Evento Académico Internacional / Cadena logística del aguacate en mercados internacionales</div>
                        <div class="experience-description">
                            <a href="https://upec.edu.ec/index.php/boletin-057-2024/" target="_blank" class="link-item" style="display: inline-block; margin-top: 10px;">
                                <i class="fas fa-link"></i>
                                <span>Ver reconocimiento</span>
                            </a>
                        </div>
                    </div>
                    <div class="experience-item">
                        <div class="experience-date">2024 - 2025</div>
                        <div class="experience-title">Reconocimiento por liderazgo en eventos estudiantiles y culturales</div>
                        <div class="experience-description">
                            Universidad Politécnica Estatal del Carchi
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Publicaciones Científicas</h2>
                <div class="section-content">
                    <div class="experience-item">
                        <div class="experience-date">2024</div>
                        <div class="experience-title">Análisis de la cadena logística en la comercialización del aguacate desde Ecuador hacia mercados internacionales</div>
                        <div class="experience-description">
                            7mo Congreso de Ingenierías, Universidad Politécnica Estatal del Carchi - Tulcán.<br>
                            Ponencia en evento académico.
                            <a href="https://acortar.link/xiqxh2" target="_blank" class="link-item" style="display: inline-block; margin-top: 10px;">
                                <i class="fas fa-link"></i>
                                <span>Ver publicación</span>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Desarrollo de contenido virtual y creación de prototipos</h2>
                <div class="section-content">
                    <div class="experience-item">
                        <div class="experience-date">2021 - Actual</div>
                        <div class="experience-title">FC Concerts - Ecuador</div>
                        <div class="experience-description">
                            Canal de YouTube sobre eventos y conciertos
                            <a href="https://acortar.link/IiENDY" target="_blank" class="link-item" style="display: inline-block; margin-top: 10px;">
                                <i class="fas fa-link"></i>
                                <span>Ver canal</span>
                            </a>
                        </div>
                    </div>
                    <div class="experience-item">
                        <div class="experience-date">2023</div>
                        <div class="experience-title">Universidad Politécnica Estatal del Carchi - Tulcán</div>
                        <div class="experience-description">
                            Simulación de procesos con FlexSim para proyectos de mejora logística
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h2 class="section-title">Referencias</h2>
                <div class="section-content">
                    <div class="references-container">
                        <div class="reference-item">
                            <div class="reference-name">Francisco Cruz García, MSc.</div>
                            <div class="reference-position">Gerente Petro Amazonas</div>
                            <div class="reference-institution">Escuela Politécnica Nacional - Quito</div>
                            <div class="reference-contact">
                                <i class="fas fa-phone"></i>
                                <span>0987243160</span>
                            </div>
                            <div class="reference-contact">
                                <i class="fas fa-envelope"></i>
                                <span>franciscocruz16@gmail.com</span>
                            </div>
                        </div>
                        <div class="reference-item">
                            <div class="reference-name">Gabriela Alexandra Calvachi Heredia, MSc.</div>
                            <div class="reference-position">Comunicador Social / GAD Antonio Ante</div>
                            <div class="reference-institution">Universidad Central del Ecuador - Quito</div>
                            <div class="reference-contact">
                                <i class="fas fa-phone"></i>
                                <span>0994265185</span>
                            </div>
                            <div class="reference-contact">
                                <i class="fas fa-envelope"></i>
                                <span>gabyalex22@hotmail.com</span>
                            </div>
                        </div>
                        <div class="reference-item">
                            <div class="reference-name">Ana Karen Palacios Puentestar, MSc.</div>
                            <div class="reference-position">Directora Administrativa / GAD Mira</div>
                            <div class="reference-institution">Universidad Católica del Ecuador – Ibarra</div>
                            <div class="reference-contact">
                                <i class="fas fa-phone"></i>
                                <span>0984697214</span>
                            </div>
                            <div class="reference-contact">
                                <i class="fas fa-envelope"></i>
                                <span>anapalacios04@yahoo.com</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </main>
        
        <footer>
            <p>© 2025 Francis Jefferson Chingal Hernández</p>
            <p>Última actualización: March 18, 2025</p>
            <a href="#" class="download-btn" id="downloadPdf">
                <i class="fas fa-download"></i>
                Descargar CV
            </a>
        </footer>
    </div>
    
    <script>
        // Toggle sections
        const sectionTitles = document.querySelectorAll('.section-title');
        
        sectionTitles.forEach(title => {
            title.addEventListener('click', () => {
                title.classList.toggle('collapsed');
            });
        });
        
        // Skill hover effect for mobile
        const skillItems = document.querySelectorAll('.skill-item');
        
        skillItems.forEach(item => {
            item.addEventListener('click', () => {
                const skillLevel = item.querySelector('.skill-level');
                
                // Toggle visibility instead of hover on mobile
                if (window.innerWidth <= 768) {
                    if (skillLevel.style.opacity === '1') {
                        skillLevel.style.opacity = '0';
                        skillLevel.style.transform = 'translateY(-10px)';
                    } else {
                        skillLevel.style.opacity = '1';
                        skillLevel.style.transform = 'translateY(0)';
                    }
                }
            });
        });
        
        // Download PDF functionality (mock)
        document.getElementById('downloadPdf').addEventListener('click', function(e) {
            e.preventDefault();
            alert('Esta funcionalidad requeriría integración con una biblioteca de generación de PDF como jsPDF o una solución de servidor.');
        });
    </script>
</body>
</html>
