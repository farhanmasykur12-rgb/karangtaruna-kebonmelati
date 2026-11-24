<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Karang Taruna — Kebon Melati RW 05, Dukuh Pinggir</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #1e40af;
            --secondary: #f59e0b;
            --dark: #1f2937;
            --light: #f9fafb;
        }

        body {
            line-height: 1.6;
            color: var(--dark);
            background: #f0f4f8;
        }

        nav {
            background: var(--primary);
            padding: 1rem 5%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            color: white;
            font-size: 1.3rem;
            font-weight: 700;
            text-decoration: none;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .menu-toggle {
            display: none;
            color: white;
            font-size: 1.8rem;
            cursor: pointer;
        }

        header {
            margin-top: 60px;
            background: linear-gradient(135deg, var(--primary) 0%, #1e3a8a 100%);
            color: white;
            padding: 5rem 5%;
            text-align: center;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        header p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
            opacity: 0.9;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 2rem;
            background: var(--secondary);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(245, 158, 11, 0.4);
        }

        section {
            padding: 4rem 5%;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--secondary);
            margin: 0.5rem auto 0;
            border-radius: 2px;
        }

        /* === PENGUMUMAN TURNAMEN === */
        .pengumuman {
            background: linear-gradient(135deg, #1e40af 0%, #111827 100%);
            color: white;
            padding: 3rem 2rem;
            border-radius: 16px;
            margin: 2rem 0;
            box-shadow: 0 8px 30px rgba(30, 64, 175, 0.3);
        }

        .pengumuman h2 {
            font-size: 2rem;
            text-align: center;
            margin-bottom: 0.5rem;
        }

        .pengumuman .sub-judul {
            text-align: center;
            color: #fcd34d;
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        .pengumuman-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            text-align: center;
            margin-bottom: 2rem;
        }

        .info-card {
            background: rgba(255,255,255,0.1);
            padding: 1.5rem;
            border-radius: 10px;
            border: 1px solid rgba(255,255,255,0.15);
        }

        .info-card h3 {
            color: var(--secondary);
            font-size: 1rem;
            margin-bottom: 0.5rem;
        }

        .info-card p {
            font-size: 1.1rem;
            font-weight: 600;
        }

        .daftar-box {
            text-align: center;
            background: rgba(245, 158, 11, 0.15);
            padding: 2rem;
            border-radius: 10px;
            border: 2px solid var(--secondary);
        }

        .daftar-box h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }

        .wa-btn {
            display: inline-block;
            background: #25d366;
            color: white;
            padding: 0.9rem 2rem;
            border-radius: 50px;
            font-weight: bold;
            text-decoration: none;
            font-size: 1.1rem;
            margin-top: 0.5rem;
            transition: background 0.3s;
        }

        .wa-btn:hover {
            background: #128c7e;
        }

        .hashtag {
            text-align: center;
            margin-top: 1.5rem;
            color: #93c5fd;
            font-weight: 500;
        }

        .tentang-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .tentang-text h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        .tentang-text p {
            margin-bottom: 1rem;
            text-align: justify;
        }

        .visi-misi {
            background: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        .visi-misi h4 {
            color: var(--secondary);
            margin-bottom: 0.8rem;
        }

        .program-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .program-card {
            background: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }

        .program-card:hover {
            transform: translateY(-5px);
        }

        .program-card h3 {
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .pengurus-table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        .pengurus-table th,
        .pengurus-table td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid #e5e7eb;
        }

        .pengurus-table th {
            background: var(--primary);
            color: white;
        }

        .kontak-form {
            background: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark);
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 2px solid #e5e7eb;
            border-radius: 6px;
            font-size: 1rem;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .btn-submit {
            background: var(--primary);
            color: white;
            border: none;
            cursor: pointer;
            padding: 0.8rem 2rem;
            font-size: 1rem;
            border-radius: 6px;
            transition: background 0.3s;
        }

        .btn-submit:hover {
            background: #1e3a8a;
        }

        .info-kontak {
            margin-top: 2rem;
            line-height: 2;
        }

        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem 5%;
            margin-top: 2rem;
        }

        @media (max-width: 768px) {
            .nav-links {
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: var(--primary);
                flex-direction: column;
                padding: 1rem;
                display: none;
            }

            .nav-links.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .tentang-content {
                grid-template-columns: 1fr;
            }

            header h1 {
                font-size: 1.8rem;
            }

            section > div[style*="grid-template-columns"] {
                grid-template-columns: 1fr !important;
            }
        }
    </style>
</head>
<body>

    <!-- Navigasi -->
    <nav>
        <div class="nav-container">
            <a href="#" class="logo">Karang<span>Taruna</span></a>
            <div class="menu-toggle" onclick="toggleMenu()">☰</div>
            <ul class="nav-links" id="navLinks">
                <li><a href="#beranda">Beranda</a></li>
                <li><a href="#pengumuman">Pengumuman</a></li>
                <li><a href="#tentang">Tentang</a></li>
                <li><a href="#program">Program</a></li>
                <li><a href="#pengurus">Pengurus</a></li>
                <li><a href="#kontak">Kontak</a></li>
            </ul>
        </div>
    </nav>

    <!-- Beranda -->
    <header id="beranda">
        <h1>Karang Taruna Kebon Melati<br>RW 05 — Dukuh Pinggir</h1>
        <p>Bersama Membangun Generasi Muda yang Kreatif, Produktif, dan Peduli Lingkungan</p>
        <a href="#pengumuman" class="btn">📢 Info Kegiatan Terbaru</a>
    </header>

    <!-- PENGUMUMAN TURNAMEN -->
    <section id="pengumuman" style="background: #f0f4f8; margin: 0 -5%; padding: 4rem 5%;">
        <div style="max-width: 1000px; margin: 0 auto;">
            <div class="pengumuman">
                <h2>⚽ TURNAMEN BOLA DUBES</h2>
                <p class="sub-judul">Edisi Akhir Tahun — Kegiatan Karang Taruna</p>
                
                <div class="pengumuman-grid">
                    <div class="info-card">
                        <h3>📅 Pendaftaran</h3>
                        <p>23 – 25 November</p>
                    </div>
                    <div class="info-card">
                        <h3>🎯 Mulai Pertandingan</h3>
                        <p>28 November</p>
                    </div>
                    <div class="info-card">
                        <h3>📍 Lokasi</h3>
                        <p>Stadion Kopro</p>
                    </div>
                    <div class="info-card">
                        <h3>💰 Kontribusi</h3>
                        <p>Rp 20.000 / Tim</p>
                    </div>
                    <div class="info-card">
                        <h3>📋 Sistem</h3>
                        <p>Acak / Kocokan</p>
                    </div>
                </div>

                <div class="daftar-box">
                    <h3>📲 Cara Mendaftar</h3>
                    <p>Silakan hubungi via WhatsApp:</p>
                    <p style="font-size: 1.3rem; font-weight: bold; margin: 0.5rem 0;">Dzuhri Rubino</p>
                    <a href="https://wa.me/6289513072791" target="_blank" class="wa-btn">
                        💬 0895-1307-2791
                    </a>
                    <p style="margin-top: 1rem; font-style: italic;">Sertai keseruan bersama kami! Ayo segera daftarkan tim kamu! 💪</p>
                </div>

                <div class="hashtag">
                    #TURNAMENBOLADUBES &nbsp; #BOLADUBES &nbsp; #KarangTarunaKebonMelati
                </div>
            </div>
        </div>
    </section>

    <!-- Tentang Kami -->
    <section id="tentang">
        <h2 class="section-title">Tentang Kami</h2>
        <div class="tentang-content">
            <div class="tentang-text">
                <h3>Siapa Kami?</h3>
                <p>Karang Taruna adalah organisasi sosial wadah pengembangan generasi muda yang tumbuh dan berkembang atas dasar kesadaran dan tanggung jawab sosial dari, oleh, dan untuk masyarakat.</p>
                <p>Karang Taruna Kelurahan Kebon Melati RW 05 — Dukuh Pinggir berkomitmen untuk memberdayakan pemuda di wilayah kita agar menjadi generasi yang mandiri, kreatif, dan bermanfaat bagi masyarakat.</p>
            </div>
            <div class="visi-misi">
                <h4>🎯 Visi</h4>
                <p>Terwujudnya pemuda yang beriman, berkualitas, mandiri, dan berpartisipasi aktif dalam pembangunan masyarakat.</p>
                <br>
                <h4>📋 Misi</h4>
                <ul style="margin-left: 1.2rem; line-height: 1.8;">
                    <li>Mengembangkan potensi dan kreativitas pemuda</li>
                    <li>Meningkatkan kepedulian sosial dan lingkungan</li>
                    <li>Membangun kerjasama antar pemuda dan masyarakat</li>
                    <li>Melaksanakan kegiatan yang bermanfaat bagi warga</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Program Kerja -->
    <section id="program" style="background: white; margin: 2rem -5%; padding: 4rem 5%;">
        <div style="max-width: 1200px; margin: 0 auto;">
            <h2 class="section-title">Program Kerja Kami</h2>
            <div class="program-grid">
                <div class="program-card">
                    <h3>🧦 Kegiatan Sosial</h3>
                    <p>Bakti sosial, kunjungan panti asuhan, dan bantuan kepada warga yang membutuhkan secara berkala.</p>
                </div>
                <div class="program-card">
                    <h3>🌿 Kebersihan Lingkungan</h3>
                    <p>Kerja bakti membersihkan lingkungan, penanaman pohon, dan pengelolaan sampah di wilayah Dukuh Pinggir.</p>
                </div>
                <div class="program-card">
                    <h3>⚽ Olahraga & Seni</h3>
                    <p>Kompetisi olahraga antar warga, panggung seni, dan kegiatan positif lainnya untuk
