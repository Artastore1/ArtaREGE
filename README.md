<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LIST HARGA REGE/GS/PANEL NYA</title>
    <title>ALL TRANSAKSI UDAH OTOMATIS</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #1d1f20;
            color: #f0f0f0;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
        .container {
            background-color: #2a2d2e;
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
            max-width: 800px;
            width: 90%;
            margin: 20px;
        }
        h1, h2, h3 {
            text-align: center;
            color: #76c7c0;
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        li {
            background-color: #3b3f40;
            margin: 10px 0;
            padding: 15px;
            border: 1px solid #5c6061;
            border-radius: 8px;
            transition: background-color 0.3s;
        }
        li:hover {
            background-color: #444;
        }
        .instructions, .qris, .upload-section, .download-link {
            text-align: center;
            margin: 20px 0;
        }
        .qris input, .upload-section input {
            display: block;
            margin: 10px auto;
            padding: 10px;
            width: 80%;
            max-width: 300px;
            border-radius: 8px;
            border: 1px solid #5c6061;
            background-color: #3b3f40;
            color: #f0f0f0;
        }
        .qris button, .upload-section button {
            display: block;
            margin: 10px auto;
            padding: 10px 20px;
            background-color: #76c7c0;
            color: #1d1f20;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .qris button:hover, .upload-section button:hover {
            background-color: #64b0a9;
        }
        .download-link {
            display: none;
            text-align: center;
        }
        .download-link a {
            color: #76c7c0;
            text-decoration: none;
            font-weight: bold;
        }
        .download-link a:hover {
            text-decoration: underline;
        }
        img {
            max-width: 200px;
            margin: 10px auto;
            display: block;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>LIST HARGA NYA</h1>
        
        <h2>List Harga GS VIP</h2>
        <ul>
            <li>GS 30% Headshot 5K (kode: gs30)</li>
            <li>GS 40% Headshot 7K (kode: gs40)</li>
            <li>GS 50% Headshot 10K (kode: gs50)</li>
            <li>GS 60% Headshot 15K (kode: gs60)</li>
            <li>GS 70% Headshot 20K (kode: gs70)</li>
            <li>GS 80% Headshot 25K (kode: gs80)</li>
            <li>GS 90% Headshot 30K (kode: gs90)</li>
            <li>GS 97% Headshot 35K (kode: gs97)</li>
        </ul>

        <h2>List Harga Rege VIP</h2>
        <ul>
            <li>Rege Pelicin Layar 5K (kode: rege_pelicin)</li>
            <li>Rege AIM Stabil Lity 10K (kode: rege_stabil)</li>
            <li>Rege AIM Lock 15K (kode: rege_lock)</li>
            <li>Rege AIM FOV 20K (kode: rege_fov)</li>
            <li>Rege Agresif + AIM Stability V3 25K (kode: rege_agresif)</li>
        </ul>

        <h2>List Harga Panel</h2>
        <ul>
            <li>Panel 15K (kode: panel)</li>
        </ul>

        <div class="instructions">
            <h3>Cara Pembelian</h3>
            <ol>
                <li>Pilih produk yang ingin dibeli dari daftar di atas.</li>
                <li>Masukkan nominal transfer dan klik tombol untuk mendapatkan QRIS.</li>
                <li>Lakukan pembayaran melalui QRIS.</li>
                <li>Setelah pembayaran, screenshot bukti transfer Anda.</li>
                <li>Upload bukti transfer pada form yang tersedia di bawah ini, beserta kode produk yang dibeli.</li>
                <li>Setelah verifikasi, link download untuk produk yang dibeli akan muncul.</li>
            </ol>
        </div>

        <div class="qris">
            <input type="number" id="nominalTF" placeholder="Masukkan nominal transfer">
            <button onclick="generateQRIS()">Dapatkan QRIS</button>
            <div id="qrisImage"></div>
        </div>

        <div class="upload-section">
            <p>Upload Bukti Transfer:</p>
            <input type="file" id="buktiTF">
            <input type="text" id="kodeProduk" placeholder="Masukkan kode produk (contoh: rege_lock)">
            <button onclick="showDownloadLink()">Submit</button>
        </div>

        <div class="download-link">
            <p>Terima kasih! Anda dapat mendownload file Anda di sini:</p>
            <a id="downloadLink" href="#">Download Link</a>
        </div>
    </div>

    <script>
        function generateQRIS() {
            var nominal = document.getElementById('nominalTF').value;
            if (nominal) {
                var qrisLink = 'https://saweria.co/Artaboys?nominal=' + nominal;
                document.getElementById('qrisImage').innerHTML = '<img src="https://api.qrserver.com/v1/create-qr-code/?data=' + encodeURIComponent(qrisLink) + '&size=200x200" alt="QRIS">';
            } else {
                alert('Masukkan nominal transfer terlebih dahulu.');
            }
        }

        function showDownloadLink() {
            var kodeProduk = document.getElementById('kodeProduk').value.toLowerCase();
            var downloadLink = document.getElementById('downloadLink');

            var links = {
                'gs30': 'https://drive.google.com/file/d/1yJAcKBx_QSxEGHZZklaMF0duyzJDltg9/view?usp=drive_link',
                'gs40': 'https://drive.google.com/file/d/1yJAcKBx_QSxEGHZZklaMF0duyzJDltg9/view?usp=drive_link',
                'gs50': 'https://drive.google.com/file/d/1yJAcKBx_QSxEGHZZklaMF0duyzJDltg9/view?usp=drive_link.',
                'gs60': 'https://drive.google.com/file/d/1yJAcKBx_QSxEGHZZklaMF0duyzJDltg9/view?usp=drive_link',
                'gs70': 'https://drive.google.com/file/d/1yJAcKBx_QSxEGHZZklaMF0duyzJDltg9/view?usp=drive_link',
                'gs80': 'https://drive.google.com/file/d/1yJAcKBx_QSxEGHZZklaMF0duyzJDltg9/view?usp=drive_link',
                'gs90': 'https://drive.google.com/file/d/1yJAcKBx_QSxEGHZZklaMF0duyzJDltg9/view?usp=drive_link',
                'gs97': 'https://drive.google.com/file/d/1yJAcKBx_QSxEGHZZklaMF0duyzJDltg9/view?usp=drive_link',
                'rege_pelicin': 'https://drive.google.com/file/d/17Z6i20PckE-dhMopvOoCbm1agpTqZ5ag/view?usp=drive_link',
                'rege_stabil': 'https://drive.google.com/file/d/1OoQ7ggiLdUNXre-xzo0L1VK36gyInAb0/view?usp=drive_link',
                'rege_lock': 'https://drive.google.com/file/d/1jGZfpaveIVI4dGFLYicMuGfFLOWYJ78Z/view?usp=drive_link',
                'rege_fov': 'https://drive.google.com/file/d/1YtIJrz_ch1bOctkzoz6aiMA-NqYkmn_O/view?usp=drive_link',
                'rege_agresif': 'https://drive.google.com/file/d/1iJ0OuVis0IFGpuMHOgvoWXSMWHV_naux/view?usp=drive_link',
                'panel': 'https://drive.google.com/file/d/1k5mX977fec-w-Nem9I4F9qg9OGKvIBs7/view?usp=drive_link'
            };

            if (links[kodeProduk]) {
                downloadLink.href = links[kodeProduk];
                document.querySelector('.download-link').style.display = 'block';
            } else {
                alert('Kode produk tidak dikenal!');
                downloadLink.href = '#';
                document.querySelector('.download-link').style.display = 'none';
            }
        }
    </script>
</body>
</html>
