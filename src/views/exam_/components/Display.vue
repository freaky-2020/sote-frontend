<template>
  <el-card>
    <div>
        <!--      @click是v-on:click的缩写，这时v-for循环的index就起到了用处，将所点击的button的index下标传到clickbtnX方法内-->
        <!--      :type是v-bind:type的缩写，其意思是判断flagX是否等于index+1，如果等于，加上名为primary的样式，如果不等于则空-->
        <!--      v-for需要有:key="item.id，否则会报错"-->
      <a @click="goAnchor('#masd')">点击这里跳转</a>
      <div slot="header" class="clearfix">
        <h3 class="box-center">单选题（共1题，0.00分）</h3>
      </div>
      1.给书柜定位时，宜用mm定位线
      <div v-for="(item,index) in navList" :key="item.id" @click="clickbtnX(index)">
        <el-button class="elbtn" size="mini" circle :type="flagX===(index+1)?'primary':''" >{{ item.name }}</el-button>
        sdfsd
      </div>
      <div slot="header" class="clearfix">
        <h3 class="box-center">多选题（共1题，0.00分）</h3>
      </div>
      1.给书柜定位时，宜用mm定位线
      <div v-for="(item,index) in navList" :key="item.id" @click="clickbtnX(index)">
        <el-button class="elbtn" size="mini" circle :type="flagX===(index+1)?'primary':''" >{{ item.name }}</el-button>
        sdfsd
      </div>
      1.给书柜定位时，宜用mm定位线
      <div v-for="(item,index) in navList" :key="item.id" @click="clickbtnX(index)">
        <el-button class="elbtn" size="mini" circle :type="flagX===(index+1)?'primary':''" >{{ item.name }}</el-button>
        sdfsd
      </div>
      1.给书柜定位时，宜用mm定位线
      <div v-for="(item,index) in navList" :key="item.id" @click="clickbtnX(index)">
        <el-button class="elbtn" size="mini" circle :type="flagX===(index+1)?'primary':''" >{{ item.name }}</el-button>
        sdfsd
      </div>
      1.给书柜定位时，宜用mm定位线
      <div v-for="(item,index) in navList" :key="item.id" @click="clickbtnX(index)">
        <el-button id="masd" class="elbtn" size="mini" circle :type="flagX===(index+1)?'primary':''" >{{ item.name }}</el-button>
        sdfsd
      </div>
    </div>
  </el-card>
</template>
<script>
export default {
  data() {
    return {
      navList: [
        { name: 'A' },
        { name: 'B' },
        { name: 'C' },
        { name: 'D' }
      ],
      flagX: 1
    }
  },
  methods: {
    clickbtnX(index) {
      this.flagX = index + 1
    },
    //模拟锚点跳转
    goAnchor(selector) {//参数selector是id选择器（#anchor14）
      document.querySelector(selector).scrollIntoView({
        behavior: "smooth"
      });
    },
  }
}
</script>
<style lang="scss">
.elbtn{
  width: 25px;
  height: 25px;
  margin-bottom: 10px;
}
</style>
