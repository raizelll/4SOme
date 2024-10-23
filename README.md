
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Sederhana</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 50px;
        }

        .container {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 300px;
            margin: 0 auto;
        }

        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            cursor: pointer;
            width: 100%;
            border-radius: 5px;
        }

        button:hover {
            background-color: #0056b3;
        }

        #welcome {
            display: none;
        }

        #loginForm {
            display: block;
        }

        img {
            max-width: 100%;
            height: auto;
            margin-top: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>

    <!-- Form Login -->
    <div class="container" id="loginForm">
        <h1>Login</h1>
        <p>Masukkan nama pengguna dan kata sandi untuk melanjutkan:</p>
        <input type="text" id="username" placeholder="Nama Pengguna"><br>
        <input type="password" id="password" placeholder="Kata Sandi"><br>
        <button onclick="login()">Login</button>
    </div>

    <!-- Halaman setelah login -->
    <div class="container" id="welcome">
        <h1>Selamat Datang</h1>
        <p>Anda berhasil login!</p>
        <img src="gambar.jpg" alt="Gambar Ilustrasi">
    </div>

    <script>
        function login() {
            var username = document.getElementById('username').value;
            var password = document.getElementById('password').value;

            // Sederhana: cek jika username dan password tidak kosong (bisa dimodifikasi untuk logika autentikasi sebenarnya)
            if (username === "user" && password === "1234") {
                document.getElementById('loginForm').style.display = "none"; // Sembunyikan form login
                document.getElementById('welcome').style.display = "block"; // Tampilkan halaman selamat datang
            } else {
                alert("Nama pengguna atau kata sandi salah!");
            }
        }
    </script>

</body>
</html>
