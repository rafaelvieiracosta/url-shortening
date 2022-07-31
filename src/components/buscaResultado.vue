<template>
  <section>
    <div class="inputBusca_div">
      <div class="inputBusca container">
        <div class="inputBusca-input">
          <input
            type="text"
            name="link"
            id="link"
            placeholder="Encurte um link aqui"
            v-model="urlNormal"
            @click="removeErrorStyle"
          />
          <span>Por favor, adicione um link</span>
        </div>
        <button @click="encurtarLink">Encurte!</button>
      </div>
    </div>
    <div class="resultadoBusca_div">
      <div class="resultadoBusca container">
        <div
          class="resultadoBusca_item"
          v-for="(url, index) in urlHistory"
          :key="index"
        >
          <p>{{ url.urlAfter }}</p>
          <div>
            <a :href="`https://${url.urlBefore}`" target="_blank">{{
              url.urlBefore
            }}</a>
            <button @click="copyUrl">Copiar</button>
          </div>
        </div>

        <div class="resultadoBusca_item">
          <p>https://www.frontendmentor.io</p>
          <div>
            <a href="https://shrtco.de/Hvxdcp" target="_blank"
              >shrtco.de/Hvxdcp</a
            >
            <button @click="copyUrl">Copiar!</button>
          </div>
        </div>

        <div class="resultadoBusca_item">
          <p>https://twitter.com/frontendmentor</p>
          <div>
            <a href="https://shrtco.de/JLnLHY" target="_blank"
              >shrtco.de/JLnLHY</a
            >
            <button @click="copyUrl">Copiar!</button>
          </div>
        </div>
        <div class="resultadoBusca_item">
          <p>https://www.linkedin.com/company/frontend-mentor/</p>
          <div>
            <a href="https://www.linkedin.com/company/frontend-mentor/"
              >shrtco.de/POdrLH</a
            >
            <button @click="copyUrl">Copiar!</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      urlNormal: "",
      urlHistory: [],
    };
  },
  methods: {
    encurtarLink() {
      const regex =
        // eslint-disable-next-line no-useless-escape
        /[(http(s)?):\/\/(www\.)?a-zA-Z0-9@:%._\+~#=]{2,256}\.[a-z]{2,6}\b([-a-zA-Z0-9@:%_\+.~#?&//=]*)/gi;

      const isUrl = regex.test(this.urlNormal);

      if (isUrl) {
        fetch(`https://api.shrtco.de/v2/shorten?url=${this.urlNormal}`)
          .then((r) => r.json())
          .then((r) => {
            this.urlHistory.unshift({
              urlAfter: this.urlNormal,
              urlBefore: r.result.short_link,
            });
          });
      } else {
        const inputDiv = document.querySelector(".inputBusca-input");
        inputDiv.classList.add("error");
      }
    },
    removeErrorStyle() {
      const inputDiv = document.querySelector(".inputBusca-input");
      if (inputDiv.classList.contains("error"))
        inputDiv.classList.remove("error");
    },
    copyUrl(event) {
      const aLink = event.target.parentElement.querySelector("a").innerText;

      var copyTextarea = document.createElement("textarea");
      copyTextarea.style.position = "fixed";
      copyTextarea.style.opacity = "0";
      copyTextarea.textContent = aLink;

      document.body.appendChild(copyTextarea);
      copyTextarea.select();
      document.execCommand("copy");
      document.body.removeChild(copyTextarea);
    },
  },
};
</script>

<style>
.inputBusca_div {
  margin-top: 68px;
  padding: 0 20px;
  background: linear-gradient(180deg, #fff 50%, #e6eaf0 50%);
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
.inputBusca-input {
  flex: 1;
  position: relative;
}
.inputBusca-input span {
  display: none;
  font-style: italic;
  font-weight: 500;
  font-size: 15px;
  letter-spacing: 0.015em;
  color: #f46262;
  position: absolute;
  left: 0;
  bottom: -30px;
}
.inputBusca input {
  width: 100%;
  padding: 16px 30px 14px;
  border: 2px solid #fff;
  outline: none;
  border-radius: 8px;
  font-weight: 500;
  font-size: 20px;
  transition: 0.2s;
}
.inputBusca-input.error input {
  border: 2px solid #f46262;
  color: #f46262;
}
.inputBusca-input.error input::placeholder {
  color: #f46262;
}
.inputBusca-input.error span {
  display: block;
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
  background: #e6eaf0;
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
  gap: 15px;
}
.resultadoBusca_item > p {
  padding: 16px 0;
  padding-left: 32px;
  word-break: break-all;
}
.resultadoBusca_item div {
  display: flex;
  align-items: center;
  gap: 24px;
  padding: 16px 0;
  padding-right: 26px;
}
.resultadoBusca_item div > a {
  color: #18a0fb;
}
.resultadoBusca_item div > a:hover {
  text-decoration: underline;
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
    padding: 34px;
  }
  .inputBusca-input span {
    bottom: -23px;
  }
}
@media (max-width: 776px) {
  .resultadoBusca_item {
    flex-direction: column;
    align-items: initial;
    font-size: 16px;
    gap: initial;
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
@media (max-width: 625px) {
  .inputBusca input,
  .inputBusca button {
    width: 100%;
  }
}
@media (max-width: 550px) {
  .inputBusca button {
    font-size: 18px;
    padding: 10px 44px;
  }
  .inputBusca input {
    font-size: 16px;
    padding: 8px 16px;
    min-width: 100px;
  }
}
</style>
