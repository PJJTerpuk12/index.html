<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PJJ Terpuk 12 GBKP Km8 - Persekutuan Jemaat</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, rgba(255,255,255,0.95), rgba(255,255,255,0.9));
            backdrop-filter: blur(15px);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
            border-bottom: 1px solid rgba(255,255,255,0.2);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .logo-icon {
            width: 55px;
            height: 55px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
        }

        .logo-text {
            font-size: 1.4rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        .nav-menu a {
            text-decoration: none;
            color: #2c3e50;
            font-weight: 600;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-menu a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            transition: width 0.3s ease;
        }

        .nav-menu a:hover::after {
            width: 100%;
        }

        .nav-menu a:hover {
            color: #667eea;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
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
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 1000"><defs><radialGradient id="a" cx="50%" cy="50%" r="50%"><stop offset="0%" stop-color="%23ffffff" stop-opacity="0.1"/><stop offset="100%" stop-color="%23ffffff" stop-opacity="0"/></radialGradient></defs><circle cx="200" cy="200" r="150" fill="url(%23a)"/><circle cx="800" cy="300" r="100" fill="url(%23a)"/><circle cx="400" cy="700" r="200" fill="url(%23a)"/><circle cx="900" cy="800" r="120" fill="url(%23a)"/></svg>');
            animation: float 20s ease-in-out infinite;
        }

        .hero-content {
            max-width: 900px;
            padding: 0 2rem;
            color: white;
            z-index: 2;
            position: relative;
        }

        .hero h1 {
            font-size: 4.5rem;
            font-weight: 900;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            letter-spacing: -2px;
        }

        .hero .subtitle {
            font-size: 1.8rem;
            margin-bottom: 2rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
            opacity: 0.9;
            font-weight: 300;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 2rem;
        }

        .btn {
            padding: 1rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .btn-primary {
            background: rgba(255,255,255,0.2);
            color: white;
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255,255,255,0.3);
        }

        .btn-primary:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        .btn-secondary {
            background: white;
            color: #667eea;
            border: 2px solid white;
        }

        .btn-secondary:hover {
            background: transparent;
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        /* Info Section */
        .info-section {
            position: absolute;
            right: 5%;
            top: 50%;
            transform: translateY(-50%);
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(20px);
            color: white;
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
            min-width: 350px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .info-section h3 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            text-align: center;
            font-weight: 700;
        }

        .info-item {
            margin-bottom: 1.2rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 0.8rem;
            background: rgba(255,255,255,0.1);
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .info-item:hover {
            background: rgba(255,255,255,0.2);
            transform: translateX(5px);
        }

        .info-icon {
            width: 35px;
            height: 35px;
            background: rgba(255,255,255,0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
        }

        .contact-btn {
            background: linear-gradient(135deg, #ff6b6b, #ee5a52);
            color: white;
            padding: 1.2rem 2rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-top: 1.5rem;
            width: 100%;
        }

        .contact-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 107, 107, 0.4);
        }

        /* Mobile Menu */
        .mobile-menu {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }

        .mobile-menu span {
            width: 28px;
            height: 3px;
            background: #2c3e50;
            margin: 4px 0;
            transition: 0.3s;
            border-radius: 2px;
        }

        /* Scroll Indicator */
        .scroll-indicator {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            color: white;
            animation: bounce 2s infinite;
            font-size: 2rem;
        }

        /* Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateX(-50%) translateY(0); }
            40% { transform: translateX(-50%) translateY(-15px); }
            60% { transform: translateX(-50%) translateY(-8px); }
        }

        .info-section {
            animation: float 4s ease-in-out infinite;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }

            .mobile-menu {
                display: flex;
            }

            .hero h1 {
                font-size: 3rem;
            }

            .hero .subtitle {
                font-size: 1.4rem;
            }

            .info-section {
                position: static;
                transform: none;
                margin: 2rem;
                width: calc(100% - 4rem);
                animation: none;
            }

            .hero {
                flex-direction: column;
                justify-content: center;
                gap: 2rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn {
                width: 100%;
                max-width: 300px;
            }

            nav {
                padding: 0 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">
                <div class="logo-icon">✝</div>
                <div class="logo-text">PJJ Terpuk 12</div>
            </div>
            <ul class="nav-menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#tentang">Tentang</a></li>
                <li><a href="#kegiatan">Kegiatan</a></li>
                <li><a href="#pengurus">Pengurus</a></li>
                <li><a href="#jadwal">Jadwal</a></li>
                <li><a href="#galeri">Galeri</a></li>
                <li><a href="#kontak">Kontak</a></li>
            </ul>
            <div class="mobile-menu">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </nav>
    </header>

    <main>
        <section class="hero" id="home">
            <div class="hero-content">
                <h1>PJJ TERPUK 12</h1>
                <p class="subtitle">Persekutuan Jemaat Jingga Terpadu Pungkuran 12<br>GBKP Km.8</p>
                <div class="hero-buttons">
                    <a href="#tentang" class="btn btn-primary">
                        📖 Tentang Kami
                    </a>
                    <a href="#kegiatan" class="btn btn-secondary">
                        🎯 Kegiatan
                    </a>
                </div>
            </div>
            
            <div class="info-section">
                <h3>🏛️ Info Persekutuan</h3>
                <div class="info-item">
                    <div class="info-icon">👥</div>
                    <div>
                        <div style="font-weight: bold;">Anggota Aktif</div>
                        <div style="opacity: 0.8;">50+ Jemaat</div>
                    </div>
                </div>
                <div class="info-item">
                    <div class="info-icon">📅</div>
                    <div>
                        <div style="font-weight: bold;">Pertemuan</div>
                        <div style="opacity: 0.8;">Minggu ke-2 & ke-4</div>
                    </div>
                </div>
                <div class="info-item">
                    <div class="info-icon">🕐</div>
                    <div>
                        <div style="font-weight: bold;">Waktu</div>
                        <div style="opacity: 0.8;">19.00 - 21.00 WIB</div>
                    </div>
                </div>
                <div class="info-item">
                    <div class="info-icon">📍</div>
                    <div>
                        <div style="font-weight: bold;">Lokasi</div>
                        <div style="opacity: 0.8;">GBKP Km.8 P.Bulan</div>
                    </div>
                </div>
                <button class="contact-btn">💬 Hubungi Pengurus</button>
            </div>

            <div class="scroll-indicator">
                ⬇️
            </div>
        </section>
    </main>

    <script>
        // Mobile menu toggle
        const mobileMenu = document.querySelector('.mobile-menu');
        const navMenu = document.querySelector('.nav-menu');

        mobileMenu.addEventListener('click', () => {
            navMenu.style.display = navMenu.style.display === 'flex' ? 'none' : 'flex';
        });

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Contact button action
        document.querySelector('.contact-btn').addEventListener('click', () => {
            // Ganti dengan nomor WhatsApp pengurus PJJ
            window.open('https://wa.me/6281234567890?text=Halo,%20saya%20ingin%20tahu%20lebih%20lanjut%20tentang%20PJJ%20Terpuk%2012', '_blank');
        });

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
                header.style.backdropFilter = 'blur(20px)';
            } else {
                header.style.background = 'linear-gradient(135deg, rgba(255,255,255,0.95), rgba(255,255,255,0.9))';
                header.style.backdropFilter = 'blur(15px)';
            }
        });

        // Parallax effect
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallax = document.querySelector('.hero::before');
            if (parallax) {
                parallax.style.transform = `translateY(${scrolled * 0.5}px)`;
            }
        });
    </script>
</body>
</html>
