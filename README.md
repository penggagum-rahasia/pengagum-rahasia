<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WillYouBeMine?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f8f9fa;
            color: #333;
            margin: 0;
            padding: 0;
        }
        .container {
            margin-top: 50px;
        }
        h1 {
            color: #e74c3c;
        }
        p {
            font-size: 18px;
            color: #555;
        }
        .button {
            background-color: #e74c3c;
            color: white;
            padding: 15px 25px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 10px;
            border-radius: 5px;
            transition: background-color 0.3s ease;
            cursor: pointer;
        }
        .button:hover {
            background-color: #c0392b;
        }
        footer {
            margin-top: 50px;
            font-size: 14px;
            color: #888;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Dear Adinda Putri Amaliah</h1>
        <p>Ada sesuatu yang ingin aku sampaikan...</p>
        
        <h2>Pengakuan</h2>
        <p>Sejak kita bertemu, aku mulai menyadari bahwa kamu adalah orang yang spesial. Aku suka caramu tersenyum, caramu berbicara, dan bagaimana kamu membuat hariku lebih cerah.</p>
        <p>Jadi, aku ingin jujur, aku suka kamu dan berharap kita bisa menjadi lebih dari sekadar teman.</p>
        
        <h3>Apakah kamu juga merasa hal yang sama?</h3>
        <button class="button" onclick="chooseAnswer('Aku juga suka kamu!')">Aku juga suka kamu!</button>
        <button class="button" onclick="chooseAnswer('Kita bisa ngobrol lebih lanjut?')">Kita bisa ngobrol lebih lanjut?</button>
        <button class="button" onclick="chooseAnswer('Aku butuh waktu untuk berpikir.')">Aku butuh waktu untuk berpikir.</button>
        <br><br>
        <button class="button" onclick="getAnswer()">Cek Jawaban</button>
    </div>

    <footer>
        <p>Dibuat dengan ♥ oleh N</p>
    </footer>

    <script>
        // Fungsi untuk menyimpan pilihan ke Local Storage
        function chooseAnswer(answer) {
            localStorage.setItem('chosenAnswer', answer);
            alert('Jawabanmu telah disimpan: ' + answer);
        }

        // Fungsi untuk mendapatkan jawaban yang dipilih (bisa dipakai di halaman lain)
        function getAnswer() {
            const answer = localStorage.getItem('chosenAnswer');
            if (answer) {
                alert('Jawaban yang dipilih: ' + answer);
            } else {
                alert('Belum ada jawaban yang dipilih.');
            }
        }
    </script>
</body>
</html>
