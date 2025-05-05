<!DOCTYPE html>
<html>
<head>
  <title>Hola!</title>
  <script>
    let contador = 0;
    function spam() {
      for (let i = 0; i < 100000; i++) {
        let nuevaVentana = window.open("", "", "width=200,height=100");
        if (nuevaVentana) {
          nuevaVentana.document.write("<h1>Hola</h1>");
          nuevaVentana.document.title = "Hola " + (i + 1);
        } else {
          alert("El navegador bloqueó las ventanas emergentes.");
          break;
        }
      }
    }
    window.onload = spam;
  </script>
</head>
<body>
  <h1>¡Preparate!</h1>
</body>
</html>
