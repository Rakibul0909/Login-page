
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to right, #FF4B85, #FF61A6, #7C4DFF, #00BFAE); /* All color mix background */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .login-container {
            background-color: #fff;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            width: 350px;
            text-align: center;
            animation: slideUp 0.6s ease-out;
        }
        h2 {
            margin-bottom: 30px;
            color: #333;
            font-size: 28px;
        }
        .input-field {
            width: 100%;
            padding: 15px;
            margin: 15px 0;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            transition: border-color 0.3s;
        }
        .input-field:focus {
            border-color: #FF61A6;
            outline: none;
        }
        .btn {
            width: 100%;
            padding: 15px;
            background-color: #4CAF50; /* Green button */
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .btn:hover {
            background-color: #45a049; /* Darker green on hover */
        }
        .message {
            margin-top: 15px;
            font-size: 16px;
            color: #fff;
        }
        .error {
            color: #ff4747;
        }
        .success {
            color: #4CAF50;
        }

        @keyframes slideUp {
            0% {
                transform: translateY(30px);
                opacity: 0;
            }
            100% {
                transform: translateY(0);
                opacity: 1;
            }
        }

    </style>
</head>
<body>
    <div class="login-container">
        <h2>Login</h2>
        <form id="loginForm" method="post">
            <input type="text" id="username" class="input-field" placeholder="Enter username" required>
            <input type="password" id="password" class="input-field" placeholder="Enter password" required>
            <button type="submit" class="btn">Login</button>
            <div id="message" class="message"></div>
        </form>
    </div>

    <script>
        document.getElementById('loginForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            const validUsername = "Rakibul";
            const validPassword = "7878";
            
            const messageElement = document.getElementById('message');
            
            if (username === validUsername && password === validPassword) {
                messageElement.textContent = "Login Successful!";
                messageElement.classList.remove('error');
                messageElement.classList.add('success');
            } else {
                messageElement.textContent = "Invalid Your Password";
                messageElement.classList.remove('success');
                messageElement.classList.add('error');
            }
        });
    </script>
</body>
</html>
   