from pathlib import Path

# HTML content with blue theme + music
html_content = """
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Para Danilo</title>
  <style>
    body {
      background-color: #1e1e1e;
      color: #d4d4d4;
      font-family: "Courier New", Courier, monospace;
      padding: 40px;
      text-align: center;
    }
    .code-box {
      background-color: #252526;
      padding: 20px;
      border-radius: 12px;
      max-width: 600px;
      margin: 0 auto 20px;
      text-align: left;
      white-space: pre-wrap;
      box-shadow: 0 0 15px rgba(100, 149, 237, 0.3);
      color: #87cefa;
    }
    .btn {
      background-color: #4682b4;
      color: #fff;
      border: none;
      padding: 12px 24px;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 20px;
      transition: background-color 0.3s ease;
    }
    .btn:hover {
      background-color: #4169e1;
    }
    .hidden-message {
      display: none;
      margin-top: 30px;
      font-size: 18px;
      color: #00bfff;
      animation: fadeIn 1s ease-in-out forwards;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>

  <h1>Para: Danilo</h1>

  <div class="code-box">
<code>
class Amor:
    def __init__(self, nome):
        self.nome = nome
        self.amor = "infinito"
    
    def declarar(self):
        return f"Danilo, eu te amo para sempre."

meu_amor = Amor("Danilo")
print(meu_amor.declarar())
</code>
  </div>

  <button class="btn" onclick="mostrarMensagem()">Clique aqui</button>

  <div class="hidden-message" id="mensagem">
    Danilo, meu amor por você é como um loop infinito: nunca para, nunca falha.  
    Você é o código mais precioso da minha vida.
  </div>

  <audio autoplay loop>
    <source src="https://cdn.pixabay.com/audio/2023/03/20/audio_5a3aa05f7b.mp3" type="audio/mpeg">
    Seu navegador não suporta áudio.
  </audio>

  <script>
    function mostrarMensagem() {
      document.getElementById("mensagem").style.display = "block";
    }
  </script>

</body>
</html>
"""

# Save updated HTML with music
output_path = Path("/mnt/data/para_danilo_com_musica.html")
output_path.write_text(html_content, encoding="utf-8")

output_path.name
