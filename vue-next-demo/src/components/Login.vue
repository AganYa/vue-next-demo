<template>
  <div class="contanier">
    <div class="login_wrapper">
      <div class="header">Login</div>
      <div class="form_wrapper">
        <input class="input_item" name="username" placeholder="username" type="text" />
        <input class="input_item" name="password" placeholder="password" type="password" />
        <div @click="onClickLogin" class="login_btn">Login</div>
      </div>
      <div class="sign">
        还没有账号？点击我注册
        <a href="#">Sign Up</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    onClickLogin() {
      this.$router.push('/home');
    }
  }
};
</script>
<style lang='less' scoped>
@baseFontSize: 50;
.contanier {
  height: 100%;
  background-image: linear-gradient(to right, #a8edea, #fed6e3);

  .login_wrapper {
    background-color: #fff;
    width: 500rem / @baseFontSize;
    height: 1000rem / @baseFontSize;
    padding: 0 100rem / @baseFontSize;
    border-radius: 30rem / @baseFontSize;
    position: absolute;
    left: 50%;
    top: 50%;
    z-index: 2;
    transform: translate(-50%, -50%);

    .header {
      font-size: 60rem / @baseFontSize;
      font-weight: bold;
      text-align: center;
      line-height: 400rem / @baseFontSize;
    }
    .form_wrapper {
      .input_item {
        display: block;
        width: 100%;
        margin-bottom: 40rem / @baseFontSize;
        border: 0;
        padding: 20rem / @baseFontSize;
        border-bottom: 1px solid rgb(128, 125, 125);
        font-size: 30rem / @baseFontSize;
        outline: none;
        &::placeholder {
          text-transform: uppercase;
        }
      }

      .login_btn {
        text-align: center;
        padding: 20rem / @baseFontSize;
        width: 100%;
        margin-top: 80rem / @baseFontSize;
        color: #fff;
        background-image: linear-gradient(to right, #fddb92, #d1fdff);
      }
    }

    .sign {
      width: 540rem / @baseFontSize;
      text-align: center;
      line-height: 160rem / @baseFontSize;
      font-size: 30rem / @baseFontSize;

      a {
        text-decoration-line: none;
        color: #a6c1ee;
      }
    }
  }
}
</style>