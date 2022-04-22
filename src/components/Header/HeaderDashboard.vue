<template>
  <header>
    <div class="container header-inner">
      <div class="header-top">
        <ul class="header-top__menu">
          <li v-for="(item, index) in topIcons" :key="index">
            <img :src="item.urlIcon" />
            <a href="">{{ item.title }}</a>
          </li>
        </ul>
      </div>
      <div class="header-middle">
        <div class="logo">
          <img src="../../assets/imgs/header-icon-middle/logo.png" alt="" />
        </div>
        <div class="box-search">
          <input type="text" placeholder="Bạn đang tìm thuốc gì..." />
          <button class="box-search__btn">
            <fa
              :icon="['fas', 'search']"
              :style="{ color: '#838383', 'margin-right': '0.5rem' }"
            />
            <p>Tìm kiếm</p>
          </button>
        </div>
        <div class="header-middle-btn">
          <button>
            <img
              src="../../assets/imgs/header-icon-middle/01.png"
              :style="{ 'margin-right': '0.5rem' }"
              alt=""
            />
            <p>Tạo toa thuốc</p>
          </button>
          <button>
            <img
              src="../../assets/imgs/header-icon-middle/02.png"
              :style="{ 'margin-right': '0.5rem' }"
              alt=""
            />
            <p>Giỏ hàng</p>
          </button>
        </div>
      </div>
      <div class="header-bottom">
        <ul>
          <li v-for="(item, index) in bottomIcons" :key="index">
            <img :src="item.urlIcon" />
            <a href="">{{item.tabMenuName}}</a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "PhanolLinkHeader",
  data() {
    return {
      topIcons: [
        {
          urlIcon: require("../../assets/imgs/header-icon-top/01.png"),
          title: "Khuyến mãi HOT",
        },
        {
          urlIcon: require("../../assets/imgs/header-icon-top/02.png"),
          title: "Thông báo của tôi",
        },
        {
          urlIcon: require("../../assets/imgs/header-icon-top/03.png"),
          title: "Đăng nhập tài khoản",
        },
      ],
      bottomIcons: [
        {
          urlIcon: require("../../assets/imgs/header-icon-bottom/01.png"),
          tabMenuName: "danh mục sản phẩm",
        },
        {
          urlIcon: require("../../assets/imgs/header-icon-bottom/02.png"),
          tabMenuName: "khuyến mãi hot",
        },
        {
          urlIcon: require("../../assets/imgs/header-icon-bottom/03.png"),
          tabMenuName: "hệ thống nhà thuốc",
        },
        {
          urlIcon: require("../../assets/imgs/header-icon-bottom/04.png"),
          tabMenuName: "góc sức khỏe",
        },
        {
          urlIcon: require("../../assets/imgs/header-icon-bottom/05.png"),
          tabMenuName: "giới thiệu",
        },
        {
          urlIcon: require("../../assets/imgs/header-icon-bottom/05.png"),
          tabMenuName: "hướng dẫn",
        },
      ],
    };
  },
};
</script>

<style lang="css">
/* ---- Css Global ----*/
@import "../../assets/css/main.css";
/* ---- End Css Global ----*/



/* ========== Phanol Header ==========*/

header {
  height: 168px;
  box-sizing: border-box;
  margin-top: 0;
  background-color: #01adab;
    font-family: "Neosanintel";
}
header .header-inner {
  background-color: #01adab;
  height: 100%;
  box-sizing: border-box;
  padding: 0.75rem 0;
}
/* ----> Header Top <---- */
header .header-top {
}
header .header-top .header-top__menu {
  list-style-type: none;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  margin: 0.5rem 0;

}

header .header-top .header-top__menu li {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 3rem;
  cursor: pointer;
}
header .header-top .header-top__menu li:nth-child(3) {
  margin-right: 0;
}

header .header-top .header-top__menu li img {
  display: block;
  margin-right: 0.5rem;

  width: 1.5rem;
  height: 1.5rem;
}
header .header-top .header-top__menu li a {
  text-decoration: none;
  color: white;

}
/* ----> End Header Top <---- */

/* ----> Header Middle <---- */
header .header-inner .header-middle {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
header .header-inner .header-middle .box-search {
  display: flex;
  align-items: center;
  position: relative;
}
header .header-inner .header-middle .box-search input {
  width: 44.5rem;
  display: block;
  box-sizing: border-box;
  padding: 0.75rem 1.5rem;
  border: #707070;
  border-radius: 5px;
  overflow: hidden;
}
header .header-inner .header-middle .box-search input ::placeholder {
  color: #838383;
  font-size: 14px;
}
header .header-inner .header-middle .box-search .box-search__btn {
  position: absolute;
  right: 0;
  width: 7.8rem;
  border: none;
  border-radius: 0 5px 5px 0;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

header .header-inner .header-middle .box-search .box-search__btn p {
  text-transform: capitalize;
  color: #838383;
}
header .header-inner .header-middle .header-middle-btn {
  display: flex;
}
header .header-inner .header-middle .header-middle-btn button {
  width: 145px;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40px;
  border-radius: 5px;
  box-sizing: border-box;
  border: #707070;
  cursor: pointer;
}
header .header-inner .header-middle .header-middle-btn button p {
  color: #838383;
}
header .header-inner .header-middle .header-middle-btn button:nth-child(1) {
  margin-right: 1rem;
}
header .header-inner .header-bottom{
  
}
header .header-inner .header-bottom ul{
  list-style-type: none;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 5px auto;
  padding-left: 0;
}
header .header-inner .header-bottom ul li{
  padding-left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0.5rem;
  margin-right: 1.5rem;
  cursor: pointer;
}
header .header-inner .header-bottom ul li:last-child{
  margin-right: 0;
}
header .header-inner .header-bottom ul li a{
  text-decoration: none;
  color: white;
  text-transform: uppercase;
  font-size: 15.75px;
  letter-spacing: 1.75px;

}
header .header-inner .header-bottom ul li img{
  margin-right: 0.75rem;

}

/* ----> End Header Middle <---- */
</style>
