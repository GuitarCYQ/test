<template>
  <div>
    <el-container>
      <el-aside width="200px">
        <el-menu default-active="2" class="el-menu-vertical-demo">
          <h3 class="title">校园活动</h3>
          <el-menu-item index="2">
            <i class="el-icon-menu"></i>
            <span slot="title">
              <router-link to="/dynamic">Go to Foo</router-link>
            </span>
          </el-menu-item>
        </el-menu>
      </el-aside>
      <el-main>
        <el-row class="row_b">
          <el-col :span="7">
            <el-breadcrumb separator="/">
              <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
              <el-breadcrumb-item><a href="/">活动管理</a></el-breadcrumb-item>
              <el-breadcrumb-item>活动列表</el-breadcrumb-item>
              <el-breadcrumb-item>活动详情</el-breadcrumb-item>
            </el-breadcrumb>
          </el-col>
          <el-col :span="5" :offset="12">
            <el-button type="primary" size="mini" round icon="el-icon-add">
              发布活动
            </el-button>
          </el-col>
        </el-row>
        <el-row>
          <!-- 标签页 -->
          <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="全部" name="first"></el-tab-pane>
            <el-tab-pane label="外单位发布" name="second"></el-tab-pane>
            <el-tab-pane label="未分类" name="third"></el-tab-pane>
          </el-tabs>
        </el-row>
      </el-main>
    </el-container>
    <!-- <el-row>
      <el-col :span="3">
        <el-menu default-active="2" class="el-menu-vertical-demo">
          <h3 class="title">校园活动</h3>
          <el-menu-item index="2">
            <i class="el-icon-menu"></i>
            <span slot="title">
              <router-link to="/release">Go to Foo</router-link>
            </span>
          </el-menu-item>
        </el-menu>
      </el-col>

      <el-col :span="9">
        <el-row>
          <el-col :span="24">
            <div class="grid-content bg-purple-dark">asdsa</div>
          </el-col>
        </el-row>
      </el-col>
    </el-row> -->
  </div>
</template>

<script>
  export default {
    data() {
      return {
        activeName: 'first',
      }
    },
  }
</script>

<style scoped>
  .title {
    text-align: center;
  }
  .el-container {
    height: 100%;
  }
  .el-aside {
    height: 100%;
  }
  .el-menu {
    height: 100%;
  }
  .el-menu-item {
    height: 100%;
  }
  .row_b {
    border-bottom: 1px solid #ccc;
    padding-bottom: 10px;
  }
  .el-breadcrumb {
    margin-top: 5px;
  }
  .el-tabs {
    margin-top: 30px;
    border: none !important;
  }
</style>
