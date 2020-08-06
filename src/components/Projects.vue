<template>
  <div class="container">
    <div class="box" v-for="(item, index) in projects" :key="index">
      <div class="centerTitle">{{ item.name }}</div>
      <div class="title">项目名：{{ item.name }}</div>
      <div class="src">项目在线演示地址：{{ item.src }}</div>
      <div class="resource">项目源码地址：{{ item.src }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data() {
    return {
      projects: [
        { name: "vue电商项目", src: "www.baidu.com" },
        { name: "移动端布局", src: "www.baidu.com" },
        { name: "基于hbase的微博粉丝管理系统", src: "www.baidu.com" },
        { name: "简易旅游app", src: "www.baidu.com" },
        { name: "法典在线学习系统", src: "www.baidu.com" },
        // { name: "基于hbase的微博粉丝管理系统", src: "" },
        // { name: "简易旅游app", src: "" },
        // { name: "法典在线学习系统", src: "" },
      ],
    };
  },
};
</script>
<style lang="less">
.container {
  margin-top: 20px;
  height: 300px;
  display: flex;
  justify-content: center;
  .box {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 300px;
    font-family: "楷体";
    // line-height: 300px;
    text-align: left;
    flex-shrink: 0;
    flex-basis: 230px;
    background-color: #fff;
    box-shadow: 1px 1px 10px 1px rgba(0, 0, 0, 0.1);
    box-sizing: border-box;
    margin: 0 20px;
    border-radius: 5px;
    transition: all 0.5s;
    cursor: pointer;
    overflow: hidden;
    .centerTitle {
      font-weight: 700;
      font-size: 20px;
    }
    &:hover {
      box-shadow: 5px 5px 10px 5px rgba(0, 0, 0, 0.1);
      transform: translateY(-6px);
    }
    &:hover .centerTitle {
      display: none;
    }
    .title,
    .src,
    .resource {
      position: absolute;
      // display: none;
      height: 40px;
      width: 90%;
      font-weight: 400;
      color: #fff;
      // transform: translateX(130%);
      top: 10%;
      left: 100%;
      font-family: "楷体";

      transition: all 1s;
      background-color: #3498db;
      border-radius: 4px;
      margin-left: 20px;
      padding: 6px 5px;
    }
    .src {
      top: 40%;
      transition: all 1.2s;
      background-color: #f1c40f;
    }
    .resource {
      top: 70%;
      transition: all 1.4s;
      background-color: #2ecc71;
    }
    &:hover .title {
      left: 0;
    }

    &:hover .src {
      left: 0;
    }

    &:hover .resource {
      left: 0;
    }
    box-sizing: border-box;
    padding: 10px;
  }
}
</style>
