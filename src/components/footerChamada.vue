<template>
  <footer>
    <div class="chamada">
      <h2>Aumente seus links hoje</h2>
      <button>Iniciar</button>
    </div>
    <div class="infos_div">
      <div class="infos_wrapper container">
        <img src="../assets/logo-branco.svg" alt="Shortly" />
        <div class="infos">
          <div class="infos_nav">
            <p>Características</p>
            <ul>
              <li><a href="#">Encurtamento de links</a></li>
              <li><a href="#">Links de marca</a></li>
              <li><a href="#">Análise</a></li>
            </ul>
          </div>

          <div class="infos_nav">
            <p>Recursos</p>
            <ul>
              <li><a href="#">Blog</a></li>
              <li><a href="#">Desenvolvedores</a></li>
              <li><a href="#">Suporte</a></li>
            </ul>
          </div>

          <div class="infos_nav">
            <p>Corporação</p>
            <ul>
              <li><a href="#">Sobre</a></li>
              <li><a href="#">Nosso time</a></li>
              <li><a href="#">Carreiras</a></li>
              <li><a href="#">Contato</a></li>
            </ul>
          </div>

          <ul class="redes">
            <li>
              <a href="#"
                ><img src="../assets/icon-facebook.svg" alt="Facebook"
              /></a>
            </li>
            <li>
              <a href="#"
                ><img src="../assets/icon-twitter.svg" alt="Twitter"
              /></a>
            </li>
            <li>
              <a href="#"
                ><img src="../assets/icon-pinterest.svg" alt="Pinterest"
              /></a>
            </li>
            <li>
              <a href="#"
                ><img src="../assets/icon-instagram.svg" alt="Instagram"
              /></a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style>
footer {
  background: #0b0c12;
  padding-bottom: 72px;
}
.chamada {
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 250px;
  background: #363b47;
  background-image: url("../assets/bg-boost-desktop.svg");
  background-size: cover;
  background-repeat: no-repeat;
}
.chamada h2 {
  font-weight: 700;
  font-size: 40px;
  letter-spacing: -0.025em;
  color: #f5f7fa;
  text-align: center;
}
.chamada button {
  display: inline-block;
  padding: 13px 40px;
  color: #f5f7fa;
  background: #18a0fb;
  transition: 0.2s;
  border-radius: 50px;
  font-weight: 700;
  font-size: 20px;
  letter-spacing: -0.01em;
  margin-top: 22px;
  border: none;
  cursor: pointer;
}
.chamada button:hover {
  background: #47b5ff;
}
.infos_div {
  padding: 0 20px;
  margin-top: 72px;
}
.infos_wrapper {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 30px;
}
.infos {
  display: flex;
  flex-wrap: wrap;
  gap: 78px;
}
.infos_nav {
}
.infos_nav ul {
  margin-top: 22px;
}
.infos_nav p {
  color: #f5f7fa;

  font-weight: 700;
  font-size: 16px;
  line-height: 32px;
  letter-spacing: -0.015em;
}
.infos_nav li + li {
  margin-top: 10px;
}
.infos_nav a {
  font-weight: 400;
  font-size: 16px;
  letter-spacing: -0.04em;
  color: #474d59;
  transition: 0.2s;
}
.infos_nav a:hover {
  color: #18a0fb;
}
.redes {
  display: flex;
  gap: 20px;
}
@media (max-width: 1021px) {
  .infos_wrapper {
    display: block;
    text-align: center;
  }
  .infos {
    justify-content: center;
    margin-top: 20px;
    text-align: left;
  }
}
@media (max-width: 636px) {
  .infos_nav {
    width: 100%;
    max-width: 166px;
  }
}
@media (max-width: 497px) {
  .infos {
    flex-direction: column;
    align-items: center;
    gap: 50px;
  }
  .infos_nav {
    width: auto;
    text-align: center;
  }
}
</style>
