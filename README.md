<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sign Up - PFKahoot!</title>
  <link rel="icon" type="image/png" href="favicon.png">
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gradient-to-br from-blue-900 to-white min-h-screen flex items-center justify-center p-4">
  <div class="bg-white rounded-2xl shadow-lg p-6 w-full max-w-md">
    <h1 class="text-3xl font-bold text-center text-blue-700 mb-6">Create Your Account</h1>

    <form onsubmit="signup(event)" class="space-y-4">
      <input type="text" id="username" placeholder="Username" class="w-full px-4 py-2 border rounded" required>
      <input type="email" id="email" placeholder="E-mail Address" class="w-full px-4 py-2 border rounded" required>
      <input type="password" id="password" placeholder="Password" class="w-full px-4 py-2 border rounded" required>
      <input type="password" id="confirmPassword" placeholder="Confirm Password" class="w-full px-4 py-2 border rounded" required>
      <button type="submit" class="w-full bg-blue-600 text-white py-2 rounded hover:bg-blue-700">Sign up</button>
    </form>

    <p class="text-center text-sm mt-4">
      Already have an account?
      <a href="index.html" class="text-blue-600">Sign in</a>
    </p>
  </div>

  <script>
    function signup(e) {
      e.preventDefault();
      const username = document.getElementById('username').value;
      const email = document.getElementById('email').value;
      const password = document.getElementById('password').value;
      const confirmPassword = document.getElementById('confirmPassword').value;

      if (password !== confirmPassword) {
        alert("Passwords do not match!");
        return;
      }

      alert(`Account created for ${username} (${email})!`);
      // Redirection ou enregistrement backend ici
    }
  </script>
</body>
</html>
