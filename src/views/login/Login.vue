<template>
  <div id="login">
    <div class="login-body">
      <img src="~assets/images/Equipment.png" class="login-header-img">
      <div class="login-box">
        <div class="login-earth" style="top: -8px">
          <div class="login-earth-contaner"></div>
          <div class="login-earth-slogan">
            <div class="login-earth-slogan-text login-earth-slogan-title">
              <p>医疗设备</p>
              <p>全生命周期管理系统</p>
            </div>
            <div class="login-earth-slogan-text login-earth-slogan-subtitle">
                <span>专注</span>
                <span>专业</span>
                <span>专用</span>
            </div>
          </div>
          <div class="login-from" style="top: 50px;">
            <div class="login_logo">
                <a href="javascrtipt:;">
                    <img src="~assets/images/userTow.png"></a>
            </div>
            <div class="login_name">
                <p>众联设备管理系统</p>
                <h4 id="version">版本号：5.2.3</h4>
            </div>
            <div class="login-from-item">
                <input name="user" id="user" required="" lay-verify="required" type="text" placeholder="用户名" autocomplete="on" onkeyup="WidthCheck(this,6);">
            </div>
            <div class="login-from-item">
                <input type="password" id="password" name="user_pwd" required="" lay-verify="required|password" placeholder="密码">
                <span class="show-pwd"></span>
            </div>
            <div class="login-action-line">
                <input value="立即登陆" style="width: 100%;" type="submit" id="LoginBtn">
            </div>

            <p id="message"></p>
          </div>
        </div>
      </div>
      <div class="login-footer">
        <div class="login-footer-body">
          <div class="login-footer-text login-footer-left"><a href="http://www.zlianyx.com/ " target="blank" id="azlyx">深圳市众联医信科技有限公司</a> 版权所有 ©2017-2019 技术支持电话：0755-84820386 189 7920 2829</div>
          <div class="login-footer-text login-footer-left"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Login',
}
</script>

<style>
  @import "~assets/css/login.css";


 html, body {
      width: 100%;
      height: 100%;
      background-color: #1D0C43;
  }

  .login-content {
      width: 100%;
      height: calc(100vh - 72px - 20px);
      overflow: hidden;
  }

  .login-box {
      width: 1200px;
      height: 100%;
      margin: auto;
      position: relative;
      /*top: 10px;*/
  }


  .login-earth {
      width: 460px;
      height: 460px;
      position: absolute;
      left: 110px;
      top: 85px;
  }

  .login-earth-contaner {
      position: absolute;
      height: 654px;
      width: 646px;
      background: url('~assets/images/full-intro-earth.png') center center/contain no-repeat;
      top: -125px;
      left: -135px;
  }

  .login-earth-slogan {
      position: absolute;
      height: 118px;
      width: 738px;
      top: 100px;
      left: -130px;
  }

  .login-from {
      width: 300px;
      position: absolute;
      right: 20px;
      top: 160px;
      padding: 38px;
      background-color: #fff;
      border-radius: 6px;
  }

  .login-from-title {
      text-align: center;
      font-weight: 700;
      font-size: 20px;
      margin-bottom: 25px;
  }

  .login-from-item {
      position: relative;
  }

  .login-from-item input {
      padding-right: 0;
      width: 100%;
      box-sizing: border-box;
  }

  .login-action-line input {
      background-color: #00a690;
  }

  .login-from-item .show-pwd {
      width: 17px;
      height: 17px;
      background-repeat: no-repeat;
      background-position: center;
      background-size: contain;
      position: absolute;
      right: 10px;
      top: 16px;
      cursor: pointer;
  }

  .login-action-link {
      margin-top: 15px;
  }

  .login-action-link .layui-form-checked i, .layui-form-checked:hover i {
      color: #fff;
      background-color: #00a690;
  }

  .login-action-link .green-checkbox-wrapper {
      float: left;
  }

  .login-action-link .remember > span {
      line-height: 30px;
      font-size: 18px;
      color: #9b9b9c;
      text-align: left;
  }

  .login-action-link .remember:after {
      content: "";
      display: block;
      clear: both;
  }

  .login-footer:after {
      content: "";
      display: block;
      clear: both;
  }

  .login-footer {
      height: 20px;
      font-size: 12px;
      color: #fff;
      text-align: center;
  }

  .login-footer .login-footer-left {
      /*float: left;*/
      width: auto;
      color: #ffffff;
  }

  .login-footer .login-footer-right {
      /*float: right;*/
      width: auto;
  }

  .login-footer-text {
      line-height: 20px;
  }

  .login-footer-body {
      width: 1200px;
      margin: auto;
      padding: 0 20px;
      box-sizing: border-box;
  }

  .login-header {
      height: 66px;
      width: 1200px;
      margin: auto;
      padding: 0 20px;
  }

  .login-header-wrap {
      line-height: 66px;
      color: #fff;
  }

  .login-header-img {
      height: 40px;
      width: 188px;
      margin-left: 5%;
      margin-top: 1%;
  }



  .login-earth-slogan-text {
      text-align: center;
      color: #fff;
  }

  .login-earth-slogan-title p {
      font-size: 52px;
      letter-spacing: 28px;
      font-family: 方正兰亭超细黑简体;
      margin-top: 10px;
  }

  .login-earth-slogan-subtitle {
      margin-top: 15px;
  }

  .login-earth-slogan-subtitle span {
      font-size: 25px;
      letter-spacing: 3px;
      font-family: 方正兰亭超细黑简体;
  }

  .login-earth-slogan-subtitle span + span {
      margin-left: 30px;
  }

  #azlyx {
      color: #ffffff !important;
  }

</style>
