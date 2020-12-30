<!-- 测试按钮 -->
<template>
  <div>
    <el-row>
      <el-button round>圆角按钮</el-button>
      <el-button type="primary" size="mini" round>主要按钮</el-button>
      <el-button type="success" size="mini" round>成功按钮</el-button>
      <el-button type="info" round>信息按钮</el-button>
      <el-button type="warning" round>警告按钮</el-button>
      <el-button type="danger" round @click="clickMe">危险按钮</el-button>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "Button",
  data() {
    return {
      msg: "这里很危险",
    };
  },
  methods: {
    clickMe() {
      console.log(this.msg);
      this.$emit("reseveMsg", this.msg);
    },
  },
};
</script>

<style  scoped>
.el-button--primary {
  background-color: #afa;
}
</style>
