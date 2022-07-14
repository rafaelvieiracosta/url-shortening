<template>
  <header>
    <div class="header_div container open">
      <img src="../assets/logo.svg" alt="Shortly" />
      <div class="header_mobile" @click="toggleMenuMobile">
        <span></span>
        <span></span>
        <span></span>
      </div>
      <div class="header_links">
        <ul class="pages">
          <li><a href="#">Features</a></li>
          <li><a href="#">Pricing</a></li>
          <li><a href="#">Resources</a></li>
        </ul>

        <div class="login">
          <a href="#">Login</a>
          <a href="#">Sign Up</a>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "App",
  data() {
    return {};
  },
  methods: {
    toggleMenuMobile() {
      document.querySelector(".header_div").classList.toggle("open");
    },
  },
};
</script>

<style>
.header_div {
  display: flex;
  gap: 44px;
  padding: 48px 0;
  position: relative;
}
.header_links {
  flex: 1;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.header_mobile {
  display: none;
  cursor: pointer;
}
.pages {
  display: flex;
  gap: 30px;
}
.login a,
.pages a {
  font-weight: 700;
  font-size: 15px;
  color: #989ea6;
  transition: 0.2s;
}
.login a:hover,
.pages a:hover {
  color: #0b0c12;
}
.login {
  display: flex;
  gap: 36px;
  align-items: center;
}
.login a:last-child {
  color: #f5f7fa;
  background: #18a0fb;
  padding: 8px 24px;
  border-radius: 30px;
  transition: 0.2s;
}
.login a:last-child:hover {
  background: #47b5ff;
}
@media (max-width: 800px) {
  .header_div {
    align-items: center;
    justify-content: space-between;
  }
  .header_links {
    display: none;
  }
  .header_div.open .header_links {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 111px;
    width: 100%;
    background: #242833;
    border-radius: 10px;
    padding: 40px 24px;
  }
  .login a,
  .pages a {
    font-size: 18px;
    color: #f5f7fa;
  }
  .login a:hover,
  .pages a:hover {
    color: #f5f7fa;
  }
  .pages {
    flex-direction: column;
    align-items: center;
  }
  .login {
    margin-top: 30px;
    padding-top: 30px;
    flex-direction: column;
    border-top: 1px solid #989ea623;
    width: 100%;
    gap: 24px;
  }
  .login a {
    width: 100%;
    text-align: center;
  }
  .login a:last-child {
    padding: 10px 24px;
  }
  .header_mobile {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 24px;
    height: 21px;
  }
  .header_div.open .header_mobile {
    justify-content: center;
  }
  .header_mobile span {
    height: 3px;
    width: 100%;
    background: #989ea6;
  }
  .header_div.open .header_mobile span {
    position: absolute;
  }
}
</style>
