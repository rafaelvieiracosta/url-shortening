<template>
  <section id="detalhesEstatisticas">
    <div class="detalhesEstatisticas_div container">
      <h2>Estatísticas Avançadas</h2>
      <p>
        Acompanhe o desempenho de seus links na web com nosso painel de
        estatísticas avançadas
      </p>

      <div class="caracteristicas">
        <div class="caracteristicas_item">
          <div class="icone">
            <img
              src="../assets/icon-brand-recognition.svg"
              alt="Ícone reconhecimento de marca"
            />
          </div>
          <h3>Análise de marca</h3>
          <p>
            Aumente o reconhecimento da sua marca a cada clique. Links genéricos
            não significam nada. Links de marca ajudam a incutir confiança.
          </p>
        </div>

        <div class="caracteristicas_item">
          <div class="icone">
            <img
              src="../assets/icon-detailed-records.svg"
              alt="Ícone Registros Detalhados"
            />
          </div>
          <h3>Registros Detalhados</h3>
          <p>
            Obtenha informações sobre quem está clicando em seus links. Saber
            quando e onde as pessoas se envolvem com seu conteúdo ajuda.
          </p>
        </div>

        <div class="caracteristicas_item">
          <div class="icone">
            <img
              src="../assets/icon-fully-customizable.svg"
              alt="Ícone Totalmente personalizável"
            />
          </div>
          <h3>Totalmente Alterável</h3>
          <p>
            Melhore o reconhecimento da marca e a descoberta de conteúdo por
            meio de links personalizáveis, aumentando o envolvimento do público.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
#detalhesEstatisticas {
  padding: 68px 20px 120px;
  background: #f5f7fa;
}
.detalhesEstatisticas_div > h2 {
  font-weight: 700;
  font-size: 40px;
  line-height: 60px;
  letter-spacing: -0.025em;
  text-align: center;
}
.detalhesEstatisticas_div > p {
  text-align: center;
  font-weight: 500;
  font-size: 18px;
  line-height: 32px;
  max-width: 50ch;
  margin: 0 auto;
  margin-top: 10px;
  color: #474d59;
}
.caracteristicas {
  margin-top: 98px;
  display: flex;
  gap: 30px;
  flex-wrap: wrap;
}
.caracteristicas_item:nth-child(2) {
  margin-top: 44px;
}
.caracteristicas_item:nth-child(3) {
  margin-top: 88px;
}
.caracteristicas_item {
  flex: 1 0 320px;
  padding: 76px 32px 40px;
  background: #fff;
  border-radius: 10px;
  position: relative;
  max-height: 267px;
}
.caracteristicas_item > h3 {
  font-weight: 700;
  font-size: 22px;
}
.caracteristicas_item > p {
  font-weight: 500;
  font-size: 16px;
  line-height: 26px;
  letter-spacing: -0.035em;
  color: #474d59;
}
.caracteristicas_item:nth-child(1)::before,
.caracteristicas_item:nth-child(2)::before {
  content: "";
  display: block;
  position: absolute;
  width: 30px;
  height: 8px;
  right: -30px;
  background: #18a0fb;
}
.caracteristicas_item:nth-child(1)::before {
  bottom: 107px;
}
.caracteristicas_item:nth-child(2)::before {
  bottom: 151px;
}
.icone {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 88px;
  height: 88px;
  border-radius: 50%;
  background: #0b0c12;
  position: absolute;
  top: -44px;
}
@media (max-width: 1076px) {
  .caracteristicas_item {
    max-height: initial;
  }
  .caracteristicas_item:nth-child(1)::before,
  .caracteristicas_item:nth-child(2)::before {
    display: none;
  }
  .caracteristicas_item:nth-child(2) {
    margin-top: 0;
  }
  .caracteristicas_item:nth-child(3) {
    margin-top: 0;
  }
  .caracteristicas {
    gap: 60px;
  }
}
@media (max-width: 400px) {
  .caracteristicas_item {
    flex: 1 0 200px;
  }
}
</style>
