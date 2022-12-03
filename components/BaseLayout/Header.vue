<template>
  <div class="header">
    <div class="left-wrap">
      <div class="select-area">
        <el-dropdown @command="handleCommand">
            <span class="el-dropdown-link">
              全球<i class="el-icon-arrow-down el-icon--right"></i>
            </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item command="a">中国大陆</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
      <div class="login-text-slice">
        <span class="global-color">亲，请登录</span>
        <nuxt-link to="/regis">注册</nuxt-link>
      </div>
      <div class="login-text-slice">
        <a href="">手机逛SGO</a>
      </div>
    </div>

    <div class="right-wrap">
        <div class="profile">
          <el-dropdown @command="handleCommand">
            <span class="el-dropdown-link">
              我的<i class="el-icon-arrow-down el-icon--right"></i>
            </span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item command="a">买到的宝贝</el-dropdown-item>
              <el-dropdown-item command="b">我的足迹</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </div>

        <div class="cart">
          <nuxt-link to="/cart">购物车</nuxt-link>
        </div>


      <div class="collect">
        <el-dropdown @command="handleCommand">
            <span class="el-dropdown-link">
              收藏夹<i class="el-icon-arrow-down el-icon--right"></i>
            </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item command="a">收藏的宝贝</el-dropdown-item>
            <el-dropdown-item command="b">收藏的店铺</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderCompo",

  methods: {
    handleCommand() {},
  }
}
</script>

<style scoped lang="scss">
// login-text-slice start
.header, .left-wrap, .right-wrap {
  height: 100%;
  justify-content: space-between;
  @extend .flex-center;
}

.select-area, .login-text-slice , .profile, .cart, .collect  {
  @extend .ml-10;
}
.login-text-slice {

}

.global-color {
  color: $base-color;
}
// login-text-slice end
</style>
