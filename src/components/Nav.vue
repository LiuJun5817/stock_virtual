<template>
  <header>
    <div class="nav">
        <!--   头部导航 navigator     -->
        <img src="../img/汉堡包.png" alt="logo 图" @click="unfold_info" style="cursor:pointer;">
        <span class="title">股权分配虚拟仿真实验平台</span>
        <!-- 无意义的，为了撑开布局空间 -->
        <span class="spacer"></span>
        <img src="../img/金币.png" alt="">
        <a>总资产:1000000</a>
        <!-- <a href="#" @click="change_theme">切换主题</a> -->
    </div>
  </header>
</template>

<script>
export default {
  name: 'Nav',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav {
    /*导航栏设置*/
    width: 100%;
    height: 50px;
    background-color: black;
    color: #fff;
    /*字体为白色*/
    display: flex;
    /*弹性布局*/
    justify-content: left;
    align-items: center;
    /*平向左，居中对齐*/
}

.nav img {
    /*图片设置*/
    /*规定图片大小时，尽量只规定高或者宽，这样图片不会被拉伸变形*/
    height: 34px;
    margin-left: 30px;
    margin-right: 2px;
    border-radius: 50%;
}

.nav .spacer {
    width: 50%;
    /*把空格撑开*/
}

.nav a {
    /*a标签设置*/
    color: #fff;
    /*标签颜色：白色*/
    text-decoration: none;
    /*文本装饰：无*/
    padding: 0 10px;
    /*左右空开10像素*/
}


</style>
