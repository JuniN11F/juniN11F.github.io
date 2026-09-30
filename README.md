
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Sistema do Amor ❤️</title>

<style>
* {
  box-sizing: border-box;
}

body {
  background: #160d1b;
  color: white;
  font-family: monospace;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  margin: 0;
  padding: 20px;
}

main {
  background: #24172c;
  border: 2px solid #ff5ca8;
  border-radius: 20px;
  padding: 28px;
  width: 100%;
  max-width: 430px;
  text-align: center;
  box-shadow: 0 0 25px #ff5ca833;
}

h1 {
  color: #ff80bd;
  font-size: 25px;
}

.descricao {
  color: #d6c6dd;
  line-height: 1.6;
  font-size: 14px;
}

label {
  display: block;
  text-align: left;
  margin-top: 16px;
  color: #ffb3d6;
}

input, select, button {
  width: 100%;
  padding: 12px;
  margin-top: 8px;
  border-radius: 9px;
  font-family: inherit;
  font-size: 14px;
}

input, select {
  background: #35243e;
  color: white;
  border: 1px solid #68456f;
}

button {
  margin-top: 22px;
  background: #ff5ca8;
  color: #260b1b;
  border: none;
  font-weight: bold;
  cursor: pointer;
  transition: 0.2s;
}

button:hover {
  transform: scale(1.03);
  background: #ff8bc2;
}

#resultado {
  display: none;
  margin-top: 24px;
  padding: 15px;
  background: #1a1120;
  border-radius: 12px;
  border: 1px solid #754263;
  animation: aparecer 0.6s ease;
}

#resultado h2 {
  color: #ff80bd;
  font-size: 24px;
  line-height: 1.4;
}

.pequeno {
  color: #c9b9d0;
  font-size: 12px;
  line-height: 1.6;
}

.erro {
  color: #ff6d9f;
  font-size: 13px;
  font-weight: bold;
}

@keyframes aparecer {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
</head>

<body>

<main>
  <div style="font-size:38px">💘</div>

  <h1>Sistema do Amor.exe</h1>

  <p class="descricao">
    Responda às perguntas abaixo para descobrir
    uma informação extremamente importante.
  </p>

  <form id="formulario">

    <label for="nome">Qual é o seu nome?</label>
    <input
      id="nome"
      type="text"
      placeholder="Digite seu nome..."
      required
    >

    <label for="data">Qual é a data de hoje?</label>
    <input
      id="data"
      type="date"
      required
    >

    <label for="time">Qual é o time do seu coração?</label>
    <select id="time">
      <option>Flamengo</option>
      <option>Vasco</option>
      <option>Fluminense</option>
      <option>Botafogo</option>
      <option>Corinthians</option>
      <option>Palmeiras</option>
      <option>São Paulo</option>
      <option>Outro time</option>
      <option>Não gosto de futebol</option>
    </select>

    <label for="amor">Você ama o Fernando?</label>
    <select id="amor">
      <option>Sim, muito!</option>
      <option>Mais ou menos...</option>
      <option>Não vou responder 😏</option>
    </select>

    <button type="submit">
      DESCOBRIR RESULTADO 🔎
    </button>

  </form>

  <section id="resultado" aria-live="polite"></section>
</main>

<script>
const formulario = document.getElementById("formulario");
const resultado = document.getElementById("resultado");

formulario.addEventListener("submit", function(event) {
  event.preventDefault();

  resultado.style.display = "block";

  resultado.innerHTML = `
    <p class="pequeno">Analisando respostas...</p>

    <p class="erro">
      ⚠️ ERRO 404: resposta alternativa não encontrada.
    </p>

    <h2>Flávia, eu te amo muito ❤️</h2>

    <p class="pequeno">
      Não importa o que você respondeu.<br>
      O sistema já tinha decidido KKKKK 😂
    </p>

    <p class="pequeno">— Fernando 💗</p>
  `;

  formulario.style.display = "none";

  resultado.scrollIntoView({
    behavior: "smooth",
    block: "center"
  });
});
</script>

</body>
</html>
