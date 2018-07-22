<template>
  <div>
    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" background-color="red" text-color="white">
      <el-menu-item index="1">
        <nuxt-link :to='"/login"' style="text-decoration:none">Log In</nuxt-link>
      </el-menu-item>
      <el-submenu index="2">
        <template slot="title">Workspace</template>
        <el-menu-item index="2-1">item one</el-menu-item>
        <el-menu-item index="2-2">item two</el-menu-item>
        <el-menu-item index="2-3">item three</el-menu-item>
        <el-submenu index="2-4">
          <template slot="title">item four</template>
          <el-menu-item index="2-4-1">item one</el-menu-item>
          <el-menu-item index="2-4-2">item two</el-menu-item>
          <el-menu-item index="2-4-3">item three</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">Orders</a></el-menu-item>
    </el-menu>
    <div style="background-image:url('/Santorini.jpg');background-size:100%;min-height:60vh;background-position:center center">
      <el-container>
        <el-main>
          <h1 style="margin:0;color:white; font-family:'Schoolbell';text-align:center;font-size:5em">TravelPost</h1>
          <h1 style="text-align:center;color:white;margin:0;font-weight:lighter">It's a passion to get lost!</h1>
        </el-main>
      </el-container>
    </div>
  </div>
</template>

<script>

export default {
}
</script>
