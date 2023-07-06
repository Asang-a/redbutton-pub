<template>
  <div>
    <!-- header -->
    <div class="main-header">
      <div class="area-title">
        <p>
          지점<br />
          이름
        </p>
        <span>로그아웃</span>
      </div>

      <div class="align-center">
        <div class="box-main" v-for="n in 2" :key="n">
          <div class="box-main-top">
            <p class="title">
              title
              <span class="icon-right-arrow"></span>
            </p>
            <p>info</p>
          </div>
          <div class="box-main-bottom">
            <ul>
              <li v-for="i in 5" :key="i">가나다라<span class="year">2016</span></li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <div class="main-contents">
      <!-- header tab -->
      <ul class="tab">
        <li class="on">공지사항</li>
        <li>즐겨찾기</li>
      </ul>

      <!-- body -->
      <div class="contents-body">
        <table>
          <tr>
            <th>분류</th>
            <th>제목</th>
            <th>일시</th>
            <th></th>
          </tr>
          <tr v-for="n in 8" :key="n">
            <td>구매</td>
            <td>제ㅔㅔㅔ목</td>
            <td>23년 03월 04일</td>
            <td></td>
          </tr>
        </table>
      </div>

      <!-- body-write -->
      <div></div>
    </div>

    <Footer></Footer>
  </div>
</template>

<script setup lang="ts">
import Footer from '@/components/Footer.vue'
</script>
<script lang="ts">
export default {}
</script>

<style lang="scss">
.main-header {
  background-color: $bodyDefault;
  height: 540px;
  border-radius: 0 0 40px 40px;
}

.area-title {
  display: flex;
  justify-content: space-between;
  padding: 50px 65px 0 65px;
  p {
    font-size: 50px;
    font-weight: 520;
    line-height: 1.2;
  }

  span {
    color: $achromatic50;
    margin-top: 10px;
  }
}

.box-main {
  background-color: $achromatic0;
  border-radius: 30px;
  width: 710px;
  margin: 52px 13px;

  .box-main-top {
    box-sizing: border-box;
    padding: 38px;
    height: 175px;
    > .title {
      font-size: 38px;
      font-weight: 520;
      padding-bottom: 14px;
      color: $achromatic100;
    }
    > p {
      color: $textHyperlink;
      font-size: 30px;
    }
    .icon-right-arrow {
      float: right;
    }
  }

  .box-main-bottom {
    box-sizing: border-box;
    padding: 38px;
    height: 95px;
    border-top: 1px solid;
    border-color: $achromatic40;

    ul {
      white-space: nowrap;
      overflow-x: auto;
      li {
        display: inline-block;
        margin-right: 27px;
        .year {
          font-size: 24px;
          margin-left: 5px;
          color: $achromatic50;
        }
      }
    }
  }
}

.main-contents {
  padding: 45px;

  .tab {
    padding: 0 0 40px 0;
  }

  .contents-body {
    background-color: $achromatic0;
    border-radius: 30px;
  }
}
</style>
