<template>
  <div>
    <mt-swipe :auto="4000" :speed="500">
      <mt-swipe-item>
        <img src="../assets/images/banner/banner1.jpg">
      </mt-swipe-item>
      <mt-swipe-item>
        <img src="../assets/images/banner/banner2.jpg">
      </mt-swipe-item>
      <mt-swipe-item>
        <img src="../assets/images/banner/banner3.jpg">
      </mt-swipe-item>
    </mt-swipe>
    <div class="hot">
          <div class="title">
            <span>豆瓣时刻</span>
            <span>更多专栏
              <!--<i class="fas fa-user">要改成下面这种形式的标签写法</i>-->
              <font-awesome-icon :icon="['fas','angle-right']" />
            </span>
          </div>
          <div class="content">
            <ul>
              <li>
                <img src="../assets/images/main/detail1.jpg" />
                <div>舌尖上的中国</div>
                <div>
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_half.png">
                  <img src="../assets/images/common/rating_star_xsmall_off.png">
                  <span>3.5</span>
                </div>
              </li>
              <li>
                <img src="../assets/images/main/detail1.jpg" />
                <div>舌尖上的中国</div>
                <div>
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_half.png">
                  <img src="../assets/images/common/rating_star_xsmall_off.png">
                  <span>3.5</span>
                </div>
              </li>
              <li>
                <img src="../assets/images/main/detail1.jpg" />
                <div>舌尖上的中国</div>
                <div>
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_half.png">
                  <img src="../assets/images/common/rating_star_xsmall_off.png">
                  <span>3.5</span>
                </div>
              </li>
              <li>
                <img src="../assets/images/main/detail1.jpg" />
                <div>舌尖上的中国</div>
                <div>
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_on.png">
                  <img src="../assets/images/common/rating_star_xsmall_half.png">
                  <img src="../assets/images/common/rating_star_xsmall_off.png">
                  <span>3.5</span>
                </div>
              </li>
            </ul>
          </div>
          
        </div>
  </div>
</template>
<script>
  
</script>
<style lang="less" scoped>
.mint-swipe{
   height:350px;//需要给父容器设置一个高度，否则不显示
   margin-bottom:50px;
  .mint-swipe-item{
    img{
      width:100%;//需要设置宽度，否则在切换的时候会出现别的图片
      height:350px;
    }
  }
}
.hot{
    margin-bottom:50px;
  }
  .mint-navbar{
    border: 1px solid #ccc;
    .mint-tab-item.is-selected{
      color:#42bd56;
      border-color:#42bd56;
    }
    .mint-tab-item{
      padding:32px 0;
      font-size:30px;
      .navTitle{
        font-size:30px;
      }
    }
  }
  .mint-tab-container-item{
    margin-top:30px;
    .title{
      text-align:left;
      border-left:10px solid #42bd56;
      padding:0 30px 0 15px;
      >span:last-child{
        color:#42bd56;
        float:right;
      }
    }
    .content{
      ul{
        font-size:0;
        overflow:scroll;
        white-space:nowrap;
        padding:0;
        li{
          width:500px;
          font-size:26px;
          list-style:none;
          display:inline-block;
          padding:30px 0 0 20px;
          >img{
            width:500px;
            height:300px;
          }
          div{
            text-align:left;
            margin:10px 0;
            img{
              width:20px;
              height:30px;
              vertical-align:bottom;
            }
            img:last-of-type{
              margin-right:10px;
            }
            span{
              display:inline-block;
              vertical-align:middle;
              color:#aaa;
            }
          }
        }
      }
    }
  }
</style>