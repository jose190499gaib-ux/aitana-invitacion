<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bautizo y Primer Cumpleaños de Aitana Lilyan - Una Doble Celebración</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700;800&family=Inter:wght@300;400;500;600;700&family=Sacramento&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            overflow-x: hidden;
        }
        
        .playfair {
            font-family: 'Playfair Display', serif;
        }
        
        .sacramento {
            font-family: 'Sacramento', cursive;
        }
        
        /* Colores personalizados */
        :root {
            --rosa-pastel: #f8bbd9;
            --dorado: #d4af37;
            --beige: #f5f5dc;
            --beige-oscuro: #e8e0d1;
            --rosa-claro: #fce7f3;
        }
        
        .bg-rosa-pastel { background-color: var(--rosa-pastel); }
        .bg-dorado { background-color: var(--dorado); }
        .bg-beige { background-color: var(--beige); }
        .bg-beige-oscuro { background-color: var(--beige-oscuro); }
        
        .text-rosa-pastel { color: var(--rosa-pastel); }
        .text-dorado { color: var(--dorado); }
        .text-beige { color: var(--beige); }
        
        .border-rosa-pastel { border-color: var(--rosa-pastel); }
        .border-dorado { border-color: var(--dorado); }
        
        .gradient-bg {
            background: linear-gradient(135deg, var(--rosa-pastel) 0%, var(--beige) 50%, var(--dorado) 100%);
        }
        
        .hero-bg {
            background: linear-gradient(rgba(248, 187, 217, 0.6), rgba(255, 255, 255, 0.95));
            position: relative;
        }
        
        .hero-bg::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><radialGradient id="a" cx="50%" cy="50%"><stop offset="0%" stop-color="%23ffffff" stop-opacity="0.1"/><stop offset="100%" stop-color="%23ffffff" stop-opacity="0"/></radialGradient></defs><circle cx="200" cy="200" r="100" fill="url(%23a)"/><circle cx="800" cy="300" r="150" fill="url(%23a)"/><circle cx="400" cy="700" r="120" fill="url(%23a)"/></svg>');
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .card {
            backdrop-filter: blur(10px);
            background: rgba(255, 255, 255, 0.95);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
            pointer-events: none;
        }
        
        .floating-element {
            position: absolute;
            font-size: 30px;
            animation: floatElement 6s linear infinite;
        }
        
        @keyframes floatElement {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        .countdown-box {
            background: linear-gradient(45deg, #ffffff, rgba(248, 187, 217, 0.1));
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            color: #2d3748;
            margin: 20px 0;
            border: 2px solid var(--rosa-pastel);
            box-shadow: 0 8px 25px rgba(248, 187, 217, 0.2);
        }
        
        .rsvp-form {
            background: linear-gradient(135deg, var(--rosa-pastel), var(--dorado));
            color: white;
        }
        
        .nav-link {
            transition: all 0.3s ease;
        }
        
        .nav-link:hover {
            color: var(--rosa-pastel) !important;
            transform: translateY(-2px);
        }
        
        .section-divider {
            height: 4px;
            background: linear-gradient(90deg, var(--rosa-pastel), var(--dorado));
            border-radius: 2px;
            width: 80px;
            margin: 0 auto 30px;
        }
        
        .btn-primary {
            background: linear-gradient(45deg, var(--rosa-pastel), #e91e63);
            border: none;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(248, 187, 217, 0.3);
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(248, 187, 217, 0.3);
        }
        
        .birthday-theme {
            background: linear-gradient(135deg, var(--rosa-pastel), var(--dorado));
        }
        
        .baptism-theme {
            background: linear-gradient(135deg, var(--dorado), var(--beige-oscuro));
        }
        
        .dual-celebration {
            background: linear-gradient(45deg, var(--dorado) 0%, var(--rosa-pastel) 50%, var(--beige) 100%);
        }
        
        .parents-section {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.98), rgba(248, 248, 248, 0.95));
            backdrop-filter: blur(20px);
            border: 2px solid rgba(248, 187, 217, 0.3);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 20px 40px rgba(248, 187, 217, 0.2);
        }
        
        .parents-names {
            color: #4a5568;
            font-weight: 500;
            line-height: 1.6;
        }
        
        .invitation-text {
            color: #718096;
            font-style: italic;
            margin-top: 15px;
        }
        
        .rsvp-option {
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .rsvp-option:hover {
            transform: scale(1.05);
        }
        
        .rsvp-option.selected {
            border-color: var(--dorado);
            background-color: rgba(212, 175, 55, 0.1);
        }
        
        .admin-panel {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
        }
        
        .admin-button {
            background: linear-gradient(45deg, #4a5568, #2d3748);
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 50%;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .admin-button:hover {
            transform: scale(1.1);
        }
        
        .admin-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.8);
            z-index: 1001;
        }
        
        .admin-content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            border-radius: 20px;
            padding: 30px;
            max-width: 90%;
            max-height: 80%;
            overflow-y: auto;
            width: 600px;
        }
        
        .guest-item {
            padding: 15px;
            border-bottom: 1px solid #e5e5e5;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .status-attending {
            color: #10b981;
            font-weight: bold;
        }
        
        .status-not-attending {
            color: #ef4444;
            font-weight: bold;
        }
        
        @media (max-width: 768px) {
            .parents-section {
                padding: 20px;
                margin-bottom: 20px;
            }
        }
    </style>
</head>
<body class="bg-gradient-to-br from-pink-100 to-white">
    <!-- Floating Elements Animation -->
    <div class="floating-elements"></div>
    
    <!-- Navigation -->
    <nav class="bg-white/90 backdrop-blur-md shadow-lg fixed w-full top-0 z-50">
        <div class="container mx-auto px-4">
            <div class="flex justify-between items-center py-4">
                <div class="sacramento text-3xl font-bold text-rosa-pastel">
                    Aitana Lilyan
                </div>
                <div class="hidden md:flex space-x-8">
                    <a href="#inicio" class="nav-link text-gray-700 hover:text-rosa-pastel font-medium">Inicio</a>
                    <a href="#detalles" class="nav-link text-gray-700 hover:text-rosa-pastel font-medium">Detalles</a>
                    <a href="#rsvp" class="nav-link text-gray-700 hover:text-rosa-pastel font-medium">RSVP</a>
                </div>
                <button class="md:hidden" onclick="toggleMobileMenu()">
                    <i class="fas fa-bars text-gray-700"></i>
                </button>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobileMenu" class="md:hidden bg-white border-t hidden">
            <div class="px-4 py-2 space-y-2">
                <a href="#inicio" class="block py-2 text-gray-700 hover:text-rosa-pastel">Inicio</a>
                <a href="#detalles" class="block py-2 text-gray-700 hover:text-rosa-pastel">Detalles</a>
                <a href="#rsvp" class="block py-2 text-gray-700 hover:text-rosa-pastel">RSVP</a>
            </div>
        </div>
    </nav>

    <!-- Admin Panel -->
    <div class="admin-panel">
        <button class="admin-button" onclick="openAdminPanel()" title="Ver Confirmaciones">
            <i class="fas fa-users"></i>
        </button>
    </div>

    <!-- Admin Modal -->
    <div id="adminModal" class="admin-modal">
        <div class="admin-content">
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-2xl font-bold text-gray-800">Panel de Confirmaciones</h2>
                <button onclick="closeAdminPanel()" class="text-gray-500 hover:text-gray-700">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            
            <!-- Statistics -->
            <div class="grid grid-cols-3 gap-4 mb-6">
                <div class="bg-green-100 p-4 rounded-lg text-center">
                    <div class="text-2xl font-bold text-green-600" id="attendingCount">0</div>
                    <div class="text-green-600">Confirman</div>
                </div>
                <div class="bg-red-100 p-4 rounded-lg text-center">
                    <div class="text-2xl font-bold text-red-600" id="notAttendingCount">0</div>
                    <div class="text-red-600">No asisten</div>
                </div>
                <div class="bg-blue-100 p-4 rounded-lg text-center">
                    <div class="text-2xl font-bold text-blue-600" id="totalCount">0</div>
                    <div class="text-blue-600">Total</div>
                </div>
            </div>
            
            <!-- Guest List -->
            <div class="max-h-96 overflow-y-auto">
                <h3 class="text-lg font-semibold mb-3">Lista de Invitados:</h3>
                <div id="guestList">
                    <p class="text-gray-500 text-center py-8">No hay confirmaciones aún</p>
                </div>
            </div>
            
            <!-- Export Options -->
            <div class="mt-6 flex space-x-4">
                <button onclick="exportToCSV()" class="bg-blue-500 text-white px-4 py-2 rounded-lg hover:bg-blue-600">
                    <i class="fas fa-download mr-2"></i>Exportar CSV
                </button>
                <button onclick="clearAllData()" class="bg-red-500 text-white px-4 py-2 rounded-lg hover:bg-red-600">
                    <i class="fas fa-trash mr-2"></i>Limpiar Datos
                </button>
            </div>
        </div>
    </div>

    <!-- Hero Section -->
    <section id="inicio" class="hero-bg min-h-screen flex items-center justify-center relative">
        <div class="text-center text-gray-800 z-10 px-4 max-w-5xl mx-auto">
            <!-- Parents Section -->
            <div class="parents-section text-gray-700 mb-8">
                <div class="text-center">
                    <h3 class="playfair text-2xl md:text-3xl font-semibold mb-6" style="color: var(--dorado)">Con inmensa alegría</h3>
                    <div class="parents-names text-lg md:text-xl mb-4">
                        <p class="playfair font-semibold text-xl md:text-2xl">Sr. José Luis García Ibañez</p>
                        <p class="text-gray-500 my-2">&</p>
                        <p class="playfair font-semibold text-xl md:text-2xl">Sra. Alidenisse Aguilar Martinez</p>
                    </div>
                    
                    <p class="invitation-text text-base md:text-lg">
                        Tienen el honor de invitarle a celebrar dos momentos muy especiales<br>
                        en la vida de su pequeña hija
                    </p>
                </div>
            </div>
            
            <!-- Padrinos Section -->
            <div class="parents-section text-gray-700 mb-8">
                <div class="text-center">
                    <h3 class="playfair text-2xl md:text-3xl font-semibold mb-6" style="color: var(--rosa-pastel)">Los Padrinos:</h3>
                    <div class="parents-names text-lg md:text-xl">
                        <p class="playfair font-semibold text-xl md:text-2xl">Sr. Fernando De Jesús Benítez Robles</p>
                        <p class="text-gray-500 my-2">&</p>
                        <p class="playfair font-semibold text-xl md:text-2xl">Sra. Andrea Morales Mijangos</p>
                    </div>
                </div>
            </div>
            
            <div class="mb-8">
                <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/b020c114-98e4-4320-a02a-d0865fa93f0e.png" alt="Beautiful animated angel with soft pink wings and golden halo, gently floating with sparkles around, representing divine blessing for baptism celebration" class="mx-auto rounded-full border-4 border-white shadow-2xl" />
            </div>
            
            <h1 class="sacramento text-7xl md:text-9xl font-bold mb-2 text-gray-700">Aitana Lilyan</h1>
            <h2 class="playfair text-3xl md:text-4xl font-medium mb-6 tracking-wide text-gray-600">García Aguilar</h2>
            
            <div class="dual-celebration text-white p-8 rounded-2xl mb-8 inline-block shadow-2xl">
                <h3 class="playfair text-3xl md:text-4xl font-bold mb-4">Bautizo y Primer Cumpleaños</h3>
                <div class="flex items-center justify-center space-x-6 text-4xl">
                    <i class="fas fa-cross"></i>
                    <span class="text-3xl font-light">+</span>
                    <i class="fas fa-birthday-cake"></i>
                </div>
            </div>
            
            <div class="bg-white/80 rounded-2xl p-8 backdrop-blur-sm inline-block mb-8 shadow-xl border border-rosa-pastel/30">
                <p class="playfair text-2xl md:text-3xl mb-3 font-semibold text-gray-700">Sábado, 4 de Octubre 2025</p>
                <p class="text-lg md:text-xl font-light text-gray-600">Una doble bendición para celebrar</p>
            </div>
            
            <!-- Countdown Timer -->
            <div class="countdown-box mt-8 inline-block shadow-xl">
                <h3 class="playfair text-xl font-semibold mb-4">Faltan para la celebración:</h3>
                <div id="countdown" class="flex justify-center space-x-4 text-2xl font-bold flex-wrap gap-4"></div>
            </div>
            
            <div class="mt-10 space-y-4 md:space-y-0 md:space-x-6 flex flex-col md:flex-row justify-center">
                <button onclick="document.getElementById('rsvp').scrollIntoView({behavior: 'smooth'})" class="btn-primary bg-white text-rosa-pastel px-8 py-4 rounded-full font-semibold hover:bg-gray-100 transition-all duration-300 text-lg shadow-lg">
                    <i class="fas fa-envelope mr-2"></i>Confirmar Asistencia
                </button>
                <button onclick="document.getElementById('detalles').scrollIntoView({behavior: 'smooth'})" class="bg-white/80 backdrop-blur-sm text-gray-700 px-8 py-4 rounded-full font-semibold hover:bg-white transition-all duration-300 text-lg shadow-lg border border-rosa-pastel/30">
                    <i class="fas fa-info-circle mr-2"></i>Ver Detalles
                </button>
            </div>
        </div>
    </section>

    <!-- Event Details -->
    <section id="detalles" class="py-20 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="playfair text-5xl md:text-6xl text-center text-gray-800 mb-4 font-bold">Ubicaciones y Horarios</h2>
            <div class="section-divider"></div>
            
            <div class="grid md:grid-cols-2 gap-10 mt-16 max-w-6xl mx-auto">
                <!-- Bautizo -->
                <div class="card rounded-2xl p-10 text-center shadow-2xl baptism-theme text-white transform hover:scale-105 transition-all duration-300">
                    <div class="text-5xl mb-6">
                        <i class="fas fa-cross"></i>
                    </div>
                    <h3 class="playfair text-3xl font-bold mb-6">Ceremonia de Bautizo</h3>
                    <div class="space-y-4">
                        <p class="text-xl font-semibold">Iglesia Santa Cruz</p>
                        <div class="bg-white/20 rounded-lg p-4 backdrop-blur-sm">
                            <p class="text-2xl font-bold">12:00 PM</p>
                        </div>
                        <p class="text-base opacity-90 leading-relaxed">Sacramento de purificación y bendición<br>Una nueva vida en Cristo</p>
                        <div class="map-container h-48 bg-gray-200 rounded-xl mt-6 relative overflow-hidden shadow-lg">
                            <iframe 
                                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3048.5!2d-101.123!3d22.456!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjLCsDI3JzIxLjYiTiAxMDHCsDA3JzIzLjAiVw!5e0!3m2!1ses!2smx!4v1234567890" 
                                width="100%" 
                                height="100%" 
                                style="border:0;" 
                                allowfullscreen="" 
                                loading="lazy">
                            </iframe>
                        </div>
                        <a href="https://maps.app.goo.gl/NuTyCNi9dUaNYAsu9?g_st=aw" target="_blank" class="inline-block bg-white text-yellow-600 px-6 py-3 rounded-full text-sm font-semibold hover:bg-yellow-50 transition-all duration-300 mt-4 shadow-lg">
                            <i class="fas fa-map-marker-alt mr-2"></i>Ver en Mapa
                        </a>
                    </div>
                </div>
                
                <!-- Cumpleaños -->
                <div class="card rounded-2xl p-10 text-center shadow-2xl birthday-theme text-white transform hover:scale-105 transition-all duration-300">
                    <div class="text-5xl mb-6">
                        <i class="fas fa-birthday-cake"></i>
                    </div>
                    <h3 class="playfair text-3xl font-bold mb-6">Fiesta de Cumpleaños</h3>
                    <div class="space-y-4">
                        <p class="text-xl font-semibold">Salón Aru</p>
                        <div class="bg-white/20 rounded-lg p-4 backdrop-blur-sm">
                            <p class="text-2xl font-bold">3:30 PM</p>
                        </div>
                        <p class="text-base opacity-90 leading-relaxed">Celebrando su primer año de vida<br>Con alegría y amor familiar</p>
                        <div class="map-container h-48 bg-gray-200 rounded-xl mt-6 relative overflow-hidden shadow-lg">
                            <iframe 
                                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3048.5!2d-101.456!3d22.789!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjLCsDQ3JzIwLjAiTiAxMDHCsDI3JzIxLjYiVw!5e0!3m2!1ses!2smx!4v1234567891" 
                                width="100%" 
                                height="100%" 
                                style="border:0;" 
                                allowfullscreen="" 
                                loading="lazy">
                            </iframe>
                        </div>
                        <a href="https://maps.app.goo.gl/yNfRKNf47Qqd6MSx5?g_st=aw" target="_blank" class="inline-block bg-white text-pink-600 px-6 py-3 rounded-full text-sm font-semibold hover:bg-pink-50 transition-all duration-300 mt-4 shadow-lg">
                            <i class="fas fa-map-marker-alt mr-2"></i>Ver en Mapa
                        </a>
                    </div>
                </div>
            </div>
            
            <!-- Additional Info -->
            <div class="grid md:grid-cols-2 gap-8 mt-16 max-w-4xl mx-auto">
                <div class="card rounded-xl p-8 text-center shadow-lg transform hover:scale-105 transition-all duration-300">
                    <div class="text-rosa-pastel text-4xl mb-4 relative">
                        <i class="fas fa-envelope"></i>
                        <span class="absolute -top-2 -right-2 text-dorado text-2xl">
                            <i class="fas fa-dollar-sign"></i>
                        </span>
                    </div>
                    <h4 class="playfair text-xl font-semibold mb-3">Regalo Especial</h4>
                    <p class="text-gray-700 font-medium">Gracias por permitirme escoger mi regalo</p>
                    <p class="text-sm text-gray-500 mt-3 italic">Tu aportación será muy apreciada</p>
                </div>
                
                <div class="card rounded-xl p-8 text-center shadow-lg transform hover:scale-105 transition-all duration-300">
                    <div class="text-rosa-pastel text-4xl mb-4">
                        <i class="fas fa-music"></i>
                    </div>
                    <h4 class="playfair text-xl font-semibold mb-3">Entretenimiento</h4>
                    <p class="text-gray-700 font-medium">La Explosión de la Kumbia</p>
                    <p class="text-sm text-gray-500 mt-3 italic">Música y diversión para toda la familia</p>
                </div>
            </div>
        </div>
    </section>

    <!-- RSVP Section -->
    <section id="rsvp" class="py-20" style="background-color: var(--rosa-claro);">
        <div class="container mx-auto px-4">
            <h2 class="playfair text-5xl md:text-6xl text-center text-gray-800 mb-4 font-bold">Confirma tu Asistencia</h2>
            <div class="section-divider"></div>
            
            <div class="max-w-2xl mx-auto mt-12">
                <div class="card rounded-2xl p-8 shadow-2xl">
                    <form id="rsvpForm" class="space-y-6">
                        <div>
                            <label for="nombre" class="block text-lg font-semibold text-gray-700 mb-3">Nombre completo</label>
                            <input type="text" id="nombre" name="nombre" required 
                                   class="w-full px-4 py-3 border-2 border-rosa-pastel rounded-lg focus:outline-none focus:border-dorado transition-colors duration-300 text-lg">
                        </div>
                        
                        <div>
                            <label class="block text-lg font-semibold text-gray-700 mb-4">¿Podrás acompañarnos?</label>
                            <div class="grid md:grid-cols-2 gap-4">
                                <div class="rsvp-option border-2 border-gray-300 rounded-lg p-6 text-center" onclick="selectOption('si')">
                                    <div class="text-green-500 text-4xl mb-3">
                                        <i class="fas fa-check-circle"></i>
                                    </div>
                                    <h4 class="playfair text-xl font-semibold text-gray-700">¡Sí, ahí estaré!</h4>
                                    <p class="text-gray-500 mt-2">Confirmo mi asistencia</p>
                                    <input type="radio" name="asistencia" value="si" class="hidden">
                                </div>
                                
                                <div class="rsvp-option border-2 border-gray-300 rounded-lg p-6 text-center" onclick="selectOption('no')">
                                    <div class="text-red-500 text-4xl mb-3">
                                        <i class="fas fa-times-circle"></i>
                                    </div>
                                    <h4 class="playfair text-xl font-semibold text-gray-700">No podré asistir</h4>
                                    <p class="text-gray-500 mt-2">Lamento no poder acompañarlos</p>
                                    <input type="radio" name="asistencia" value="no" class="hidden">
                                </div>
                            </div>
                        </div>
                        
                        <div>
                            <label for="mensaje" class="block text-lg font-semibold text-gray-700 mb-3">Mensaje para la familia (opcional)</label>
                            <textarea id="mensaje" name="mensaje" rows="4" 
                                      class="w-full px-4 py-3 border-2 border-rosa-pastel rounded-lg focus:outline-none focus:border-dorado transition-colors duration-300 text-lg"
                                      placeholder="Escribe un mensaje especial para Aitana y su familia..."></textarea>
                        </div>
                        
                        <div class="text-center">
                            <button type="submit" class="btn-primary text-white px-8 py-4 rounded-full font-semibold text-lg shadow-lg transform hover:scale-105 transition-all duration-300">
                                <i class="fas fa-paper-plane mr-2"></i>Enviar Confirmación
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-4 text-center">
            <h3 class="sacramento text-3xl mb-4 text-rosa-pastel">Aitana Lilyan García Aguilar</h3>
            <p class="text-gray-300 mb-6">Bautizo y Primer Cumpleaños</p>
            <p class="text-gray-400">4 de Octubre 2025</p>
            <div class="mt-8 text-gray-500">
                <p>Con amor, la familia García Aguilar</p>
            </div>
        </div>
    </footer>

    <script>
        // Toggle mobile menu
        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        // Countdown timer
        function updateCountdown() {
            const eventDate = new Date('2025-10-04T12:00:00').getTime();
            const now = new Date().getTime();
            const timeLeft = eventDate - now;

            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);

            document.getElementById('countdown').innerHTML = `
                <div class="text-center">
                    <div class="text-3xl font-bold">${days}</div>
                    <div class="text-sm">Días</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl font-bold">${hours}</div>
                    <div class="text-sm">Horas</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl font-bold">${minutes}</div>
                    <div class="text-sm">Minutos</div>
                </div>
                <div class="text-center">
                    <div class="text-3xl font-bold">${seconds}</div>
                    <div class="text-sm">Segundos</div>
                </div>
            `;

            if (timeLeft < 0) {
                document.getElementById('countdown').innerHTML = '<div class="text-2xl font-bold">¡Es hoy!</div>';
            }
        }

        setInterval(updateCountdown, 1000);
        updateCountdown();

        // RSVP form functionality
        function selectOption(option) {
            // Remove selected class from all options
            document.querySelectorAll('.rsvp-option').forEach(el => {
                el.classList.remove('selected');
            });
            
            // Add selected class to clicked option
            event.currentTarget.classList.add('selected');
            
            // Check the corresponding radio button
            document.querySelector(input[value="${option}"]).checked = true;
        }

        // Handle form submission
        document.getElementById('rsvpForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const nombre = document.getElementById('nombre').value;
            const asistencia = document.querySelector('input[name="asistencia"]:checked');
            const mensaje = document.getElementById('mensaje').value;
            
            if (!nombre || !asistencia) {
                alert('Por favor completa todos los campos requeridos.');
                return;
            }
            
            // Create form data object
            const formData = {
                nombre: nombre,
                asistencia: asistencia.value,
                mensaje: mensaje,
                fecha: new Date().toISOString(),
                id: Date.now() // Simple ID generation
            };
            
            // Save to localStorage
            saveGuestResponse(formData);
            
            console.log('Datos del formulario:', formData);
            
            // Show confirmation message
            alert(¡Gracias ${nombre}! Tu respuesta ha sido registrada. ${asistencia.value === 'si' ? '¡Nos vemos en la celebración!' : 'Lamentamos que no puedas acompañarnos.'});
            
            // Reset form
            this.reset();
            document.querySelectorAll('.rsvp-option').forEach(el => {
                el.classList.remove('selected');
            });
        });

        // Guest management functions
        function saveGuestResponse(guestData) {
            let guests = JSON.parse(localStorage.getItem('weddingGuests')) || [];
            
            // Check if guest already exists (by name)
            const existingIndex = guests.findIndex(g => g.nombre.toLowerCase() === guestData.nombre.toLowerCase());
            
            if (existingIndex !== -1) {
                // Update existing guest
                guests[existingIndex] = guestData;
            } else {
                // Add new guest
                guests.push(guestData);
            }
            
            localStorage.setItem('weddingGuests', JSON.stringify(guests));
        }

        function getGuestResponses() {
            return JSON.parse(localStorage.getItem('weddingGuests')) || [];
        }

        function openAdminPanel() {
            document.getElementById('adminModal').style.display = 'block';
            loadGuestList();
        }

        function closeAdminPanel() {
            document.getElementById('adminModal').style.display = 'none';
        }

        function loadGuestList() {
            const guests = getGuestResponses();
            const guestListEl = document.getElementById('guestList');
            const attendingCountEl = document.getElementById('attendingCount');
            const notAttendingCountEl = document.getElementById('notAttendingCount');
            const totalCountEl = document.getElementById('totalCount');
            
            // Calculate statistics
            const attending = guests.filter(g => g.asistencia === 'si').length;
            const notAttending = guests.filter(g => g.asistencia === 'no').length;
            const total = guests.length;
            
            // Update counters
            attendingCountEl.textContent = attending;
            notAttendingCountEl.textContent = notAttending;
            totalCountEl.textContent = total;
            
            // Update guest list
            if (guests.length === 0) {
                guestListEl.innerHTML = '<p class="text-gray-500 text-center py-8">No hay confirmaciones aún</p>';
                return;
            }
            
            const guestHTML = guests.map(guest => {
                const statusClass = guest.asistencia === 'si' ? 'status-attending' : 'status-not-attending';
                const statusText = guest.asistencia === 'si' ? 'Asiste' : 'No asiste';
                const statusIcon = guest.asistencia === 'si' ? 'fa-check' : 'fa-times';
                
                return `
                    <div class="guest-item">
                        <div>
                            <div class="font-semibold">${guest.nombre}</div>
                            <div class="text-sm text-gray-500">${new Date(guest.fecha).toLocaleDateString('es-ES')}</div>
                            ${guest.mensaje ? <div class="text-sm text-gray-600 mt-1 italic">"${guest.mensaje}"</div> : ''}
                        </div>
                        <div class="${statusClass}">
                            <i class="fas ${statusIcon} mr-1"></i>${statusText}
                        </div>
                    </div>
                `;
            }).join('');
            
            guestListEl.innerHTML = guestHTML;
        }

        function exportToCSV() {
            const guests = getGuestResponses();
            if (guests.length === 0) {
                alert('No hay datos para exportar');
                return;
            }
            
            // Create CSV content
            const headers = ['Nombre', 'Asistencia', 'Mensaje', 'Fecha'];
            const csvContent = [
                headers.join(','),
                ...guests.map(guest => [
                    "${guest.nombre}",
                    guest.asistencia === 'si' ? 'Asiste' : 'No asiste',
                    "${guest.mensaje || ''}",
                    new Date(guest.fecha).toLocaleDateString('es-ES')
                ].join(','))
            ].join('\n');
            
            // Download CSV
            const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });
            const link = document.createElement('a');
            link.href = URL.createObjectURL(blob);
            link.download = 'confirmaciones_bautizo_aitana.csv';
            link.click();
        }

        function clearAllData() {
            if (confirm('¿Estás seguro de que quieres eliminar todas las confirmaciones? Esta acción no se puede deshacer.')) {
                localStorage.removeItem('weddingGuests');
                loadGuestList();
                alert('Todos los datos han sido eliminados.');
            }
        }

        // Close admin modal when clicking outside
        document.getElementById('adminModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeAdminPanel();
            }
        });

        // Floating elements animation
        function createFloatingElement() {
            const elements = ['💕', '✨', '👶', '🎂', '⭐', '💖'];
            const element = document.createElement('div');
            element.className = 'floating-element';
            element.textContent = elements[Math.floor(Math.random() * elements.length)];
            element.style.left = Math.random() * 100 + 'vw';
            element.style.animationDuration = (Math.random() * 3 + 4) + 's';
            element.style.color = hsl(${Math.random() * 60 + 300}, 70%, 80%);
            
            document.querySelector('.floating-elements').appendChild(element);
            
            setTimeout(() => {
                element.remove();
            }, 6000);
        }

        setInterval(createFloatingElement, 3000);

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
                
                // Close mobile menu if open
                document.getElementById('mobileMenu').classList.add('hidden');
            });
        });
    </script>
</body>
</html>
