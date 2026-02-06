      <!DOCTYPE html>
      <html>
      <head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Apex Oil Company - Login</title>
          <style>
              body {
                  margin: 0;
                  font-family: Arial, sans-serif;
                  background: linear-gradient(135deg, #1B4F72 0%, #2E86AB 100%);
                  min-height: 100vh;
                  display: flex;
                  align-items: center;
                  justify-content: center;
              }
              .login-box {
                  background: white;
                  padding: 40px;
                  border-radius: 20px;
                  width: 90%;
                  max-width: 400px;
                  box-shadow: 0 20px 60px rgba(0,0,0,0.3);
              }
              .logo {
                  text-align: center;
                  margin-bottom: 30px;
              }
              .logo-icon {
                  font-size: 60px;
                  margin-bottom: 10px;
              }
              h1 {
                  text-align: center;
                  color: #1B4F72;
                  margin: 0 0 10px 0;
                  font-size: 24px;
              }
              .subtitle {
                  text-align: center;
                  color: #666;
                  margin-bottom: 30px;
              }
              input {
                  width: 100%;
                  padding: 15px;
                  margin-bottom: 15px;
                  border: 2px solid #ddd;
                  border-radius: 10px;
                  font-size: 16px;
                  box-sizing: border-box;
              }
              button {
                  width: 100%;
                  padding: 15px;
                  background: #27AE60;
                  color: white;
                  border: none;
                  border-radius: 10px;
                  font-size: 18px;
                  font-weight: bold;
                  cursor: pointer;
              }
          </style>
      </head>
      <body>
          <div class="login-box">
              <div class="logo">
                  <div class="logo-icon">🛢️</div>
                  <h1>Apex Oil Company, Inc.</h1>
                  <p class="subtitle">Investor Portal</p>
              </div>
              <form id="loginForm">
                  <input type="email" id="email" placeholder="Email Address" required>
                  <input type="password" id="password" placeholder="Password" required>
                  <button type="submit">Login to Dashboard</button>
              </form>
          </div>
          <script>
              document.getElementById('loginForm').addEventListener('submit', function(e) {
                  e.preventDefault();
                  localStorage.setItem('userEmail', document.getElementById('email').value);
                  localStorage.setItem('loggedIn', 'yes');
                  window.location.href = 'dashboard.html';
              });
          </script>
      </body>
      </html>
