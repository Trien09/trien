# trien
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trang Web Sinh Động</title>
    <style>
        body {
            background-color: #f4f4f9;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            overflow-x: hidden; /* Ngừng cuộn ngang */
        }

        .dragon {
            position: absolute;
            width: 150px;
            height: 150px;
            background: url('https://www.pngall.com/wp-content/uploads/2016/06/Dragon-PNG-Image.png') no-repeat center center;
            background-size: contain;
            animation: fly 5s infinite linear;
            z-index: 10;
        }

        @keyframes fly {
            0% { transform: translateX(-200px); }
            50% { transform: translateX(100vw); }
            100% { transform: translateX(-200px); }
        }

        .register-box {
            width: 300px;
            background-color: white;
            padding: 20px;
            margin: 50px auto;
            border-radius: 10px;
            box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.1);
        }

        h2 {
            text-align: center;
            color: #333;
        }

        input[type="text"], input[type="email"], input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }

        input[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        input[type="submit"]:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>

    <!-- Con rồng bay -->
    <div class="dragon"></div>

    <!-- Form đăng ký người chơi -->
    <div class="register-box">
        <h2>Đăng Ký Người Chơi</h2>
        <form action="/submit_form" method="POST">
            <input type="text" name="username" placeholder="Tên người dùng" required>
            <input type="email" name="email" placeholder="Email" required>
            <input type="password" name="password" placeholder="Mật khẩu" required>
            <input type="submit" value="Đăng Ký">
        </form>
    </div>

</body>
</html>
