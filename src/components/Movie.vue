<template>
  <div>
    <mt-navbar v-model="selected">
      <mt-tab-item id="movie">
        <span class="navTitle">电影</span>
      </mt-tab-item>
      <mt-tab-item id="book">
        <span class="navTitle">读书</span>
      </mt-tab-item>
      <mt-tab-item id="tv">
        <span class="navTitle">电视</span>
      </mt-tab-item>
      <mt-tab-item id="city">
        <span class="navTitle">同城</span>
      </mt-tab-item>
      <mt-tab-item id="music">
        <span class="navTitle">音乐</span>
      </mt-tab-item>
    </mt-navbar>

    <!-- tab-container -->
    <mt-tab-container v-model="selected">
      <mt-tab-container-item id="movie">
        <div class="hot">
          <div class="title">
            <span>影院热映</span>
            <span>更多
              <!--<i class="fas fa-user">要改成下面这种形式的标签写法</i>-->
              <font-awesome-icon :icon="['fas','angle-right']" />
            </span>
          </div>
          <div class="content">
            <ul>
              <li>
                <img src="../assets/images/main/time1.jpg" />
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
                <img src="../assets/images/main/time1.jpg" />
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
                <img src="../assets/images/main/time1.jpg" />
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
                <img src="../assets/images/main/time1.jpg" />
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
        <div class="soon">
          <div class="title">
            <span>院线即将上映</span>
            <span>更多
              <!--<i class="fas fa-user">要改成下面这种形式的标签写法</i>-->
              <font-awesome-icon :icon="['fas','angle-right']" />
            </span>
          </div>
          <div class="content">
            <ul>
              <li>
                <img src="../assets/images/main/time1.jpg" />
                <div>舌尖上的中国</div>
                <div>
                  <span>暂无评分</span>
                </div>
              </li>
              <li>
                <img src="../assets/images/main/time1.jpg" />
                <div>舌尖上的中国</div>
                <div>
                  <span>暂无评分</span>
                </div>
              </li>
              <li>
                <img src="../assets/images/main/time1.jpg" />
                <div>舌尖上的中国</div>
                <div>
                  <span>暂无评分</span>
                </div>
              </li>
              <li>
                <img src="../assets/images/main/time1.jpg" />
                <div>舌尖上的中国</div>
                <div>
                  <span>暂无评分</span>
                </div>
              </li>
            </ul>
          </div>
          
        </div>
      </mt-tab-container-item>
      <mt-tab-container-item id="book">
        读书
      </mt-tab-container-item>
      <mt-tab-container-item id="tv">
        电视
      </mt-tab-container-item>
      <mt-tab-container-item id="city">
        同城
      </mt-tab-container-item>
      <mt-tab-container-item id="music">
        音乐
      </mt-tab-container-item>
    </mt-tab-container>
  </div>
</template>
<script>
  export default {
    data(){
      return {
        selected:'movie'
      }
    }
  }
</script>
<style lang="less" scoped>
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
          width:220px;
          font-size:26px;
          list-style:none;
          display:inline-block;
          padding:30px 0 0 20px;
          >img{
            width:220px;
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