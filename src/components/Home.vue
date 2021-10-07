<template>
  <div>
    <section>
      <header class="top_tips">
        <span class="num_tip" v-if="fatherComponent == 'home'">{{level}}</span>
        <span class="num_tip" v-if="fatherComponent == 'item'">题目{{itemNum}}</span>
      </header>
    </section>
    <el-container>
      <el-header >
        服务器环境：
        <el-select v-model="value" placeholder="请选择">
          <el-option
            v-for="item in options1"
            :key="item.value"
            :label="item.label"
            :value="item.value">
          </el-option>
        </el-select>
        节点：
        <el-select v-model="value" placeholder="请选择">
          <el-option
            v-for="item in options2"
            :key="item.value"
            :label="item.label"
            :value="item.value">
          </el-option>
        </el-select>
        <el-checkbox v-model="checked1" label="重载配表" border></el-checkbox>
      </el-header>
      <el-container>
        <el-aside width="130px" >Aside</el-aside>
        <el-container>
          <el-main >content</el-main>
<!--          <el-footer>Footer</el-footer>-->
        </el-container>
      </el-container>
    </el-container>
  </div>


</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      options1: [{
        value: '选项1',
        label: 'QA'
      }, {
        value: '选项2',
        label: 'Dev'
      }, {
        value: '选项3',
        label: 'Prod'
      }],
      options2: [{
        value: '选项1',
        label: 'gateway'
      }, {
        value: '选项2',
        label: 'login'
      }, {
        value: '选项3',
        label: 'sns'
      }, {
        value: '选项4',
        label: '龙须面'
      }, {
        value: '选项5',
        label: '北京烤鸭'
      }],
      value: ''
    }
  }

}
</script>

<style lang="less">
.top_tips{
  position: absolute;
  height: 7.35rem;
  width: 3.25rem;
  top: -1.3rem;
  right: 1.6rem;
  background: url(../assets/logo.png) no-repeat;
  background-size: 100% 100%;
  z-index: 10;
  .num_tip{
    position: absolute;
    left: 0.48rem;
    bottom: 1.1rem;
    height: 0.7rem;
    width: 2.5rem;
    font-size: 0.6rem;
    font-family: '黑体';
    font-weight: 600;
    color: #a57c50;
    text-align: center;
  }
}

.el-header, .el-footer {
  background-color: #409EFF;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #D3DCE6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #E9EEF3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
