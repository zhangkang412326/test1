<!-- 首页 -->
<template>
  <div>
    <ul>
      <li v-for="(book, index) in bookList" :key="index">
          <el-link href="http://www.baidu.com" target="_blank"> {{ book }}</el-link> 
          <el-button type="primary" size="mini"  icon="el-icon-edit" round>主要按钮<i class="el-icon-edit"></i></el-button>      
      </li>
    </ul>
    
  </div>
</template>

<script>

export default {
  name: "Home",
  data() {
    return {
      bookList: ["老人与海", "海贼王", "王的盛宴"],
    };
  },
};
</script>

<style  scoped>
ul, li {
  margin: 0;
  padding: 0;
  list-style: none;
  text-align: left;
}
</style>
