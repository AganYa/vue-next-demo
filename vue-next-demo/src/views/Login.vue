<template>
  <div class="contanier">
    <div class="header">
      <span class="contact">联系妹子</span>
      <span>&nbsp;|&nbsp;</span>
      <span class="contact">企业注册</span>
    </div>

    <!-- 欢迎语 -->
    <div class="title">
      <h2>欢迎登录苏宁易购</h2>
    </div>

    <!-- 用户登录 -->
    <div class="userinfo">
      <div class="input_div">
        <input class="phone" placeholder="请输入手机号" type="text" />
      </div>

      <div class="input_div">
        <input class="password" placeholder="密码" type="password" />
      </div>

      <div class="login">
        <a href="#">登录</a>
      </div>
      <div class="sign_up">
        <a href="#">注册</a>
      </div>
    </div>

    <!-- 第三方登录 -->
    <div class="other_login">
      <p class="login_tip">其他登录方式</p>
      <div class="login_icon">
        <a>
          <img alt src="https://res.suning.cn/project/passport/login/wapV8/images/icon_qq.png" />
        </a>
        <a>
          <img alt src="https://res.suning.cn/project/passport/login/wapV8/images/icon_epp.png" />
        </a>
        <a>
          <img alt src="https://res.suning.cn/project/passport/login/wapV8/images/icon_k.png" />
        </a>
      </div>

      <div class="login_agree">
        <span>我同意</span>
        <b>《</b>
        <a href="https://sale.suning.com/all/regProtocol/snyghyzc.html">苏宁易购会员章程</a>
        <b>》</b>
        <b>《</b>
        <a href="https://sale.suning.com/all/regProtocol/yfbxy.html">易付宝协议</a>
        <b>》</b>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang='less' scoped>
@baseFontSize: 50;
.contanier {
  width: 750rem / @baseFontSize;

  .header {
    text-align: right;
    font-size: 24rem / @baseFontSize;
    margin-bottom: 50rem / @baseFontSize;
    padding: 10rem / @baseFontSize 12rem / @baseFontSize;
  }

  .title {
    padding: 0 37.5rem / @baseFontSize;
    h2 {
      font-size: 36rem / @baseFontSize;
      font-weight: 400;
    }
  }

  .userinfo {
    padding: 0 80rem / @baseFontSize;
    .input_div {
      width: 12rem;
      height: 1.8rem;
      line-height: 1.8rem;
      margin-top: 0.6rem;
      border-bottom: 1px solid #ddd;
      position: relative;
      input {
        border: 0;
        color: #fa0;
        outline: none;
        height: 1.34rem;
        font-size: 0.7rem;
        &::placeholder {
          height: 1.34rem;
          line-height: 1rem;
          position: absolute;
          left: 0.46rem;
          top: 0.5rem;
          font-size: 0.6rem;
          color: #ccc;
          background: transparent;
          cursor: text;
        }
      }
    }

    .login {
      margin-top: 1.2rem;
      text-align: center;
      a {
        width: 12rem;
        height: 1.8rem;
        line-height: 1.8rem;
        display: block;
        color: #222;
        font-size: 0.68rem;
        border-radius: 0.36rem;
        background: #fc0;
        font-weight: 600;
      }
    }

    .sign_up {
      text-align: center;
      a {
        color: #333;
        display: inline-block;
        margin-top: 0.84rem;
        font-size: 0.6rem;
      }
    }
  }

  .other_login {
    margin-top: 200rem / @baseFontSize;

    .login_tip {
      font-size: 0.5rem;
      text-align: center;
      color: #999;
      position: relative;
      margin-bottom: 0.38rem;
      &::before {
        content: '';
        display: block;
        position: absolute;
        left: 120rem / @baseFontSize;
        top: 0.28rem;
        width: 3rem;
        border-bottom: 1px solid #ddd;
      }
      &::after {
        content: '';
        display: block;
        position: absolute;
        top: 0.28rem;
        right: 120rem / @baseFontSize;
        width: 3rem;
        border-bottom: 1px solid #ddd;
      }
    }

    .login_icon {
      display: flex;
      justify-content: space-around;
      padding: 0 0.6rem;
      a {
        display: inline-block;
        width: 1.32rem;
        height: 1.32rem;
        // margin-right: 2rem;
        img {
          width: 1.32rem;
          height: 1.32rem;
        }
      }
    }
    .login_agree {
      display: flex;
      justify-content: center;
      margin: 0.7rem;
      color: #999;
      text-align: left;
      font-size: 0.4rem;
      a {
        color: #101010;
        text-decoration: underline;
      }
    }
  }
}
</style>