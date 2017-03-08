<template lang="html">
  <el-menu default-active="1" id="nav-menu" theme="light" router>
    <div class="logo">
      <router-link to="/">
        <img src="../../assets/images/logo.svg" />
      </router-link>
    </div>
    <el-submenu index="1">
      <template slot="title"><i class="el-icon-menu"></i>系统管理</template>
      <el-menu-item index="page1">系统管理1</el-menu-item>
      <el-menu-item index="page2">系统管理2</el-menu-item>
    </el-submenu>
    <el-menu-item index="page3"><i class="el-icon-message"></i>公司管理</el-menu-item>
  </el-menu>
</template>
