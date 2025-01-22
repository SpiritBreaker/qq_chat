<template>
  <el-container class="layout-container-demo" style="height: 500px">
    <el-header>
      <span class="logo">Home</span>
      <span class="info">
        Welcome
      </span>
    </el-header>

    <el-container>
      <el-aside width="200px">
        <el-scrollbar>
          <el-menu
            active-text-color="#ffd04b"
            background-color="#545c64"
            text-color="#fff"
            :router="true">
            <el-menu-item v-for="menu in menus" :index="menu.path">
              <el-icon>
                <component :is="menu.icon"/>
              </el-icon>
              <span>{{ menu.name }}</span>
            </el-menu-item>
          </el-menu>
        </el-scrollbar>
      </el-aside>

      <el-main>
        <el-scrollbar>
          Page content goes here
        </el-scrollbar>
      </el-main>
    </el-container>
  </el-container>
</template>

<script lang="ts" setup>
const menus = [

]
</script>

<style scoped lang="scss">
.layout-container-demo  {
  .el-header, .el-aside {
    position: relative;
    background-color: rgb(84 92 100);
    color: white;
  }
  .el-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .el-aside {
    height: calc(100vh - 60px);
  }

  .logo {
    font-size: 26px;
  }
  .exit {
    text-decoration: underline;
    cursor: pointer;
  }
  .info {
    display: flex;
    align-items: center;
  }
}
</style>
