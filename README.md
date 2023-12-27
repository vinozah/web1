<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login Admin</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #f4f4f4;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    #login-form {
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      border-radius: 8px;
      text-align: center;
    }

    h2 {
      color: #333;
    }

    #error-message {
      color: red;
      margin-bottom: 10px;
    }

    label {
      display: block;
      margin: 10px 0;
      color: #555;
    }

    input {
      width: 100%;
      padding: 8px;
      margin: 6px 0 12px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    input[type="submit"] {
      background-color: #4caf50;
      color: white;
      cursor: pointer;
    }

    input[type="submit"]:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

  <div id="login-form">
    <h2>Login</h2>
    <div id="error-message"></div>
    <form onsubmit="login(event)">
      <label for="username">Username:</label>
      <input type="text" id="username" name="username" required>

      <label for="password">Password:</label>
      <input type="password" id="password" name="password" required>

      <input type="submit" value="Login">
    </form>
  </div>

  <script>
    function login(event) {
      event.preventDefault();

      // Get username and password from the form
      var username = document.getElementById('username').value;
      var password = document.getElementById('password').value;

      // Check if the credentials are correct
      if (username === 'admin' && password === 'sehat123') {
        // Redirect to the data entry page (dummy URL for example)
        window.location.href = 'cod.html';
      } else {
        // Display error message
        document.getElementById('error-message').innerText = 'Username atau password salah';
      }
    }
  </script>

</body>
</html>
