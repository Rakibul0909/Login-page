<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login Page</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="login-container">
    <div class="login-box">
      <h2>Login</h2>
      <form id="loginForm">
        <div class="input-group">
          <input type="text" id="username" required>
          <label>Username</label>
        </div>
        <div class="input-group">
          <input type="password" id="password" required>
          <label>Password</label>
        </div>
        <button type="button" onclick="validateLogin()">Log in</button>
        <p id="message"></p>
      </form>
    </div>
  </div>
  <script src="script.js"></script>
</body>
</html>
