<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Untuk Evelyn Tersayang</title>
    <style>
        :root {
            --primary-pink: #ff4d6d;
            --soft-pink: #fff0f5;
            --dark-pink: #c71585;
        }

        body {
            background-color: var(--soft-pink);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            overflow-x: hidden;
            padding: 20px;
            box-sizing: border-box;
        }

        .container {
            max-width: 600px;
            background: rgba(255, 255, 255, 0.8);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(255, 77, 109, 0.2);
            backdrop-filter: blur(10px);
        }

        .bear-container {
            width: 150px;
            margin: 0 auto 20px;
            animation: bounce 2s infinite ease-in-out;
        }

        h1 {
            color: var(--primary-pink);
            font-size: 1.8rem;
            line-height: 1.6;
            margin-bottom: 30px;
            animation: fadeIn 2s ease-in;
        }

        /* Tombol Interaktif */
        .btn-pro {
            background-color: var(--primary-pink);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(255, 77, 109, 0.4);
            transition: all 0.3s ease;
        }

        .btn-pro:hover {
            transform: scale(1.05);
            background-color: var(--dark-pink);
        }

        /* Galeri Foto Hidden */
        .gallery-section {
            display: none;
            margin-top: 30px;
            animation: slideUp 1s ease forwards;
        }

        .gallery-title {
            color: var(--dark-pink);
            font-size: 1.2rem;
            margin-bottom: 15px;
        }

        .photo-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-top: 20px;
        }

        .photo-card {
            background: white;
            padding: 8px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
            transform: rotate(var(--rotation));
            transition: transform 0.3s;
        }

        .photo-card:hover {
            transform: rotate(0deg) scale(1.05);
            z-index: 10;
        }

        .photo-card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 5px;
        }

        /* Animasi */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-15px); }
        }

        @keyframes slideUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Beruang Kuning Lucu -->
        <div class="bear-container">
            <img src="https://cdn-icons-png.flaticon.com/512/3069/3069171.png" alt="Beruang Lucu" width="100%">
        </div>

        <!-- Pesan Sayang -->
        <h1>
            Maaf yaa sayanggkuu Evelynnn yangggg cyyannnttiiikkk, iiimmyyyuttss, lucccyuuww, cintakuu, bagindaaa ratukuu, boocccyyyiillkuuuu, kanjenggg ratu, ndoroo ayuuuu, my princesss, my queeen! 🥺👉👈
        </h1>

        <!-- Tombol Trigger -->
        <button class="btn-pro" onclick="bukaGaleri()">Klik kalau dimaafin ❤️</button>

        <!-- Bagian Akhir: Foto-foto -->
        <div class="gallery-section" id="galeriFoto">
            <hr style="border: 0; border-top: 1px calc() var(--primary-pink); margin: 20px 0;">
            <p class="gallery-title">Yay! Ini memori manis kita, jangan marah lagi yaaa: 🥰</p>
            
            <div class="photo-grid">
                <!-- Foto 1 -->
                <div class="photo-card" style="--rotation: -3deg;">
                    <img src="foto1.jpg" alt="Foto Evelyn 1">
                </div>
                <!-- Foto 2 -->
                <div class="photo-card" style="--rotation: 4deg;">
                    <img src="foto2.jpg" alt="Foto Evelyn 2">
                </div>
                <!-- Foto 3 -->
                <div class="photo-card" style="--rotation: -2deg;">
                    <img src="foto3.jpg" alt="Foto Evelyn 3">
                </div>
                <!-- Foto 4 -->
                <div class="photo-card" style="--rotation: 3deg;">
                    <img src="foto4.jpg" alt="Foto Evelyn 4">
                </div>
            </div>
        </div>
    </div>

    <script>
        function bukaGaleri() {
            const galeri = document.getElementById('galeriFoto');
            galeri.style.display = 'block';
            
            // Efek otomatis scroll ke bagian foto
            setTimeout(() => {
                galeri.scrollIntoView({ behavior: 'smooth' });
            }, 100);
        }
    </script>

</body>
</html>
