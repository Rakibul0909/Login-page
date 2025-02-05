<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 50px;
        }
        .login-box {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            margin: auto;
        }
        input {
            width: 90%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: blue;
            color: white;
            border: none;
            padding: 10px;
            width: 100%;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: darkblue;
        }
    </style>
</head>
<body>

    <div class="login-box">
        <h2>Login</h2>
        <input type="text" id="username" placeholder="Enter Username">
        <input type="password" id="password" placeholder="Enter Password">
        <button onclick="checkLogin()">Login</button>
        <p id="message" style="color: red; font-weight: bold;"></p>
    </div>

    <script>
        function checkLogin() {
            var user = document.getElementById("username").value;
            var pass = document.getElementById("password").value;
            
            if (user === "Rakibul" && pass === "7879") {
                document.getElementById("message").style.color = "green";
                document.getElementById("message").innerText = "Login Successful!";
            } else {
                document.getElementById("message").innerText = "Invalid Username or Password!";
            }
        }
    </script>

</body>
</html>
