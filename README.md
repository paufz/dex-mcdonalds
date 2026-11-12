[estaci_n_rob_tica_de_combos_presentaci_n_oficial.html](https://github.com/user-attachments/files/34772743/estaci_n_rob_tica_de_combos_presentaci_n_oficial.html)
<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Estación Robótica de Combos | Presentación Oficial & Capacitación</title>

  <!-- Tailwind CSS via CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Google Fonts: Plus Jakarta Sans & Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Plus+Jakarta+Sans:wght@700;800;900&display=swap" rel="stylesheet">

  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>

  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: {
              red: '#db0007',
              redDark: '#b30006',
              crimson: '#df0915',
              magenta: '#8a1e56',
              amber: '#f19f00',
              yellow: '#ffbc0d',
              yellowLight: '#ffd04d',
              dark: '#27251f',
              cream: '#f7f4f1',
              canvas: '#F9F9F9',
              cardGray: '#F1F2F4',
            }
          },
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            display: ['Plus Jakarta Sans', 'sans-serif'],
          },
          boxShadow: {
            'card': '0 10px 30px -5px rgba(39, 37, 31, 0.06)',
            'phone': '0 25px 50px -12px rgba(39, 37, 31, 0.28)',
          }
        }
      }
    }
  </script>

  <style>
    /* Gradientes exactos solicitados */
    .bg-vertical-tri {
      background: linear-gradient(180deg, #8a1e56 0%, #df0915 50%, #f19f00 100%);
    }

    .text-gradient-tri {
      background: linear-gradient(90deg, #f19f00 0%, #df0915 50%, #8a1e56 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      color: transparent;
      display: inline-block;
    }

    .bg-form-fade {
      background: linear-gradient(180deg, #ffffff 0%, #f19f00 100%);
    }

    /* Transiciones fluidas para las pantallas de los celulares */
    @keyframes phoneScreenEnter {
      from {
        opacity: 0;
        transform: translateX(14px) scale(0.985);
      }
      to {
        opacity: 1;
        transform: translateX(0) scale(1);
      }
    }

    .animate-phone-screen {
      animation: phoneScreenEnter 0.28s cubic-bezier(0.22, 1, 0.36, 1) forwards;
    }

    @keyframes pulseRingSoft {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.04); }
    }

    .animate-pulse-soft {
      animation: pulseRingSoft 2s infinite ease-in-out;
    }
  </style>
</head>
<body class="bg-brand-canvas text-brand-dark font-sans antialiased selection:bg-brand-yellow selection:text-brand-dark overflow-x-hidden">

  <!-- ==================== 1. TOP NAVBAR (#27251f) ==================== -->
  <header class="sticky top-0 left-0 right-0 z-50 bg-brand-dark text-white shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
      <!-- Left: Hamburger Menu + Golden Arches 'M' (#ffbc0d) -->
      <div class="flex items-center gap-4">
        <button id="menu-toggle" aria-label="Abrir menú" class="p-2 rounded-xl hover:bg-white/10 active:scale-95 transition focus:outline-none focus:ring-2 focus:ring-brand-yellow cursor-pointer">
          <i data-lucide="menu" class="w-6 h-6 text-white"></i>
        </button>

        <a href="#hero" class="flex items-center gap-2.5 group" aria-label="Inicio">
          <svg class="w-9 h-7 transition-transform duration-300 group-hover:scale-105" viewBox="0 0 100 80" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 72C12 36 22 10 33 10C44 10 47 38 47 68H53C53 38 56 10 67 10C78 10 88 36 88 72" stroke="#ffbc0d" stroke-width="11" stroke-linecap="round"/>
          </svg>
        </a>
      </div>

      <!-- Center: Desktop Quick Navigation -->
      <nav class="hidden lg:flex items-center gap-7 text-sm font-medium text-white/80">
        <a href="#beneficios" class="hover:text-brand-yellow transition">Beneficios</a>
        <a href="#app-gestion" class="hover:text-brand-yellow transition">App de gestión</a>
        <a href="#resultados" class="hover:text-brand-yellow transition">Resultados</a>
      </nav>

      <!-- Right: Pill Yellow CTA Button (#ffbc0d with #27251f text) -->
      <div>
        <a href="#registro" class="inline-flex items-center justify-center bg-brand-yellow hover:bg-brand-yellowLight text-brand-dark font-display font-extrabold text-xs sm:text-sm px-5 py-2.5 rounded-full shadow-sm transition transform hover:-translate-y-0.5 active:translate-y-0">
          Reservar lugar
        </a>
      </div>
    </div>
  </header>

  <!-- Slide-Over Navigation Drawer -->
  <div id="nav-drawer-backdrop" class="fixed inset-0 bg-black/60 backdrop-blur-xs z-50 hidden opacity-0 transition-opacity duration-300"></div>
  <aside id="nav-drawer" class="fixed top-0 left-0 bottom-0 w-72 sm:w-80 bg-brand-dark text-white z-50 transform -translate-x-full transition-transform duration-300 ease-out shadow-2xl flex flex-col justify-between p-6">
    <div>
      <div class="flex items-center justify-between pb-6 border-b border-white/10">
        <div class="flex items-center gap-2.5">
          <svg class="w-8 h-6" viewBox="0 0 100 80" fill="none">
            <path d="M12 72C12 36 22 10 33 10C44 10 47 38 47 68H53C53 38 56 10 67 10C78 10 88 36 88 72" stroke="#ffbc0d" stroke-width="11" stroke-linecap="round"/>
          </svg>
          <span class="font-display font-bold text-base">Menú</span>
        </div>
        <button id="menu-close" aria-label="Cerrar menú" class="p-2 rounded-xl hover:bg-white/10 transition cursor-pointer">
          <i data-lucide="x" class="w-5 h-5 text-white"></i>
        </button>
      </div>

      <ul class="mt-6 space-y-2">
        <li>
          <a href="#hero" class="drawer-link flex items-center gap-3 px-4 py-3 rounded-2xl hover:bg-white/10 font-medium transition">
            <i data-lucide="sparkles" class="w-5 h-5 text-brand-yellow"></i> Inicio
          </a>
        </li>
        <li>
          <a href="#beneficios" class="drawer-link flex items-center gap-3 px-4 py-3 rounded-2xl hover:bg-white/10 font-medium transition">
            <i data-lucide="shield-check" class="w-5 h-5 text-brand-yellow"></i> 4 Pilares Clave
          </a>
        </li>
        <li>
          <a href="#app-gestion" class="drawer-link flex items-center gap-3 px-4 py-3 rounded-2xl hover:bg-white/10 font-medium transition">
            <i data-lucide="smartphone" class="w-5 h-5 text-brand-yellow"></i> App de Gestión
          </a>
        </li>
        <li>
          <a href="#resultados" class="drawer-link flex items-center gap-3 px-4 py-3 rounded-2xl hover:bg-white/10 font-medium transition">
            <i data-lucide="bar-chart-3" class="w-5 h-5 text-brand-yellow"></i> Datos & Testimonios
          </a>
        </li>
      </ul>
    </div>

    <div class="pt-6 border-t border-white/10">
      <p class="text-xs text-white/60 mb-3">Cupos limitados para demostración en vivo y certificación técnica.</p>
      <a href="#registro" class="drawer-link block w-full text-center bg-brand-yellow text-brand-dark font-display font-extrabold text-sm py-3 rounded-full hover:bg-brand-yellowLight transition">
        Reservar lugar
      </a>
    </div>
  </aside>

  <!-- ==================== 2. HERO SECTION ==================== -->
  <section id="hero" class="max-w-7xl mx-auto px-0 sm:px-6 lg:px-8">
    <div class="relative rounded-b-[40px] sm:rounded-b-[52px] overflow-hidden text-white shadow-2xl bg-vertical-tri">
      <div class="relative z-10 max-w-4xl mx-auto text-center px-6 sm:px-12 lg:px-16 py-16 sm:py-22 lg:py-26 space-y-6">
        <h1 class="font-display font-black text-4xl sm:text-5xl lg:text-[3.85rem] leading-[1.06] tracking-tight text-white">
          Tu combo perfecto, armado a la vista en <span class="text-[#f19f00]">minutos</span>
        </h1>

        <p class="text-base sm:text-lg text-white/95 max-w-2xl mx-auto leading-relaxed font-normal">
          viví la presentación oficial de la primera estación robótica de comida rápida. optimizá tus horas pico con procesos automatizados y capacitá a tu personal en operación autónoma.
        </p>

        <div class="pt-2">
          <a href="#registro" class="inline-flex items-center justify-center gap-3 bg-[#27251f] hover:bg-black text-white font-display font-extrabold text-xs sm:text-sm tracking-wide uppercase px-7 sm:px-9 py-4 rounded-full shadow-xl hover:shadow-2xl transition transform hover:-translate-y-0.5 active:translate-y-0">
            <span>RESERVAR MI LUGAR EN LA PRESENTACIÓN Y CAPACITACIÓN</span>
            <span class="text-white text-base leading-none">→</span>
          </a>
        </div>
      </div>
    </div>
  </section>

  <!-- ==================== 3. CENTERED TITLE + 4-COLUMN BENEFITS GRID ==================== -->
  <section id="beneficios" class="pt-16 sm:pt-24 pb-14 sm:pb-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center max-w-3xl mx-auto mb-12 sm:mb-14">
      <h2 class="font-display font-black text-3xl sm:text-5xl leading-[1.1] tracking-tight text-brand-dark">
        Una precisión tan exacta que los errores pasan al <span class="text-gradient-tri">olvido</span>
      </h2>
    </div>

    <!-- 4-Column Benefits Grid -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
      
      <!-- Card 01 -->
      <div class="bg-[#f7f4f1] border border-zinc-200/70 rounded-2xl p-6 shadow-card hover:shadow-xl transition-all duration-300 hover:-translate-y-1 flex flex-col justify-between">
        <div>
          <span class="inline-block bg-[#db0007] text-white font-display font-extrabold text-xs px-3 py-1 rounded-md mb-5">
            01
          </span>
          <h3 class="font-display font-extrabold text-xl text-[#db0007] leading-snug mb-3">
            Cero desperdicio y armado impecable
          </h3>
          <p class="text-sm text-[#db0007] leading-relaxed font-medium">
            Garantizá que cada combo salga idéntico a lo seleccionado por el cliente, eliminando descartes, errores y pérdidas.
          </p>
        </div>
      </div>

      <!-- Card 02 -->
      <div class="bg-[#ffbc0d] rounded-2xl p-6 shadow-card hover:shadow-xl transition-all duration-300 hover:-translate-y-1 flex flex-col justify-between text-[#27251f]">
        <div>
          <span class="inline-block bg-[#27251f] text-[#ffbc0d] font-display font-extrabold text-xs px-3 py-1 rounded-md mb-5">
            02
          </span>
          <h3 class="font-display font-extrabold text-xl text-[#27251f] leading-snug mb-3">
            Alivio total en las horas pico
          </h3>
          <p class="text-sm text-[#27251f] leading-relaxed font-medium">
            Despachá pedidos completos de forma continua durante los turnos de alta demanda, sin cuellos de botella ni saturación del equipo.
          </p>
        </div>
      </div>

      <!-- Card 03 -->
      <div class="bg-[#db0007] rounded-2xl p-6 shadow-card hover:shadow-xl transition-all duration-300 hover:-translate-y-1 flex flex-col justify-between text-white">
        <div>
          <span class="inline-block bg-white text-[#db0007] font-display font-extrabold text-xs px-3 py-1 rounded-md mb-5">
            03
          </span>
          <h3 class="font-display font-extrabold text-xl text-white leading-snug mb-3">
            Confianza y atracción visual
          </h3>
          <p class="text-sm text-white/95 leading-relaxed">
            Transformá la espera en entretenimiento para el público, generando transparencia y comodidad en el salón.
          </p>
        </div>
      </div>

      <!-- Card 04 -->
      <div class="bg-[#27251f] rounded-2xl p-6 shadow-card hover:shadow-xl transition-all duration-300 hover:-translate-y-1 flex flex-col justify-between text-[#ffbc0d]">
        <div>
          <span class="inline-block bg-[#ffbc0d] text-[#27251f] font-display font-extrabold text-xs px-3 py-1 rounded-md mb-5">
            04
          </span>
          <h3 class="font-display font-extrabold text-xl text-[#ffbc0d] leading-snug mb-3">
            Operación experta garantizada
          </h3>
          <p class="text-sm text-[#ffbc0d]/95 leading-relaxed">
            Capacitá a tu equipo mediante talleres prácticos para que operen de manera autónoma desde el primer día.
          </p>
        </div>
      </div>

    </div>
  </section>

  <!-- ==================== 4. APP DE GESTIÓN & SINGLE SMARTPHONE SIMULATOR ==================== -->
  <section id="app-gestion" class="py-16 sm:py-24 bg-white border-y border-zinc-100">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
        
        <!-- Left Column (5 cols) -->
        <div class="lg:col-span-5 space-y-5">
          <h2 class="font-display font-black text-3xl sm:text-4xl text-brand-dark leading-[1.12] tracking-tight">
            Monitoreá sin esfuerzo desde una sola <span class="text-gradient-tri">interfaz</span>
          </h2>

          <p class="text-sm sm:text-base text-zinc-600 leading-relaxed">
            App de gestión para empleados y mantenimiento predictivo. Controlá el stock, las reposiciones paso a paso y el estado de los sensores en tiempo real.
          </p>

          <!-- 3 Interactive Feature Items -->
          <div class="space-y-3.5 pt-2" id="app-feature-list">
            <button type="button" data-jump-screen="3" class="app-feature-btn w-full text-left bg-brand-canvas hover:bg-zinc-100/90 rounded-2xl p-4 sm:p-5 border-2 border-brand-red/30 transition cursor-pointer">
              <div class="flex items-center gap-2.5 mb-1.5">
                <span class="w-2.5 h-2.5 rounded-full bg-brand-red shrink-0"></span>
                <h3 class="font-display font-extrabold text-base text-brand-dark">Control de stock en tiempo real</h3>
              </div>
              <p class="text-xs sm:text-sm text-zinc-600 leading-relaxed pl-5">
                Tu personal visualiza el porcentaje de cada bandeja desde la app para adelantarse a las recargas.
              </p>
            </button>

            <button type="button" data-jump-screen="5" class="app-feature-btn w-full text-left bg-brand-canvas hover:bg-zinc-100/90 rounded-2xl p-4 sm:p-5 border-2 border-transparent transition cursor-pointer">
              <div class="flex items-center gap-2.5 mb-3">
                <span class="w-2.5 h-2.5 rounded-full bg-brand-red shrink-0"></span>
                <h3 class="font-display font-extrabold text-base text-brand-dark">Alertas dinámicas por balanza integrada</h3>
              </div>

              <div class="space-y-3 pl-1">
                <div class="flex items-start gap-3">
                  <span class="shrink-0 bg-brand-red text-white font-display font-extrabold text-[11px] px-2.5 py-1 rounded-full tracking-wide">
                    50% PICO
                  </span>
                  <p class="text-xs text-zinc-600 leading-relaxed">
                    Alerta temprana al 50% para evitar quiebres de stock.
                  </p>
                </div>

                <div class="flex items-start gap-3">
                  <span class="shrink-0 bg-brand-yellow text-brand-dark font-display font-extrabold text-[11px] px-2.5 py-1 rounded-full tracking-wide">
                    30% VALLE
                  </span>
                  <p class="text-xs text-zinc-600 leading-relaxed">
                    Aviso al 30% en horarios tranquilos para optimizar recargas.
                  </p>
                </div>
              </div>
            </button>

            <button type="button" data-jump-screen="8" class="app-feature-btn w-full text-left bg-brand-canvas hover:bg-zinc-100/90 rounded-2xl p-4 sm:p-5 border-2 border-transparent transition cursor-pointer">
              <div class="flex items-center gap-2.5 mb-1.5">
                <span class="w-2.5 h-2.5 rounded-full bg-brand-red shrink-0"></span>
                <h3 class="font-display font-extrabold text-base text-brand-dark">Mantenimiento simplificado</h3>
              </div>
              <p class="text-xs sm:text-sm text-zinc-600 leading-relaxed pl-5">
                Diagnósticos automáticos de sensor, guía guiada por peso objetivo y solicitud de asistencia inmediata.
              </p>
            </button>
          </div>
        </div>

        <!-- Right Column: Single Functional Smartphone Simulator (7 cols) -->
        <div class="lg:col-span-7 flex flex-col items-center">
          <!-- Screen Stepper & Mode Controls -->
          <div class="mb-5 w-full max-w-md">
            <div class="flex flex-wrap items-center justify-center gap-1.5 mb-2.5">
              <button type="button" data-screen="inicio" class="screen-nav-pill text-[11px] font-display font-extrabold px-3 py-1.5 rounded-full transition cursor-pointer bg-[#db0007] text-white shadow-xs">
                Inicio
              </button>
              <button type="button" data-screen="maquinas" class="screen-nav-pill text-[11px] font-display font-extrabold px-3 py-1.5 rounded-full transition cursor-pointer bg-zinc-100 hover:bg-zinc-200 text-brand-dark">
                Máquinas
              </button>
              <button type="button" data-screen="detalle" class="screen-nav-pill text-[11px] font-display font-extrabold px-3 py-1.5 rounded-full transition cursor-pointer bg-zinc-100 hover:bg-zinc-200 text-brand-dark">
                Ingredientes
              </button>
              <button type="button" data-screen="instrucciones" class="screen-nav-pill text-[11px] font-display font-extrabold px-3 py-1.5 rounded-full transition cursor-pointer bg-zinc-100 hover:bg-zinc-200 text-brand-dark">
                Reposición
              </button>
              <button type="button" data-screen="proceso" class="screen-nav-pill text-[11px] font-display font-extrabold px-3 py-1.5 rounded-full transition cursor-pointer bg-zinc-100 hover:bg-zinc-200 text-brand-dark">
                Balanza
              </button>
              <button type="button" data-screen="error" class="screen-nav-pill text-[11px] font-display font-extrabold px-3 py-1.5 rounded-full transition cursor-pointer bg-zinc-100 hover:bg-zinc-200 text-brand-dark">
                Sensor
              </button>
            </div>

            <!-- Threshold Toggle (30% Valle / 50% Pico) & Reset Demo -->
            <div class="flex flex-wrap items-center justify-center gap-2">
              <span class="text-[11px] font-semibold text-zinc-500">Modo turno:</span>
              <button type="button" id="sim-valle-btn" class="text-[11px] font-display font-extrabold px-3 py-1 rounded-full bg-brand-yellow text-brand-dark shadow-xs cursor-pointer transition">
                30% VALLE
              </button>
              <button type="button" id="sim-pico-btn" class="text-[11px] font-display font-extrabold px-3 py-1 rounded-full bg-zinc-200 hover:bg-brand-red hover:text-white text-brand-dark cursor-pointer transition">
                50% PICO
              </button>
              <button type="button" id="sim-reset-btn" title="Reiniciar simulación" class="text-[11px] font-semibold px-2.5 py-1 rounded-full bg-zinc-100 hover:bg-zinc-200 text-zinc-600 cursor-pointer transition inline-flex items-center gap-1">
                <i data-lucide="rotate-ccw" class="w-3 h-3"></i> Reiniciar
              </button>
            </div>
          </div>

          <!-- SINGLE FUNCTIONAL IPHONE MOCKUP -->
          <div class="w-[300px] sm:w-[310px] bg-brand-dark rounded-[2.85rem] p-3.5 shadow-phone border-4 border-zinc-800 relative">
            <div class="w-28 h-5 bg-brand-dark rounded-b-2xl mx-auto absolute top-3.5 left-1/2 -translate-x-1/2 z-20 flex items-center justify-center">
              <div class="w-10 h-1 bg-zinc-700 rounded-full"></div>
            </div>

            <div class="bg-brand-canvas rounded-[2.25rem] overflow-hidden h-[565px] flex flex-col justify-between">
              <div id="phone-main-viewport" class="flex-1 flex flex-col overflow-hidden">
                <!-- Rendered dynamically by JS -->
              </div>

              <!-- Persistent Functional Bottom Tab Bar -->
              <div class="bg-white border-t border-zinc-200 px-3 py-2.5 flex items-center justify-around text-[10px] font-semibold text-zinc-400 shrink-0">
                <button type="button" data-nav-tab="inicio" class="phone-tab-btn flex flex-col items-center gap-0.5 text-[#db0007] font-bold cursor-pointer transition">
                  <i data-lucide="home" class="w-4 h-4"></i>
                  <span>Inicio</span>
                </button>
                <button type="button" data-nav-tab="maquinas" class="phone-tab-btn flex flex-col items-center gap-0.5 hover:text-brand-dark cursor-pointer transition relative">
                  <i data-lucide="cpu" class="w-4 h-4"></i>
                  <span>Máquinas</span>
                  <span id="tab-alert-badge" class="w-2 h-2 rounded-full bg-[#db0007] absolute top-0 right-2"></span>
                </button>
                <button type="button" data-nav-tab="tareas" class="phone-tab-btn flex flex-col items-center gap-0.5 hover:text-brand-dark cursor-pointer transition">
                  <i data-lucide="clipboard-check" class="w-4 h-4"></i>
                  <span>Tareas</span>
                </button>
                <button type="button" data-nav-tab="perfil" class="phone-tab-btn flex flex-col items-center gap-0.5 hover:text-brand-dark cursor-pointer transition">
                  <i data-lucide="user" class="w-4 h-4"></i>
                  <span>Perfil</span>
                </button>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ==================== 5. SOCIAL PROOF: METRICS + TESTIMONIALS ==================== -->
  <section id="resultados" class="py-16 sm:py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="text-center mb-12">
      <h2 class="font-display font-black text-3xl sm:text-5xl tracking-tight text-brand-dark">
        <span class="text-gradient-tri">Datos reales</span> que respaldan la solución
      </h2>
    </div>

    <!-- 3 Rounded White Metric Cards -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-14">
      <div class="bg-white rounded-3xl p-7 border border-zinc-200/80 shadow-card relative overflow-hidden">
        <div class="absolute top-0 left-0 right-0 h-2 bg-[#db0007]"></div>
        <div class="font-display font-black text-4xl sm:text-5xl text-[#db0007] mb-3 pt-1">
          50%
        </div>
        <p class="text-sm text-zinc-600 leading-relaxed">
          Revisa siempre su pedido antes de sentarse por malas experiencias previas en cocina tradicional.
        </p>
      </div>

      <div class="bg-white rounded-3xl p-7 border border-zinc-200/80 shadow-card relative overflow-hidden">
        <div class="absolute top-0 left-0 right-0 h-2 bg-[#ffbc0d]"></div>
        <div class="font-display font-black text-4xl sm:text-5xl text-[#ffbc0d] mb-3 pt-1">
          66.7%
        </div>
        <p class="text-sm text-zinc-600 leading-relaxed">
          Considera extremadamente molesto tener que volver a hacer fila en mostrador para solicitar la corrección de un pedido mal armado.
        </p>
      </div>

      <div class="bg-white rounded-3xl p-7 border border-zinc-200/80 shadow-card relative overflow-hidden">
        <div class="absolute top-0 left-0 right-0 h-2 bg-[#27251f]"></div>
        <div class="font-display font-black text-4xl sm:text-5xl text-[#27251f] mb-3 pt-1">
          100%
        </div>
        <p class="text-sm text-zinc-600 leading-relaxed">
          De personal certificado en menos de una jornada mediante un programa técnico que los habilita para gestionar la reposición y supervisión diaria desde el primer día.
        </p>
      </div>
    </div>

    <!-- Testimonials Container Card (#F1F2F4) -->
    <div class="bg-brand-cardGray rounded-[2rem] p-6 sm:p-10">
      <h3 class="font-display font-black text-2xl sm:text-3xl text-center text-brand-dark mb-8">
        Equipos más <span class="text-gradient-tri">tranquilos</span> y clientes más <span class="text-gradient-tri">felices</span>
      </h3>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div class="bg-white rounded-3xl p-6 sm:p-8 shadow-xs border border-zinc-200/60 flex flex-col justify-between">
          <p class="text-sm sm:text-base text-zinc-700 leading-relaxed mb-6">
            “Pensamos que nos iba a costar adaptarnos, pero el equipo le agarró el ritmo en una sola capacitación. Hoy en las horas pico trabajamos mucho más tranquilos y casi no tenemos reclamos en el mostrador.”
          </p>
          <div class="flex items-center gap-3.5 pt-4 border-t border-zinc-100">
            <div class="w-10 h-10 rounded-full bg-[#db0007] text-white font-display font-extrabold text-sm flex items-center justify-center shrink-0">
              S
            </div>
            <div>
              <div class="font-display font-extrabold text-sm text-brand-dark">Sergio</div>
              <div class="text-xs text-zinc-500">Gerente de sucursal</div>
            </div>
          </div>
        </div>

        <div class="bg-white rounded-3xl p-6 sm:p-8 shadow-xs border border-zinc-200/60 flex flex-col justify-between">
          <p class="text-sm sm:text-base text-zinc-700 leading-relaxed mb-6">
            “Cuando salimos en familia lo que más queremos es comer rápido y sin estrés. Poder ver cómo la máquina arma tal cual lo que pedimos nos deja súper tranquilos de que nadie se va a llevar una sorpresa.”
          </p>
          <div class="flex items-center gap-3.5 pt-4 border-t border-zinc-100">
            <div class="w-10 h-10 rounded-full bg-[#ffbc0d] text-brand-dark font-display font-extrabold text-sm flex items-center justify-center shrink-0">
              M
            </div>
            <div>
              <div class="font-display font-extrabold text-sm text-brand-dark">Martín</div>
              <div class="text-xs text-zinc-500">Padre de familia</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ==================== 6. INTERMEDIATE CTA BANNER (Pure White BG) & SHORT FORM GRADIENT ==================== -->
  <section class="pt-14 pb-10 bg-white">
    <div class="max-w-5xl mx-auto px-4 sm:px-6">
      <div class="bg-vertical-tri rounded-[2rem] p-8 sm:p-12 text-white shadow-2xl relative overflow-hidden text-center">
        <div class="max-w-2xl mx-auto space-y-5 relative z-10">
          <h2 class="font-display font-black text-3xl sm:text-4xl lg:text-[2.6rem] leading-tight text-white">
            Sumate a la evolución gastronómica
          </h2>
          <p class="text-sm sm:text-base text-white/95 leading-relaxed">
            Presentación oficial de la estación robótica y apertura de cupos de capacitación técnica para tu equipo.
          </p>
          <div class="pt-2">
            <a href="#formulario-card" class="inline-flex items-center justify-center bg-[#27251f] hover:bg-black text-white font-display font-extrabold text-xs sm:text-sm uppercase tracking-wider px-8 py-4 rounded-full shadow-lg hover:shadow-xl transition transform hover:-translate-y-0.5 active:translate-y-0">
              QUIERO RESERVAR MI LUGAR
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Shorter Gradient Section wrapping ONLY the Form -->
  <section id="registro" class="pt-4 pb-16 bg-form-fade scroll-mt-20">
    <div class="max-w-5xl mx-auto px-4 sm:px-6">
      <div>
        <div id="formulario-card" class="bg-white rounded-3xl p-7 sm:p-12 shadow-2xl border border-zinc-100 max-w-3xl mx-auto">
          <div class="text-center max-w-xl mx-auto mb-8">
            <h2 class="font-display font-black text-2xl sm:text-4xl text-brand-dark leading-tight mb-3">
              Asegurá tu lugar en la presentación y capacitá a tu equipo
            </h2>
            <p class="text-xs sm:text-sm text-zinc-600 leading-relaxed">
              Completá tus datos para reservar acceso a la demostración en vivo de la estación robótica y preinscribir a tu personal en las primeras jornadas de certificación técnica.
            </p>
          </div>

          <form id="reservation-form" novalidate class="space-y-6">
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
              <div>
                <label for="fullName" class="block text-xs font-bold text-brand-dark mb-1.5">
                  Nombre y apellido <span class="text-brand-red">*</span>
                </label>
                <input type="text" id="fullName" name="fullName" required placeholder="Ej. Laura Gómez"
                  class="w-full bg-[#F3F4F6] border border-zinc-200 focus:border-brand-red focus:bg-white rounded-xl px-4 py-3 text-sm text-brand-dark outline-none transition" />
                <p class="error-msg hidden text-[11px] text-brand-red font-medium mt-1">Ingresá tu nombre y apellido.</p>
              </div>

              <div>
                <label for="email" class="block text-xs font-bold text-brand-dark mb-1.5">
                  Correo electrónico <span class="text-brand-red">*</span>
                </label>
                <input type="email" id="email" name="email" required placeholder="laura@tulocal.com"
                  class="w-full bg-[#F3F4F6] border border-zinc-200 focus:border-brand-red focus:bg-white rounded-xl px-4 py-3 text-sm text-brand-dark outline-none transition" />
                <p class="error-msg hidden text-[11px] text-brand-red font-medium mt-1">Ingresá un correo electrónico válido.</p>
              </div>

              <div>
                <label for="phone" class="block text-xs font-bold text-brand-dark mb-1.5">
                  Número de contacto <span class="text-brand-red">*</span>
                </label>
                <input type="tel" id="phone" name="phone" required placeholder="+54 9 11 5555-0199"
                  class="w-full bg-[#F3F4F6] border border-zinc-200 focus:border-brand-red focus:bg-white rounded-xl px-4 py-3 text-sm text-brand-dark outline-none transition" />
                <p class="error-msg hidden text-[11px] text-brand-red font-medium mt-1">Ingresá un número de contacto válido.</p>
              </div>

              <div>
                <label for="staffCount" class="block text-xs font-bold text-brand-dark mb-1.5">
                  Cantidad de empleados a capacitar (estimado) <span class="text-brand-red">*</span>
                </label>
                <input type="number" id="staffCount" name="staffCount" min="1" max="500" required placeholder="Ej. 8"
                  class="w-full bg-[#F3F4F6] border border-zinc-200 focus:border-brand-red focus:bg-white rounded-xl px-4 py-3 text-sm text-brand-dark outline-none transition" />
                <p class="error-msg hidden text-[11px] text-brand-red font-medium mt-1">Indicá una cantidad válida (mínimo 1).</p>
              </div>
            </div>

            <div>
              <label class="block text-xs font-bold text-brand-dark mb-2.5">
                Modalidad de interés <span class="text-brand-red">*</span>
              </label>

              <div class="space-y-2.5" id="modality-options">
                <label class="modality-card flex items-center gap-3.5 p-3.5 rounded-2xl border-2 border-zinc-200 bg-[#F3F4F6] hover:border-brand-yellow cursor-pointer transition">
                  <input type="radio" name="modality" value="Asistir a la presentación oficial (Demostración en vivo)" class="w-4 h-4 accent-brand-red" checked />
                  <span class="text-xs sm:text-sm font-semibold text-brand-dark">Asistir a la presentación oficial (Demostración en vivo)</span>
                </label>

                <label class="modality-card flex items-center gap-3.5 p-3.5 rounded-2xl border-2 border-zinc-200 bg-[#F3F4F6] hover:border-brand-yellow cursor-pointer transition">
                  <input type="radio" name="modality" value="Inscribir equipo a capacitación técnica y certificación" class="w-4 h-4 accent-brand-red" />
                  <span class="text-xs sm:text-sm font-semibold text-brand-dark">Inscribir equipo a capacitación técnica y certificación</span>
                </label>

                <label class="modality-card flex items-center gap-3.5 p-3.5 rounded-2xl border-2 border-zinc-200 bg-[#F3F4F6] hover:border-brand-yellow cursor-pointer transition">
                  <input type="radio" name="modality" value="Ambas instancias (Presentación + Capacitación)" class="w-4 h-4 accent-brand-red" />
                  <span class="text-xs sm:text-sm font-semibold text-brand-dark">Ambas instancias (Presentación + Capacitación)</span>
                </label>
              </div>
            </div>

            <div class="pt-2">
              <button type="submit"
                class="w-full bg-[#db0007] hover:bg-brand-redDark text-white font-display font-extrabold text-xs sm:text-sm uppercase tracking-wider py-4 px-6 rounded-full shadow-lg hover:shadow-xl transition transform hover:-translate-y-0.5 active:translate-y-0 cursor-pointer">
                RESERVAR MI LUGAR EN LA PRESENTACIÓN Y CAPACITACIÓN
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>

  <!-- ==================== 7. FOOTER ==================== -->
  <footer class="bg-brand-dark text-white py-10 px-4 sm:px-6 lg:px-8 border-t border-white/10">
    <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6">
      <div class="flex items-center gap-3.5">
        <svg class="w-10 h-8 shrink-0" viewBox="0 0 100 80" fill="none">
          <path d="M12 72C12 36 22 10 33 10C44 10 47 38 47 68H53C53 38 56 10 67 10C78 10 88 36 88 72" stroke="#ffbc0d" stroke-width="11" stroke-linecap="round"/>
        </svg>
        <span class="font-display font-extrabold text-xs sm:text-sm tracking-wider uppercase text-white">
          ARGENTINA | ESTACIÓN ROBÓTICA
        </span>
      </div>

      <div class="text-center md:text-right space-y-2">
        <p class="font-display font-bold text-xs tracking-wider uppercase text-brand-yellow">
          PRESENTACIÓN OFICIAL & PROGRAMA DE CERTIFICACIÓN TÉCNICA · CUPOS LIMITADOS
        </p>
        <div class="flex flex-wrap items-center justify-center md:justify-end gap-5 text-xs text-white/60">
          <a href="#beneficios" class="hover:text-brand-yellow transition">Beneficios</a>
          <a href="#app-gestion" class="hover:text-brand-yellow transition">App de gestión</a>
          <a href="#resultados" class="hover:text-brand-yellow transition">Resultados</a>
          <a href="#registro" class="hover:text-brand-yellow transition">Reservar lugar</a>
        </div>
      </div>
    </div>
  </footer>

  <!-- ==================== OFFICIAL CONFIRMATION MODAL ==================== -->
  <div id="confirmation-modal" class="fixed inset-0 z-50 hidden items-center justify-center p-4 bg-black/70 backdrop-blur-xs">
    <div class="bg-white rounded-3xl max-w-md w-full p-7 sm:p-8 shadow-2xl text-center relative">
      <button id="close-modal-btn" aria-label="Cerrar confirmación" class="absolute top-4 right-4 p-2 rounded-full bg-zinc-100 hover:bg-zinc-200 text-zinc-600 transition cursor-pointer">
        <i data-lucide="x" class="w-4 h-4"></i>
      </button>

      <div class="w-16 h-16 rounded-full bg-emerald-100 text-emerald-600 flex items-center justify-center mx-auto mb-4">
        <i data-lucide="check-circle-2" class="w-9 h-9"></i>
      </div>

      <span class="inline-block bg-brand-yellow text-brand-dark font-display font-extrabold text-[11px] uppercase tracking-wider px-3 py-1 rounded-full mb-2">
        Pase Oficial Generado
      </span>

      <h3 class="font-display font-black text-2xl text-brand-dark mb-2">
        ¡Tu lugar está reservado!
      </h3>

      <p class="text-xs sm:text-sm text-zinc-600 mb-5" id="modal-summary-text">
        Enviamos el pase de acceso y el cronograma técnico a tu correo.
      </p>

      <div class="bg-[#F3F4F6] border border-dashed border-zinc-300 rounded-2xl p-4 text-left space-y-2.5 mb-6">
        <div class="flex items-center justify-between border-b border-zinc-200 pb-2.5">
          <div>
            <span class="block text-[10px] font-bold uppercase text-zinc-400">Código de acceso</span>
            <span id="ticket-code" class="font-mono font-extrabold text-sm text-brand-dark bg-brand-yellow px-2.5 py-0.5 rounded inline-block mt-0.5">MCD-2026-884</span>
          </div>
          <svg class="w-12 h-12 bg-white p-1 rounded-lg border border-zinc-200 shrink-0" viewBox="0 0 40 40" fill="none">
            <rect x="4" y="4" width="10" height="10" stroke="#27251f" stroke-width="2.5"/>
            <rect x="7.5" y="7.5" width="3" height="3" fill="#27251f"/>
            <rect x="26" y="4" width="10" height="10" stroke="#27251f" stroke-width="2.5"/>
            <rect x="29.5" y="7.5" width="3" height="3" fill="#27251f"/>
            <rect x="4" y="26" width="10" height="10" stroke="#27251f" stroke-width="2.5"/>
            <rect x="7.5" y="29.5" width="3" height="3" fill="#27251f"/>
            <rect x="18" y="6" width="4" height="4" fill="#db0007"/>
            <rect x="18" y="14" width="4" height="8" fill="#27251f"/>
            <rect x="6" y="18" width="8" height="4" fill="#27251f"/>
            <rect x="26" y="18" width="10" height="4" fill="#27251f"/>
            <rect x="18" y="26" width="6" height="10" fill="#27251f"/>
            <rect x="28" y="26" width="8" height="8" fill="#db0007"/>
          </svg>
        </div>

        <div class="flex justify-between text-xs">
          <span class="text-zinc-500">Titular:</span>
          <span class="font-bold text-brand-dark" id="ticket-name">-</span>
        </div>
        <div class="flex justify-between text-xs">
          <span class="text-zinc-500">Equipo a capacitar:</span>
          <span class="font-bold text-brand-dark" id="ticket-staff">-</span>
        </div>
        <div class="flex justify-between text-xs">
          <span class="text-zinc-500">Modalidad:</span>
          <span class="font-bold text-brand-red text-right max-w-[190px]" id="ticket-modality">-</span>
        </div>
      </div>

      <div class="flex gap-3">
        <button id="copy-code-btn" type="button" class="flex-1 bg-zinc-100 hover:bg-zinc-200 text-brand-dark font-display font-bold text-xs py-3 rounded-full transition cursor-pointer">
          Copiar pase
        </button>
        <button id="done-modal-btn" type="button" class="flex-1 bg-[#db0007] hover:bg-brand-redDark text-white font-display font-extrabold text-xs py-3 rounded-full transition cursor-pointer">
          Listo
        </button>
      </div>
    </div>
  </div>

  <!-- ==================== INTERACTIVE JAVASCRIPT ==================== -->
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      if (window.lucide) {
        lucide.createIcons();
      }

      /* ---------------------------------------------------------
         MOBILE APP SIMULATOR (SINGLE PHONE WITH HOME & FLOWS)
      --------------------------------------------------------- */
      let alertThreshold = 30; // 30% Valle or 50% Pico
      let currentScreen = 'inicio'; // 'inicio' | 'maquinas' | 'detalle' | 'instrucciones' | 'proceso' | 'completada' | 'error' | 'tareas' | 'perfil'
      let activeMachineId = 1;
      let currentKg = 3.2;
      const targetKg = 5.0;
      let assistanceSent = false;
      let sensorChecking = false;

      const shiftTasks = [
        { id: 1, title: 'Calibración de balanzas', time: '08:00', done: true },
        { id: 2, title: 'Reponer Queso cheddar (M1)', time: '12:30', done: false },
        { id: 3, title: 'Sanitización de tolvas', time: '15:00', done: false },
        { id: 4, title: 'Control de temperatura', time: '16:00', done: true }
      ];

      function getInitialMachines() {
        return [
          {
            id: 1,
            name: 'Máquina 1',
            ingredients: [
              { name: 'Pan', pct: 85, emoji: '🍔' },
              { name: 'Carne', pct: 78, emoji: '🥩' },
              { name: 'Queso', pct: 30, emoji: '🧀' },
              { name: 'Lechuga', pct: 90, emoji: '🥬' },
              { name: 'Tomate', pct: 88, emoji: '🍅' },
              { name: 'Cebolla', pct: 80, emoji: '🧅' }
            ]
          },
          {
            id: 2,
            name: 'Máquina 2',
            ingredients: [
              { name: 'Pan', pct: 92, emoji: '🍔' },
              { name: 'Carne', pct: 84, emoji: '🥩' },
              { name: 'Queso', pct: 89, emoji: '🧀' },
              { name: 'Lechuga', pct: 95, emoji: '🥬' },
              { name: 'Tomate', pct: 91, emoji: '🍅' },
              { name: 'Cebolla', pct: 87, emoji: '🧅' }
            ]
          },
          {
            id: 3,
            name: 'Máquina 3',
            ingredients: [
              { name: 'Pan', pct: 76, emoji: '🍔' },
              { name: 'Carne', pct: 81, emoji: '🥩' },
              { name: 'Queso', pct: 74, emoji: '🧀' },
              { name: 'Lechuga', pct: 88, emoji: '🥬' },
              { name: 'Tomate', pct: 82, emoji: '🍅' },
              { name: 'Cebolla', pct: 79, emoji: '🧅' }
            ]
          },
          {
            id: 4,
            name: 'Máquina 4',
            ingredients: [
              { name: 'Pan', pct: 94, emoji: '🍔' },
              { name: 'Carne', pct: 90, emoji: '🥩' },
              { name: 'Queso', pct: 85, emoji: '🧀' },
              { name: 'Lechuga', pct: 92, emoji: '🥬' },
              { name: 'Tomate', pct: 90, emoji: '🍅' },
              { name: 'Cebolla', pct: 86, emoji: '🧅' }
            ]
          }
        ];
      }

      let machinesState = getInitialMachines();
      const phoneViewport = document.getElementById('phone-main-viewport');

      function getLowIngredient(machine) {
        return machine.ingredients.find(i => i.pct <= alertThreshold);
      }

      function renderRedHeader(showBack = false, backTarget = 'inicio', rightIcon = 'bell') {
        const anyLow = machinesState.some(m => Boolean(getLowIngredient(m)));
        return `
          <div class="bg-[#db0007] text-white pt-7 pb-3.5 px-4 shrink-0">
            <div class="flex items-center justify-between text-[10px] font-semibold opacity-90 mb-2">
              <span>9:41</span>
              <span>5G · 100%</span>
            </div>
            <div class="flex items-center justify-between">
              ${showBack
                ? `<button type="button" data-go="${backTarget}" class="app-go-btn p-1 -ml-1 rounded-full hover:bg-white/15 cursor-pointer transition" title="Volver">
                     <i data-lucide="chevron-left" class="w-4 h-4"></i>
                   </button>`
                : `<span class="w-5"></span>`
              }
              <svg class="w-7 h-5" viewBox="0 0 100 80" fill="none">
                <path d="M12 72C12 36 22 10 33 10C44 10 47 38 47 68H53C53 38 56 10 67 10C78 10 88 36 88 72" stroke="#ffbc0d" stroke-width="12" stroke-linecap="round"/>
              </svg>
              ${rightIcon === 'sensor'
                ? `<button type="button" data-go="error" class="app-go-btn p-1 -mr-1 rounded-full hover:bg-white/15 cursor-pointer transition" title="Estado de sensor">
                     <i data-lucide="alert-triangle" class="w-4 h-4 text-[#ffbc0d]"></i>
                   </button>`
                : `<button type="button" data-go="maquinas" class="app-go-btn relative p-1 -mr-1 rounded-full hover:bg-white/15 cursor-pointer transition" title="Ver alertas">
                     <i data-lucide="bell" class="w-4 h-4 text-white"></i>
                     ${anyLow ? `<span class="w-2 h-2 bg-[#ffbc0d] rounded-full absolute top-0.5 right-0.5"></span>` : ''}
                   </button>`
              }
            </div>
          </div>
        `;
      }

      function renderWhiteSubHeader(title, backTarget) {
        return `
          <div class="bg-white text-brand-dark pt-7 pb-3 px-4 border-b border-zinc-100 shrink-0">
            <div class="flex items-center justify-between text-[10px] font-semibold text-zinc-500 mb-2">
              <span>9:41</span>
              <span>5G · 100%</span>
            </div>
            <div class="flex items-center justify-between">
              <button type="button" data-go="${backTarget}" class="app-go-btn p-1 -ml-1 hover:bg-zinc-100 rounded-full cursor-pointer transition">
                <i data-lucide="chevron-left" class="w-4 h-4"></i>
              </button>
              <span class="font-display font-extrabold text-xs">${title}</span>
              <span class="w-5"></span>
            </div>
          </div>
        `;
      }

      function updateNavIndicators() {
        const pillMap = {
          inicio: 'inicio',
          maquinas: 'maquinas',
          detalle: 'detalle',
          instrucciones: 'instrucciones',
          proceso: 'proceso',
          completada: 'proceso',
          error: 'error',
          tareas: 'inicio',
          perfil: 'inicio'
        };
        const activePill = pillMap[currentScreen] || 'inicio';

        document.querySelectorAll('.screen-nav-pill').forEach(pill => {
          if (pill.dataset.screen === activePill) {
            pill.className = 'screen-nav-pill text-[11px] font-display font-extrabold px-3 py-1.5 rounded-full transition cursor-pointer bg-[#db0007] text-white shadow-xs';
          } else {
            pill.className = 'screen-nav-pill text-[11px] font-display font-extrabold px-3 py-1.5 rounded-full transition cursor-pointer bg-zinc-100 hover:bg-zinc-200 text-brand-dark';
          }
        });

        const tabMap = {
          inicio: 'inicio',
          maquinas: 'maquinas',
          detalle: 'maquinas',
          instrucciones: 'maquinas',
          proceso: 'maquinas',
          completada: 'maquinas',
          error: 'maquinas',
          tareas: 'tareas',
          perfil: 'perfil'
        };
        const activeTab = tabMap[currentScreen] || 'inicio';

        document.querySelectorAll('.phone-tab-btn').forEach(btn => {
          if (btn.dataset.navTab === activeTab) {
            btn.className = 'phone-tab-btn flex flex-col items-center gap-0.5 text-[#db0007] font-bold cursor-pointer transition relative';
          } else {
            btn.className = 'phone-tab-btn flex flex-col items-center gap-0.5 text-zinc-400 hover:text-brand-dark cursor-pointer transition relative';
          }
        });

        const anyLow = machinesState.some(m => Boolean(getLowIngredient(m)));
        const badge = document.getElementById('tab-alert-badge');
        if (badge) badge.style.display = anyLow ? 'block' : 'none';
      }

      function renderPhoneApp(animate = true) {
        const currentMachine = machinesState.find(m => m.id === activeMachineId) || machinesState[0];
        const lowItem = getLowIngredient(currentMachine);
        const targetIngredient = lowItem || currentMachine.ingredients.find(i => i.name === 'Queso');
        const ingredientLabel = targetIngredient.name === 'Queso' ? 'Queso cheddar' : targetIngredient.name;
        const animClass = animate ? 'animate-phone-screen' : '';

        const totalMachines = machinesState.length;
        const machinesOkCount = machinesState.filter(m => !getLowIngredient(m)).length;
        const pendingTasksCount = shiftTasks.filter(t => !t.done).length;
        const firstAlertMachine = machinesState.find(m => Boolean(getLowIngredient(m)));
        const firstAlertItem = firstAlertMachine ? getLowIngredient(firstAlertMachine) : null;

        /* PANTALLA DE INICIO (HOME) */
        if (currentScreen === 'inicio') {
          phoneViewport.innerHTML = `
            ${renderRedHeader(false, 'inicio', 'bell')}
            <div class="${animClass} p-4 flex-1 overflow-y-auto space-y-3">
              <div class="flex items-center justify-between">
                <div>
                  <p class="text-[10px] font-semibold text-zinc-500">Turno Activo · Local #014</p>
                  <h4 class="font-display font-black text-base text-brand-dark">Panel de Inicio</h4>
                </div>
                <span class="bg-brand-dark text-[#ffbc0d] font-display font-extrabold text-[10px] px-2.5 py-1 rounded-full">
                  Umbral ${alertThreshold}%
                </span>
              </div>

              <div class="grid grid-cols-2 gap-2.5">
                <button type="button" data-go="maquinas" class="app-go-btn bg-white p-3 rounded-2xl border border-zinc-200 text-left hover:border-[#ffbc0d] transition cursor-pointer shadow-2xs">
                  <div class="text-[10px] font-semibold text-zinc-500">Estaciones OK</div>
                  <div class="font-display font-black text-xl text-brand-dark mt-0.5">${machinesOkCount}<span class="text-xs font-bold text-zinc-400">/${totalMachines}</span></div>
                  <div class="text-[10px] font-bold text-emerald-600 mt-1">Ver estaciones →</div>
                </button>

                <button type="button" data-go="tareas" class="app-go-btn bg-white p-3 rounded-2xl border border-zinc-200 text-left hover:border-[#ffbc0d] transition cursor-pointer shadow-2xs">
                  <div class="text-[10px] font-semibold text-zinc-500">Tareas pendientes</div>
                  <div class="font-display font-black text-xl text-brand-dark mt-0.5">${pendingTasksCount}</div>
                  <div class="text-[10px] font-bold text-[#db0007] mt-1">Abrir checklist →</div>
                </button>
              </div>

              ${firstAlertMachine ? `
                <div class="bg-[#ffbc0d]/25 border-2 border-[#ffbc0d] rounded-2xl p-3">
                  <div class="flex items-center justify-between mb-1.5">
                    <span class="bg-[#db0007] text-white font-display font-extrabold text-[9px] uppercase px-2 py-0.5 rounded-full">
                      Alerta Activa
                    </span>
                    <span class="text-[10px] font-bold text-brand-dark">${firstAlertMachine.name}</span>
                  </div>
                  <p class="font-display font-extrabold text-xs text-brand-dark">
                    ${firstAlertItem.name === 'Queso' ? 'Queso cheddar' : firstAlertItem.name} al ${firstAlertItem.pct}%
                  </p>
                  <p class="text-[10px] text-zinc-700 mt-0.5 mb-2.5">
                    Requiere reposición para mantener el flujo sin cortes.
                  </p>
                  <button type="button" id="home-resolve-alert-btn" class="w-full bg-[#db0007] hover:bg-brand-redDark text-white font-display font-extrabold text-[11px] py-2 rounded-full transition cursor-pointer">
                    Reponer ahora
                  </button>
                </div>
              ` : `
                <div class="bg-emerald-50 border border-emerald-200 rounded-2xl p-3 flex items-center gap-2.5">
                  <div class="w-8 h-8 rounded-xl bg-emerald-600 text-white flex items-center justify-center shrink-0">
                    <i data-lucide="check" class="w-4 h-4"></i>
                  </div>
                  <div>
                    <p class="font-display font-extrabold text-xs text-emerald-900">Operación al 100%</p>
                    <p class="text-[10px] text-emerald-700">Todas las bandejas están abastecidas.</p>
                  </div>
                </div>
              `}

              <div>
                <div class="font-display font-extrabold text-[11px] text-zinc-500 uppercase tracking-wider mb-2">
                  Accesos rápidos
                </div>
                <div class="space-y-2">
                  <button type="button" data-go="maquinas" class="app-go-btn w-full bg-white hover:bg-zinc-50 border border-zinc-200 rounded-xl p-2.5 flex items-center justify-between transition cursor-pointer">
                    <div class="flex items-center gap-2.5">
                      <span class="w-7 h-7 rounded-lg bg-brand-dark text-[#ffbc0d] flex items-center justify-center text-xs font-black">M1</span>
                      <span class="font-display font-bold text-xs text-brand-dark">Monitor de stock en vivo</span>
                    </div>
                    <i data-lucide="chevron-right" class="w-4 h-4 text-zinc-400"></i>
                  </button>

                  <button type="button" data-go="error" class="app-go-btn w-full bg-white hover:bg-zinc-50 border border-zinc-200 rounded-xl p-2.5 flex items-center justify-between transition cursor-pointer">
                    <div class="flex items-center gap-2.5">
                      <span class="w-7 h-7 rounded-lg bg-red-50 text-[#db0007] flex items-center justify-center">
                        <i data-lucide="activity" class="w-3.5 h-3.5"></i>
                      </span>
                      <span class="font-display font-bold text-xs text-brand-dark">Diagnóstico de balanzas</span>
                    </div>
                    <i data-lucide="chevron-right" class="w-4 h-4 text-zinc-400"></i>
                  </button>
                </div>
              </div>
            </div>
          `;

          const resolveBtn = document.getElementById('home-resolve-alert-btn');
          if (resolveBtn && firstAlertMachine) {
            resolveBtn.addEventListener('click', () => {
              activeMachineId = firstAlertMachine.id;
              currentScreen = 'instrucciones';
              renderPhoneApp(true);
            });
          }
        }

        /* MÁQUINAS */
        else if (currentScreen === 'maquinas') {
          phoneViewport.innerHTML = `
            ${renderRedHeader(true, 'inicio', 'bell')}
            <div class="${animClass} p-4 flex-1 overflow-y-auto">
              <h4 class="font-display font-extrabold text-base text-center text-brand-dark mb-3">Máquinas</h4>
              <div class="space-y-2.5">
                ${machinesState.map(m => {
                  const mLow = getLowIngredient(m);
                  const cardClasses = mLow
                    ? 'border-2 border-[#ffbc0d] bg-[#ffbc0d]/25 shadow-xs'
                    : 'border border-zinc-200 bg-white';

                  return `
                    <button type="button" data-machine-id="${m.id}"
                      class="machine-select-btn w-full text-left p-3 rounded-2xl ${cardClasses} flex items-center justify-between transition transform active:scale-[0.98] cursor-pointer hover:shadow-xs">
                      <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-xl bg-brand-dark text-[#ffbc0d] flex items-center justify-center font-display font-black text-xs shrink-0">
                          M${m.id}
                        </div>
                        <div>
                          <div class="font-display font-extrabold text-xs text-brand-dark">${m.name}</div>
                          <div class="text-[11px] font-semibold ${mLow ? 'text-[#db0007]' : 'text-zinc-500'}">
                            ${mLow ? `${mLow.name} al ${mLow.pct}%` : 'Stock OK'}
                          </div>
                        </div>
                      </div>
                      <div class="flex items-center gap-1.5">
                        ${mLow
                          ? `<span class="w-5 h-5 rounded-full bg-[#db0007] text-white text-[10px] font-black flex items-center justify-center">1</span>
                             <span class="text-xs font-bold text-brand-dark">→</span>`
                          : `<span class="w-5 h-5 rounded-full bg-emerald-500 text-white text-[10px] font-black flex items-center justify-center">✓</span>`
                        }
                      </div>
                    </button>
                  `;
                }).join('')}
              </div>
            </div>
          `;

          document.querySelectorAll('.machine-select-btn').forEach(btn => {
            btn.addEventListener('click', () => {
              activeMachineId = Number(btn.dataset.machineId);
              currentScreen = 'detalle';
              renderPhoneApp(true);
            });
          });
        }

        /* DETALLE DE INGREDIENTES */
        else if (currentScreen === 'detalle') {
          phoneViewport.innerHTML = `
            ${renderRedHeader(true, 'maquinas', 'sensor')}
            <div class="${animClass} flex-1 flex flex-col justify-between overflow-hidden bg-white">
              <div class="p-4 overflow-y-auto">
                <div class="text-center font-display font-extrabold text-sm text-brand-dark mb-2.5">${currentMachine.name}</div>

                ${lowItem ? `
                  <button type="button" data-go="instrucciones" class="app-go-btn w-full text-left rounded-2xl p-2.5 mb-3 flex items-center gap-2.5 bg-red-50 hover:bg-red-100/80 border border-red-200 transition cursor-pointer">
                    <div class="w-8 h-8 rounded-xl bg-[#db0007] text-white flex items-center justify-center shrink-0">
                      <i data-lucide="alert-triangle" class="w-4 h-4"></i>
                    </div>
                    <div class="flex-1">
                      <p class="font-display font-extrabold text-xs text-brand-dark leading-tight">
                        ${ingredientLabel} al ${lowItem.pct}%
                      </p>
                      <p class="text-[10px] text-zinc-600 mt-0.5">Se requiere reposición</p>
                    </div>
                  </button>
                ` : `
                  <div class="rounded-2xl p-2.5 mb-3 flex items-center gap-2.5 bg-emerald-50 border border-emerald-200">
                    <div class="w-8 h-8 rounded-xl bg-emerald-600 text-white flex items-center justify-center shrink-0">
                      <i data-lucide="check" class="w-4 h-4"></i>
                    </div>
                    <div>
                      <p class="font-display font-extrabold text-xs text-emerald-800 leading-tight">
                        Stock completo al 100%
                      </p>
                      <p class="text-[10px] text-emerald-700 mt-0.5">Todas las bandejas listas</p>
                    </div>
                  </div>
                `}

                <div class="flex items-center justify-between mb-2">
                  <span class="font-display font-extrabold text-xs text-brand-dark">Ingredientes</span>
                  <span class="text-[9px] font-semibold text-zinc-400">Tocá un insumo</span>
                </div>

                <div class="space-y-1.5">
                  ${currentMachine.ingredients.map(ing => {
                    const isLow = ing.pct <= alertThreshold;
                    const barColor = isLow ? 'bg-[#db0007]' : 'bg-emerald-500';
                    const pctColor = isLow ? 'text-[#db0007] font-extrabold' : 'text-brand-dark font-bold';
                    return `
                      <button type="button" data-go="instrucciones" class="app-go-btn w-full text-left flex items-center gap-2 p-1 rounded-lg hover:bg-zinc-50 transition cursor-pointer">
                        <span class="text-sm w-5 text-center">${ing.emoji}</span>
                        <div class="flex-1">
                          <div class="flex justify-between text-[11px] mb-0.5">
                            <span class="font-medium text-brand-dark">${ing.name}</span>
                            <span class="${pctColor}">${ing.pct}%</span>
                          </div>
                          <div class="w-full h-1.5 bg-zinc-100 rounded-full overflow-hidden">
                            <div class="h-full ${barColor} rounded-full transition-all duration-500" style="width: ${ing.pct}%"></div>
                          </div>
                        </div>
                      </button>
                    `;
                  }).join('')}
                </div>
              </div>

              <div class="p-3.5 bg-zinc-50 border-t border-zinc-100 shrink-0">
                <button type="button" data-go="instrucciones" class="app-go-btn w-full bg-[#ffbc0d] hover:bg-brand-yellowLight text-brand-dark font-display font-extrabold text-xs py-2.5 rounded-full shadow-sm transition transform active:scale-95 cursor-pointer">
                  Ver detalle
                </button>
              </div>
            </div>
          `;
        }

        /* INSTRUCCIONES DE REPOSICIÓN */
        else if (currentScreen === 'instrucciones') {
          phoneViewport.innerHTML = `
            ${renderWhiteSubHeader('Reposición requerida', 'detalle')}
            <div class="${animClass} flex-1 flex flex-col justify-between bg-white">
              <div class="p-4 text-center">
                <div class="w-16 h-14 mx-auto mb-2 flex items-center justify-center animate-pulse-soft">
                  <svg class="w-14 h-12" viewBox="0 0 64 52" fill="none">
                    <polygon points="32,8 56,20 32,32 8,20" fill="#ffbc0d"/>
                    <polygon points="32,16 56,28 32,40 8,28" fill="#f19f00" fill-opacity="0.85"/>
                    <polygon points="32,23 56,35 32,47 8,35" fill="#ffbc0d"/>
                  </svg>
                </div>

                <h4 class="font-display font-black text-base text-brand-dark mb-3">${ingredientLabel}</h4>

                <div class="bg-[#F3F4F6] rounded-2xl p-2.5 flex items-center gap-2.5 text-left mb-4">
                  <div class="w-8 h-8 rounded-lg bg-brand-dark text-[#ffbc0d] font-display font-black text-[11px] flex items-center justify-center shrink-0">
                    M${currentMachine.id}
                  </div>
                  <div>
                    <div class="font-display font-extrabold text-xs text-brand-dark">${currentMachine.name}</div>
                    <div class="text-[10px] text-zinc-500">Stock actual: ${targetIngredient.pct}%</div>
                  </div>
                </div>

                <div class="text-left space-y-2.5">
                  <div class="font-display font-extrabold text-xs text-brand-dark">Pasos:</div>
                  <div class="flex items-start gap-2.5">
                    <span class="w-4 h-4 rounded-full bg-[#db0007] text-white font-display font-extrabold text-[10px] flex items-center justify-center shrink-0 mt-0.5">1</span>
                    <p class="text-[11px] text-zinc-600 leading-snug">Acercate al depósito de ${targetIngredient.name.toLowerCase()}.</p>
                  </div>
                  <div class="flex items-start gap-2.5">
                    <span class="w-4 h-4 rounded-full bg-[#db0007] text-white font-display font-extrabold text-[10px] flex items-center justify-center shrink-0 mt-0.5">2</span>
                    <p class="text-[11px] text-zinc-600 leading-snug">Agregá la cantidad necesaria (hasta completar el peso objetivo).</p>
                  </div>
                </div>
              </div>

              <div class="p-3.5 space-y-2 bg-zinc-50 border-t border-zinc-100 shrink-0">
                <button type="button" id="start-restock-btn" class="w-full bg-[#ffbc0d] hover:bg-brand-yellowLight text-brand-dark font-display font-extrabold text-xs py-2.5 rounded-full shadow-sm transition transform active:scale-95 cursor-pointer">
                  Comenzar reposición
                </button>
                <button type="button" data-go="detalle" class="app-go-btn w-full bg-white hover:bg-zinc-100 text-brand-dark border border-zinc-200 font-display font-bold text-xs py-2 rounded-full transition cursor-pointer">
                  Posponer
                </button>
              </div>
            </div>
          `;

          document.getElementById('start-restock-btn').addEventListener('click', () => {
            currentKg = 3.2;
            currentScreen = 'proceso';
            renderPhoneApp(true);
          });
        }

        /* REPOSICIÓN EN PROCESO (BALANZA EN VIVO) */
        else if (currentScreen === 'proceso') {
          const progressPct = Math.min(100, Math.round((currentKg / targetKg) * 100));
          const circumference = 2 * Math.PI * 44;
          const dashOffset = circumference - (progressPct / 100) * circumference;

          phoneViewport.innerHTML = `
            ${renderWhiteSubHeader('Reposición en proceso', 'instrucciones')}
            <div class="${animClass} flex-1 flex flex-col justify-between bg-white">
              <div class="p-4 text-center flex flex-col items-center">
                <div class="relative w-32 h-32 my-2 flex items-center justify-center">
                  <svg class="w-32 h-32 -rotate-90" viewBox="0 0 100 100">
                    <circle cx="50" cy="50" r="44" stroke="#E5E7EB" stroke-width="9" fill="none"/>
                    <circle cx="50" cy="50" r="44" stroke="#ffbc0d" stroke-width="9" fill="none"
                      stroke-linecap="round"
                      stroke-dasharray="${circumference}"
                      stroke-dashoffset="${dashOffset}"
                      class="transition-all duration-500"/>
                  </svg>
                  <div class="absolute inset-0 flex flex-col items-center justify-center">
                    <span class="font-display font-black text-lg text-brand-dark leading-none">${currentKg.toFixed(1)} kg</span>
                    <span class="font-display font-bold text-xs text-zinc-500 mt-1">/ 5 kg</span>
                  </div>
                </div>

                <p class="text-xs font-semibold text-zinc-700 mb-2.5">
                  ${currentKg >= targetKg ? '¡Peso objetivo alcanzado!' : 'Agregá más queso...'}
                </p>

                <div class="w-full h-2.5 bg-zinc-200 rounded-full overflow-hidden mb-3">
                  <div class="h-full bg-[#ffbc0d] rounded-full transition-all duration-500" style="width: ${progressPct}%"></div>
                </div>

                <div class="w-full bg-indigo-50 border border-indigo-100 rounded-xl py-2 px-3 flex items-center justify-center gap-2 text-xs font-bold text-brand-dark">
                  <span class="w-4 h-4 rounded-full bg-indigo-600 text-white text-[10px] flex items-center justify-center font-black">i</span>
                  <span>Peso objetivo: 5 kg</span>
                </div>
              </div>

              <div class="p-3.5 bg-zinc-50 border-t border-zinc-100 shrink-0">
                <button type="button" id="add-weight-btn" class="w-full bg-[#ffbc0d] hover:bg-brand-yellowLight text-brand-dark font-display font-extrabold text-xs py-2.5 rounded-full shadow-sm transition transform active:scale-95 cursor-pointer">
                  + Agregar carga (+0.6 kg)
                </button>
              </div>
            </div>
          `;

          document.getElementById('add-weight-btn').addEventListener('click', () => {
            currentKg = Math.min(5.0, Number((currentKg + 0.6).toFixed(1)));
            if (currentKg >= 5.0) {
              const m = machinesState.find(item => item.id === activeMachineId);
              const low = getLowIngredient(m) || m.ingredients.find(i => i.name === 'Queso');
              if (low) low.pct = 100;
              const task = shiftTasks.find(t => t.id === 2);
              if (task) task.done = true;

              renderPhoneApp(false);
              setTimeout(() => {
                currentScreen = 'completada';
                renderPhoneApp(true);
              }, 380);
            } else {
              renderPhoneApp(false);
            }
          });
        }

        /* REPOSICIÓN COMPLETADA (LIMPIA - SIN PALITOS AMARILLOS) */
        else if (currentScreen === 'completada') {
          phoneViewport.innerHTML = `
            <div class="${animClass} flex-1 flex flex-col justify-between bg-white">
              <div class="pt-7 px-4">
                <div class="flex items-center justify-between text-[10px] font-semibold text-zinc-500">
                  <span>9:41</span>
                  <span>5G · 100%</span>
                </div>
              </div>

              <div class="px-5 text-center flex flex-col items-center justify-center flex-1">
                <div class="mb-5">
                  <div class="w-20 h-20 rounded-full bg-emerald-500 text-white flex items-center justify-center shadow-lg">
                    <i data-lucide="check" class="w-11 h-11 stroke-[3]"></i>
                  </div>
                </div>

                <h4 class="font-display font-black text-xl text-brand-dark leading-tight mb-2">
                  ¡Reposición<br/>completada!
                </h4>
                <p class="text-xs text-zinc-600">${ingredientLabel}</p>
                <p class="font-display font-extrabold text-sm text-brand-dark mt-0.5">5.0 kg</p>
              </div>

              <div class="p-3.5 bg-zinc-50 border-t border-zinc-100 shrink-0">
                <button type="button" id="finish-restock-btn" class="w-full bg-[#ffbc0d] hover:bg-brand-yellowLight text-brand-dark font-display font-extrabold text-xs py-2.5 rounded-full shadow-sm transition transform active:scale-95 cursor-pointer">
                  Volver al inicio
                </button>
              </div>
            </div>
          `;

          document.getElementById('finish-restock-btn').addEventListener('click', () => {
            const m = machinesState.find(item => item.id === activeMachineId);
            m.ingredients.forEach(i => { if (i.pct < 100 && i.name === 'Queso') i.pct = 100; });
            currentScreen = 'inicio';
            renderPhoneApp(true);
          });
        }

        /* ESTADO DE FALLA - ERROR DE SENSOR */
        else if (currentScreen === 'error') {
          phoneViewport.innerHTML = `
            <div class="${animClass} flex-1 flex flex-col justify-between bg-white">
              <div class="pt-7 px-4">
                <div class="flex items-center justify-between text-[10px] font-semibold text-zinc-500">
                  <span>9:41</span>
                  <span>5G · 100%</span>
                </div>
              </div>

              <div class="px-5 text-center flex flex-col items-center justify-center flex-1">
                <div class="w-20 h-20 rounded-3xl bg-red-50 flex items-center justify-center mb-4">
                  <svg class="w-14 h-14" viewBox="0 0 64 64" fill="none">
                    <path d="M32 8L58 54H6L32 8Z" fill="#db0007" stroke="#db0007" stroke-width="4" stroke-linejoin="round"/>
                    <rect x="30" y="24" width="4" height="15" rx="2" fill="white"/>
                    <circle cx="32" cy="45" r="2.5" fill="white"/>
                  </svg>
                </div>

                <h4 class="font-display font-black text-lg text-brand-dark mb-2">
                  Error de sensor
                </h4>
                <p class="text-[11px] text-zinc-600 leading-relaxed">
                  No se pudo verificar el peso. Por favor, revisá la balanza o contactá a mantenimiento.
                </p>

                ${sensorChecking ? `
                  <div class="mt-3 bg-amber-50 border border-amber-200 text-amber-800 text-[10px] font-bold px-3 py-1.5 rounded-full animate-pulse">
                    Calibrando balanza...
                  </div>
                ` : ''}

                ${assistanceSent ? `
                  <div class="mt-3 bg-emerald-50 border border-emerald-200 text-emerald-700 text-[10px] font-bold px-3 py-1.5 rounded-full">
                    ✓ Ticket enviado a soporte técnico
                  </div>
                ` : ''}
              </div>

              <div class="p-3.5 space-y-2 bg-zinc-50 border-t border-zinc-100 shrink-0">
                <button type="button" id="retry-sensor-btn" class="w-full bg-[#ffbc0d] hover:bg-brand-yellowLight text-brand-dark font-display font-extrabold text-xs py-2.5 rounded-full shadow-sm transition transform active:scale-95 cursor-pointer">
                  Reintentar
                </button>
                <button type="button" id="request-assist-btn" class="w-full bg-white hover:bg-zinc-100 text-brand-dark border border-zinc-200 font-display font-bold text-xs py-2 rounded-full transition cursor-pointer">
                  Solicitar asistencia
                </button>
              </div>
            </div>
          `;

          document.getElementById('retry-sensor-btn').addEventListener('click', () => {
            sensorChecking = true;
            assistanceSent = false;
            renderPhoneApp(false);
            setTimeout(() => {
              sensorChecking = false;
              currentScreen = 'inicio';
              renderPhoneApp(true);
            }, 600);
          });

          document.getElementById('request-assist-btn').addEventListener('click', () => {
            assistanceSent = true;
            renderPhoneApp(false);
          });
        }

        /* TAREAS DEL TURNO */
        else if (currentScreen === 'tareas') {
          const pendingCount = shiftTasks.filter(t => !t.done).length;
          phoneViewport.innerHTML = `
            ${renderRedHeader(true, 'inicio', 'bell')}
            <div class="${animClass} p-4 flex-1 overflow-y-auto">
              <div class="flex items-center justify-between mb-3">
                <h4 class="font-display font-extrabold text-base text-brand-dark">Tareas del turno</h4>
                <span class="bg-[#ffbc0d] text-brand-dark font-display font-extrabold text-[10px] px-2.5 py-0.5 rounded-full">
                  ${pendingCount} pend.
                </span>
              </div>
              <div class="space-y-2">
                ${shiftTasks.map(task => `
                  <button type="button" data-task-id="${task.id}" class="toggle-task-btn w-full text-left p-3 rounded-2xl border ${task.done ? 'bg-zinc-50 border-zinc-200 opacity-75' : 'bg-white border-[#ffbc0d] shadow-2xs'} flex items-center justify-between gap-2 transition cursor-pointer">
                    <div class="flex items-center gap-2.5">
                      <span class="w-4 h-4 rounded-md flex items-center justify-center text-[10px] font-black ${task.done ? 'bg-emerald-500 text-white' : 'border-2 border-zinc-300'}">
                        ${task.done ? '✓' : ''}
                      </span>
                      <div>
                        <div class="font-display font-bold text-xs ${task.done ? 'line-through text-zinc-400' : 'text-brand-dark'}">${task.title}</div>
                        <div class="text-[10px] text-zinc-400">Turno · ${task.time} hs</div>
                      </div>
                    </div>
                  </button>
                `).join('')}
              </div>
            </div>
          `;

          document.querySelectorAll('.toggle-task-btn').forEach(btn => {
            btn.addEventListener('click', () => {
              const id = Number(btn.dataset.taskId);
              const t = shiftTasks.find(item => item.id === id);
              if (t) {
                t.done = !t.done;
                renderPhoneApp(false);
              }
            });
          });
        }

        /* PERFIL */
        else if (currentScreen === 'perfil') {
          phoneViewport.innerHTML = `
            ${renderRedHeader(true, 'inicio', 'bell')}
            <div class="${animClass} p-4 flex-1 overflow-y-auto text-center">
              <div class="w-16 h-16 rounded-full bg-brand-dark text-[#ffbc0d] font-display font-black text-xl flex items-center justify-center mx-auto mt-2 mb-2.5">
                OP
              </div>
              <h4 class="font-display font-extrabold text-base text-brand-dark">Operador Certificado</h4>
              <span class="inline-block bg-emerald-100 text-emerald-700 font-display font-bold text-[10px] px-3 py-0.5 rounded-full mt-1 mb-4">
                ✓ Habilitación Técnica Activa
              </span>
              <div class="bg-white rounded-2xl p-3.5 border border-zinc-200 text-left space-y-2.5 text-xs">
                <div class="flex justify-between"><span class="text-zinc-500">Sucursal:</span><span class="font-bold text-brand-dark">Local #014</span></div>
                <div class="flex justify-between"><span class="text-zinc-500">Umbral activo:</span><span class="font-bold text-[#db0007]">${alertThreshold}% (${alertThreshold === 50 ? 'Pico' : 'Valle'})</span></div>
                <div class="flex justify-between"><span class="text-zinc-500">Reposiciones hoy:</span><span class="font-bold text-brand-dark">4 completadas</span></div>
              </div>
            </div>
          `;
        }

        document.querySelectorAll('.app-go-btn').forEach(btn => {
          btn.addEventListener('click', () => {
            currentScreen = btn.dataset.go;
            renderPhoneApp(true);
          });
        });

        updateNavIndicators();

        if (window.lucide) {
          lucide.createIcons();
        }
      }

      document.querySelectorAll('.screen-nav-pill').forEach(pill => {
        pill.addEventListener('click', () => {
          const target = pill.dataset.screen;
          if (target === 'proceso' && currentKg >= 5.0) currentKg = 3.2;
          currentScreen = target;
          renderPhoneApp(true);
        });
      });

      document.querySelectorAll('.phone-tab-btn').forEach(btn => {
        btn.addEventListener('click', () => {
          currentScreen = btn.dataset.navTab;
          renderPhoneApp(true);
        });
      });

      document.querySelectorAll('.app-feature-btn').forEach(btn => {
        btn.addEventListener('click', () => {
          document.querySelectorAll('.app-feature-btn').forEach(b => {
            b.classList.remove('border-brand-red/30');
            b.classList.add('border-transparent');
          });
          btn.classList.remove('border-transparent');
          btn.classList.add('border-brand-red/30');

          const jumpMap = { '3': 'maquinas', '5': 'instrucciones', '8': 'error' };
          currentScreen = jumpMap[btn.dataset.jumpScreen] || 'inicio';
          renderPhoneApp(true);
        });
      });

      const simValleBtn = document.getElementById('sim-valle-btn');
      const simPicoBtn = document.getElementById('sim-pico-btn');

      document.getElementById('sim-reset-btn').addEventListener('click', () => {
        machinesState = getInitialMachines();
        alertThreshold = 30;
        activeMachineId = 1;
        currentKg = 3.2;
        assistanceSent = false;
        sensorChecking = false;
        shiftTasks[1].done = false;
        currentScreen = 'inicio';
        simValleBtn.className = 'text-[11px] font-display font-extrabold px-3 py-1 rounded-full bg-brand-yellow text-brand-dark shadow-xs cursor-pointer transition';
        simPicoBtn.className = 'text-[11px] font-display font-extrabold px-3 py-1 rounded-full bg-zinc-200 hover:bg-brand-red hover:text-white text-brand-dark cursor-pointer transition';
        renderPhoneApp(true);
      });

      simValleBtn.addEventListener('click', () => {
        alertThreshold = 30;
        simValleBtn.className = 'text-[11px] font-display font-extrabold px-3 py-1 rounded-full bg-brand-yellow text-brand-dark shadow-xs cursor-pointer transition';
        simPicoBtn.className = 'text-[11px] font-display font-extrabold px-3 py-1 rounded-full bg-zinc-200 hover:bg-brand-red hover:text-white text-brand-dark cursor-pointer transition';

        const m1Cheese = machinesState[0].ingredients.find(i => i.name === 'Queso');
        if (m1Cheese) m1Cheese.pct = 30;
        renderPhoneApp(true);
      });

      simPicoBtn.addEventListener('click', () => {
        alertThreshold = 50;
        simPicoBtn.className = 'text-[11px] font-display font-extrabold px-3 py-1 rounded-full bg-[#db0007] text-white shadow-xs cursor-pointer transition';
        simValleBtn.className = 'text-[11px] font-display font-extrabold px-3 py-1 rounded-full bg-zinc-200 hover:bg-brand-yellow text-brand-dark cursor-pointer transition';

        const m1Cheese = machinesState[0].ingredients.find(i => i.name === 'Queso');
        if (m1Cheese) m1Cheese.pct = 48;
        activeMachineId = 1;
        renderPhoneApp(true);
      });

      renderPhoneApp(true);

      /* ---------------------------------------------------------
         NAVIGATION DRAWER & FORM VALIDATION
      --------------------------------------------------------- */
      const menuToggle = document.getElementById('menu-toggle');
      const menuClose = document.getElementById('menu-close');
      const navDrawer = document.getElementById('nav-drawer');
      const navBackdrop = document.getElementById('nav-drawer-backdrop');

      function openDrawer() {
        navDrawer.classList.remove('-translate-x-full');
        navBackdrop.classList.remove('hidden');
        setTimeout(() => navBackdrop.classList.remove('opacity-0'), 10);
      }

      function closeDrawer() {
        navDrawer.classList.add('-translate-x-full');
        navBackdrop.classList.add('opacity-0');
        setTimeout(() => navBackdrop.classList.add('hidden'), 300);
      }

      menuToggle.addEventListener('click', openDrawer);
      menuClose.addEventListener('click', closeDrawer);
      navBackdrop.addEventListener('click', closeDrawer);
      document.querySelectorAll('.drawer-link').forEach(link => {
        link.addEventListener('click', closeDrawer);
      });

      // Modality Radio Card Selection Styling
      const modalityCards = document.querySelectorAll('.modality-card');
      const modalityRadios = document.querySelectorAll('input[name="modality"]');

      function updateModalityCardStyles() {
        modalityRadios.forEach(radio => {
          const card = radio.closest('.modality-card');
          if (radio.checked) {
            card.classList.add('border-brand-yellow', 'bg-white', 'shadow-xs');
            card.classList.remove('border-zinc-200', 'bg-[#F3F4F6]');
          } else {
            card.classList.remove('border-brand-yellow', 'bg-white', 'shadow-xs');
            card.classList.add('border-zinc-200', 'bg-[#F3F4F6]');
          }
        });
      }

      modalityRadios.forEach(radio => {
        radio.addEventListener('change', updateModalityCardStyles);
      });
      updateModalityCardStyles();

      // Form Submit & Modal Logic
      const reservationForm = document.getElementById('reservation-form');
      const modal = document.getElementById('confirmation-modal');
      const closeModalBtn = document.getElementById('close-modal-btn');
      const doneModalBtn = document.getElementById('done-modal-btn');
      const copyCodeBtn = document.getElementById('copy-code-btn');

      reservationForm.addEventListener('submit', (e) => {
        e.preventDefault();

        const fullNameInput = document.getElementById('fullName');
        const emailInput = document.getElementById('email');
        const phoneInput = document.getElementById('phone');
        const staffInput = document.getElementById('staffCount');

        let isValid = true;

        [fullNameInput, emailInput, phoneInput, staffInput].forEach(input => {
          const errorMsg = input.parentElement.querySelector('.error-msg');
          if (!input.value.trim() || (input.type === 'email' && !input.value.includes('@'))) {
            input.classList.add('border-brand-red', 'bg-red-50/30');
            if (errorMsg) errorMsg.classList.remove('hidden');
            isValid = false;
          } else {
            input.classList.remove('border-brand-red', 'bg-red-50/30');
            if (errorMsg) errorMsg.classList.add('hidden');
          }
        });

        if (!isValid) return;

        const fullNameVal = fullNameInput.value.trim();
        const emailVal = emailInput.value.trim();
        const staffVal = staffInput.value.trim();
        const selectedModality = document.querySelector('input[name="modality"]:checked').value;

        const randomNum = Math.floor(100 + Math.random() * 900);
        const passCode = `MCD-2026-${randomNum}`;

        document.getElementById('ticket-code').textContent = passCode;
        document.getElementById('ticket-name').textContent = fullNameVal;
        document.getElementById('ticket-staff').textContent = `${staffVal} ${staffVal === 1 ? 'empleado' : 'empleados'}`;
        document.getElementById('ticket-modality').textContent = selectedModality;
        document.getElementById('modal-summary-text').textContent =
          `Enviamos el pase de acceso y el cronograma técnico a ${emailVal}.`;

        modal.classList.remove('hidden');
        modal.classList.add('flex');
      });

      function hideConfirmationModal() {
        modal.classList.add('hidden');
        modal.classList.remove('flex');
      }

      closeModalBtn.addEventListener('click', hideConfirmationModal);
      doneModalBtn.addEventListener('click', () => {
        hideConfirmationModal();
        reservationForm.reset();
        updateModalityCardStyles();
      });

      modal.addEventListener('click', (e) => {
        if (e.target === modal) hideConfirmationModal();
      });

      copyCodeBtn.addEventListener('click', () => {
        const codeText = document.getElementById('ticket-code').textContent;
        const tempInput = document.createElement('input');
        tempInput.value = codeText;
        document.body.appendChild(tempInput);
        tempInput.select();
        try {
          document.execCommand('copy');
          copyCodeBtn.textContent = '¡Código copiado!';
          setTimeout(() => {
            copyCodeBtn.textContent = 'Copiar pase';
          }, 2000);
        } catch (err) {
          copyCodeBtn.textContent = codeText;
        }
        document.body.removeChild(tempInput);
      });
    });
  </script>
</body>
</html>
