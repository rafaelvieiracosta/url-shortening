<template>
  <section>
    <div class="inputBusca_div">
      <div class="inputBusca container">
        <input
          type="text"
          name="link"
          id="link"
          placeholder="Encurte um link aqui"
        />
        <span class="error">Por favor adicione um link</span>
        <button>Encurte!</button>
      </div>
    </div>
    <div class="resultadoBusca_div">
      <div class="resultadoBusca container">
        <div class="resultadoBusca_item">
          <p>https://www.frontendmentor.io</p>
          <div>
            <p>https://rel.ink/k4lKyk</p>
            <button>Copiar</button>
          </div>
        </div>
        <div class="resultadoBusca_item">
          <p>https://www.frontendmentor.io</p>
          <div>
            <p>https://rel.ink/k4lKyk</p>
            <button>Copiar!</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.error {
  display: none;
}
.inputBusca_div {
  margin-top: 68px;
  padding: 0 20px;
  background: linear-gradient(180deg, #fff 50%, #f5f7fa 50%);
}
.inputBusca {
  background: #363b47;
  padding: 52px 64px;
  display: flex;
  justify-content: space-between;
  gap: 24px;
  border-radius: 10px;
  background-image: url("../assets/bg-shorten-desktop.svg");
  background-size: cover;
  background-repeat: no-repeat;
}
.inputBusca input {
  flex: 1;
  padding: 16px 30px 14px;
  border: 2px solid #fff;
  outline: none;
  border-radius: 8px;
  font-weight: 500;
  font-size: 20px;
  transition: 0.2s;
}
.inputBusca input:focus {
  border-color: #18a0fb;
}
.inputBusca button {
  border: none;
  border-radius: 10px;
  font-weight: 700;
  font-size: 20px;
  padding: 17px 44px;
  color: #f5f7fa;
  background: #18a0fb;
  transition: 0.2s;
  cursor: pointer;
}
.inputBusca button:hover {
  background: #47b5ff;
}
.resultadoBusca_div {
  background: #f5f7fa;
  padding: 0 20px;
  padding-bottom: 50px;
}
.resultadoBusca {
  padding-top: 24px;
}
.resultadoBusca_item {
  background: #fff;
  border-radius: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-weight: 500;
  font-size: 20px;
}
.resultadoBusca_item > p {
  padding: 24px 0 20px;
  padding-left: 32px;
}
.resultadoBusca_item div {
  display: flex;
  align-items: center;
  gap: 24px;
  padding: 24px 0 20px;
  padding-right: 32px;
}
.resultadoBusca_item div > p {
  color: #18a0fb;
}
.resultadoBusca_item + .resultadoBusca_item {
  margin-top: 16px;
}
.resultadoBusca_item div button {
  padding: 8px 0;
  text-align: center;
  font-weight: 700;
  font-size: 16px;
  letter-spacing: -0.065em;
  border-radius: 5px;
  border: none;
  background: #18a0fb;
  cursor: pointer;
  transition: 0.2s;
  color: #f5f7fa;
  min-width: 113px;
}
.resultadoBusca_item div button:hover {
  background: #47b5ff;
}
@media (max-width: 800px) {
  .inputBusca {
    flex-wrap: wrap;
    gap: 30px;
  }
  .inputBusca button {
    flex: 1;
  }
}
@media (max-width: 776px) {
  .resultadoBusca_item {
    flex-direction: column;
    align-items: initial;
    font-size: 16px;
  }
  .resultadoBusca_item > p {
    padding: 12px 16px;
  }
  .resultadoBusca_item div {
    flex-direction: column;
    align-items: initial;
    border-top: 1px solid #e5e5e5;
    padding: 12px 16px;
    gap: 12px;
  }
  .resultadoBusca_item div button {
    letter-spacing: -0.025em;
  }
}
@media (max-width: 550px) {
  .inputBusca {
    padding: 24px;
  }
  .inputBusca input {
    font-size: 16px;
    padding: 8px 16px;
    min-width: 100px;
  }
  .inputBusca button {
    font-size: 18px;
    padding: 10px 44px;
  }
}
</style>
