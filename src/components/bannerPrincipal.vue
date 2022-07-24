<template>
  <main>
    <div class="main_div container">
      <div class="main_titulos">
        <h1>Mais que apenas links curtos</h1>
        <p>
          Construa o reconhecimento da sua marca e obtenha informações sobre o
          desempenho dos seus links
        </p>
        <a href="#">Iniciar</a>
      </div>
      <div class="main_banner">
        <img
          src="../assets/illustration-working.svg"
          alt="Pessoa trabalhando em um computador"
        />
      </div>
    </div>
  </main>
</template>

<script>
export default {};
</script>

<style>
main {
  padding: 0 20px;
  margin-top: 30px;
}
.main_div {
  display: grid;
  grid-template-columns: 1fr 445px;
}
.main_titulos {
  align-self: center;
}
.main_titulos h1 {
  font-size: 80px;
  line-height: 113%;
  letter-spacing: -0.03em;
}
.main_titulos p {
  font-weight: 500;
  font-size: 22px;
  line-height: 163%;
}
.main_titulos a {
  display: inline-block;
  margin-top: 36px;
  font-weight: 700;
  font-size: 20px;
  padding: 13px 40px;
  color: #f5f7fa;
  background: #18a0fb;
  transition: 0.2s;
  border-radius: 50px;
}
.main_titulos a:hover {
  background: #47b5ff;
}
.main_banner {
  position: relative;
  height: 482px;
}
.main_banner img {
  position: absolute;
}
@media (max-width: 941px) {
  .main_titulos h1 {
    font-size: 42px;
    line-height: 48px;
    letter-spacing: -0.03em;
  }
  .main_titulos p {
    font-size: 18px;
    line-height: 30px;
  }
  .main_titulos a {
    margin-top: 30px;
  }
}
@media (max-width: 800px) {
  .main_div {
    grid-template-columns: 1fr;
  }
  .main_banner {
    grid-row: 1;
    width: 200px;
  }
  .main_titulos {
    margin-top: 32px;
    text-align: center;
  }
}
</style>
