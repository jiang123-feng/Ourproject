<template>
  <div class="home">
    <!-- 导航 -->
     <div id="daohang">
       <div class="daohang dingwei">定位</div>
       <div class="daohang">
         <input type="text" placeholder="请输入你想搜索的内容">
       </div>
       <div class="daohang  search">搜索</div>
     </div>


    <!-- 通告 -->
   <van-notice-bar
    left-icon="volume-o"
    text="  疫 情 就 是 命 令 , 防 控 就 是 责 任 ! ! ! ! ! ! ! !"
    />
    
    <!-- 分类 -->
     <div id="yqfwzs">
       <h5>疫情服务助手</h5>
       <van-grid :border="false" :column-num="3">
          <van-grid-item>
            <img src="../assets/01.jpg" />
             <span>核酸检测</span>
          </van-grid-item>
          <van-grid-item>
            <img src="../assets/02.jpg" />
             <span>核酸结果</span>
          </van-grid-item>
          <van-grid-item>
            <img src="../assets/03.jpg" />
            <span>医疗健康</span>
          </van-grid-item>
          <van-grid-item>
            <img src="../assets/04.jpg" />
             <span>风险地区</span>
          </van-grid-item>
          <van-grid-item>
            <img src="../assets/05.jpg" />
             <span>新冠疫苗专区</span>
          </van-grid-item>
          <van-grid-item>
            <img src="../assets/06.jpg" />
            <span>患者轨迹</span>
          </van-grid-item>
       </van-grid>
     </div>
     <!-- 内容 -->
     <van-tabs
        v-model="active" 
        sticky
        title-active-color="red"
        style="font-size:15px"
      >
        <van-tab title="全国" title-style="font-size:17px">
         <van-row>
            <van-col span="8">span: 8</van-col>
            <van-col span="8">span: 8</van-col>
            <van-col span="8">span: 8</van-col>
          </van-row>
        </van-tab>
        <van-tab title="本地" title-style="font-size:17px;">
         内容2
        </van-tab>
        <van-tab title="关注地" title-style="font-size:17px">内容 3</van-tab>
        <van-tab title="国外" title-style="font-size:17px">内容 4</van-tab>
     </van-tabs>
  </div>
</template>

<script>
   export default{
     data() {
       return {
         active: 0,
       }
     },
   }

</script>

<style scoped>
#daohang{
  width: 100%;
  height: 15vw;
  background-color: aqua;
  margin-bottom: 1vw;
  
}
#daohang>.daohang{
  display: inline-block;
  line-height: 15vw;
}
.daohang>input{
  width: 60vw;
  height: 8vw;
  border-radius:20px;
  outline: 0px;
  border: 0px;
  padding-left: 5vw;
  margin-right: 3vw;
}
.search{
   
}
.dingwei{
  width: 16vw;
  text-align: center;
}
.van-grid-item__content>img{
  width: 12vw;
}
#yqfwzs h5{
  font-size: 17px;
  margin:5vw 0 0 4vw;
  color: rgb(97, 91, 91);
}
</style>
