<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Stepwyrd – Passwort zurücksetzen</title>
  <style>
    body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; background: #1a1a2e; color: #eee; margin: 0; padding: 24px; min-height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; box-sizing: border-box; }
    h1 { font-size: 1.25rem; margin-bottom: 8px; }
    p { color: #aaa; text-align: center; margin-bottom: 24px; }
    a { display: inline-block; background: #e94560; color: #fff; padding: 14px 24px; border-radius: 12px; text-decoration: none; font-weight: 600; }
    a:hover { opacity: 0.9; }
  </style>
</head>
<body>
  <h1>Passwort zurücksetzen</h1>
  <p>Tippe auf den Button, um die Stepwyrd-App zu öffnen und dein neues Passwort festzulegen.</p>
  <a href="#" id="open-app">App öffnen</a>
  <script>
    (function () {
      var hash = window.location.hash || '';
      var appUrl = 'stepwyrd://reset-password' + hash;
      var link = document.getElementById('open-app');
      link.href = appUrl;
      // Optional: einmal automatisch versuchen (funktioniert nicht in allen Browsern)
      setTimeout(function () {
        try { window.location.href = appUrl; } catch (e) {}
      }, 500);
    })();
  </script>
</body>
</html>
