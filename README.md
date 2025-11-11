<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>#Lámpara Inteligente Gamer</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom, 
        #F7E7CE 0%, 
        #F7E7CE 45%, 
        #3a3a3a 45%,
        #2d2d2d 55%,
        #1a1a1a 65%,
        #0d0d0d 75%,
        #000000 85%,
        #1a1a1a 100%);
      color: white;
      margin: 0;
      padding: 0;
      min-height: 100vh;
    }
    header {
      background: #000000;
      padding: 20px;
      text-align: center;
      font-size: 1.8rem;
      font-weight: bold;
      color: #00eaff;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.5);
      position: relative;
    }
    header::before,
    header::after {
      content: '';
      position: absolute;
      top: 0;
      width: 150px;
      height: 100%;
      background-image: url('lampara1.jpg');
      background-size: cover;
      background-position: center;
      opacity: 0.3;
      filter: blur(2px);
    }
    header::before {
      left: 0;
    }
    header::after {
      right: 0;
    }
    .container {
      padding: 20px;
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }
    .product {
      background: #1a1a1a;
      padding: 15px;
      border-radius: 10px;
      width: 320px;
    }
    .stars {
      font-size: 0.9rem;
      color: gold;
      cursor: pointer;
    }
    .image-box {
      width: 100%;
      height: 200px;
      background: #2f2f2f;
      border: 2px dashed #555;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #777;
      font-size: 0.9rem;
      margin-bottom: 10px;
    }
    button {
      width: 100%;
      padding: 10px;
      background: #00eaff;
      border: none;
      color: black;
      font-weight: bold;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover { background: #02b5c7; }
    .eco-box {
      margin-top: 30px;
      background: #1a1a1a;
      padding: 15px;
      border-radius: 10px;
      text-align: center;
    }
    .eco-img {
      width: 100px;
      margin-bottom: 10px;
    }
    footer {
      text-align: center;
      margin-top: 20px;
      padding: 10px;
      color: #ccc;
      font-size: 0.8rem;
    }
  </style>
</head>
<body>
  <header>Lámpara Inteligente Gamer RGB</header>
  <div class="container">
    <div class="product">
      <div class="stars" onclick="document.getElementById('comentarios').style.display='block'">★★★★★ 4.5 / 5</div>
      <h2>Lámpara RGB Gamer</h2>
      <p>Cambia de color con la música. Perfecta para gamers y cuartos modernos. Luz suave y colores vivos.</p>
      <img src="lampara1.jpg" width="300" height="200" />
      <p><b>Precio:</b> $180.900 COP</p>
      <button>Comprar Ahora</button>
    </div>
  </div>
  <div id="comentarios" style="display:none; padding: 40px 20px; background: #2a2a2a;">
    <div style="max-width: 800px; margin: 0 auto;">
      <h3 style="text-align: center; color: #00eaff;">Comentarios de Clientes</h3>
      <div style="background: #1a1a1a; padding: 15px; border-radius: 10px; margin-bottom: 20px;">
        <p style="margin: 10px 0;">⭐️⭐️⭐️⭐️⭐️ "Muy bonita, hace mi cuarto gamer super cool"</p>
        <p style="margin: 10px 0;">⭐️⭐️⭐️⭐️ "Brilla muy bien y cambia con la música, la amo"</p>
        <p style="margin: 10px 0;">⭐️⭐️⭐️⭐️⭐️ "No gasta mucha energía y se ve genial"</p>
      </div>
      
      <div style="background: #1a1a1a; padding: 20px; border-radius: 10px;">
        <h4 style="color: #00eaff; margin-top: 0;">Deja tu comentario</h4>
        <form id="formComentario" style="display: flex; flex-direction: column; gap: 15px;">
          <div>
            <label style="display: block; margin-bottom: 5px; color: #ccc;">Nombre:</label>
            <input type="text" id="nombre" placeholder="Tu nombre" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid #555; background: #2a2a2a; color: white;" required />
          </div>
          
          <div>
            <label style="display: block; margin-bottom: 5px; color: #ccc;">Calificación:</label>
            <select id="calificacion" style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid #555; background: #2a2a2a; color: white;" required>
              <option value="">Selecciona...</option>
              <option value="5">⭐️⭐️⭐️⭐️⭐️ (5 estrellas)</option>
              <option value="4">⭐️⭐️⭐️⭐️ (4 estrellas)</option>
              <option value="3">⭐️⭐️⭐️ (3 estrellas)</option>
              <option value="2">⭐️⭐️ (2 estrellas)</option>
              <option value="1">⭐️ (1 estrella)</option>
            </select>
          </div>
          
          <div>
            <label style="display: block; margin-bottom: 5px; color: #ccc;">Comentario:</label>
            <textarea id="comentarioTexto" placeholder="Escribe tu opinión sobre el producto..." style="width: 100%; padding: 10px; border-radius: 5px; border: 1px solid #555; background: #2a2a2a; color: white; min-height: 100px; resize: vertical;" required></textarea>
          </div>
          
          <button type="submit" style="width: 100%; padding: 12px; background: #00eaff; border: none; color: black; font-weight: bold; border-radius: 5px; cursor: pointer;">
            Publicar Comentario
          </button>
        </form>
        <div id="mensajeExito" style="display: none; margin-top: 15px; padding: 10px; background: #00eaff; color: black; border-radius: 5px; text-align: center; font-weight: bold;">
          ¡Gracias por tu comentario!
        </div>
      </div>
    </div>
  </div>

  <script>
    document.getElementById('formComentario').addEventListener('submit', function(e) {
      e.preventDefault();
      const nombre = document.getElementById('nombre').value;
      const calificacion = document.getElementById('calificacion').value;
      const comentario = document.getElementById('comentarioTexto').value;
      
      // Mostrar mensaje de éxito
      document.getElementById('mensajeExito').style.display = 'block';
      
      // Limpiar formulario
      this.reset();
      
      // Ocultar mensaje después de 3 segundos
      setTimeout(() => {
        document.getElementById('mensajeExito').style.display = 'none';
      }, 3000);
    });
  </script>
  <div class="eco-box">
    <img src= logo1.jpg width="100" height="100" />
    <p>Esta lámpara cuida el planeta. Es de bajo consumo y tiene certificación Eco+.</p>
  </div>
  <footer>
    Laura Sofía Chacón • Carlos Gómez • Miguel Hernández • Karol Riaño • Cesar Santiago Guasca • Beiker Nivia • Matías Toscano
  <div style="margin-top:40px;text-align:center;">
  <h2>Próximamente</h2>
  <img src="lampara2.jpg" width="400" height="400" />
</div>
</footer>
</body>
</html>
