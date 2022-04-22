<template>
  <main>
    <div class="container slider-inner">
      <div class="slider-left"></div>
      <div class="slider-right">
        <div
          v-for="(item, index) in sliderRightIcon"
          :key="index"
          class="slider-right-strength"
        >
          <img :src="item.urlIcon" alt="" />
          <p>{{ item.title }}</p>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "PhanolLinkSlider",
  data() {
    return {
      sliderRightIcon: [
        {
          urlIcon: require("../../assets/imgs/Slider/01.png"),
          title: "Dược sỹ tư vấn",
        },
        {
          urlIcon: require("../../assets/imgs/Slider/02.png"),
          title: "Sản phẩm chính hãng",
        },
        {
          urlIcon: require("../../assets/imgs/Slider/03.png"),
          title: "Giao hàng toàn quốc",
        },
        {
          urlIcon: require("../../assets/imgs/Slider/04.png"),
          title: "Tích luỹ đổi quà",
        },
      ],
    };
  },
};
</script>

<style>
/* ---- Css Global ----*/
@import "../../assets/css/main.css";
/* ---- End Css Global ----*/



/* ========== Phanol Slider ==========*/
main {
  background-color: white;
  font-family: "Neosanintel";
}
main .slider-inner {
}
main .slider-inner .slider-left {
  width: 70%;
  background-color: red;
}
main .slider-inner .slider-right {
  width: 30%;
}
main .slider-inner .slider-right .slider-right-strength {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  box-sizing: border-box;
  padding: 1rem;
  
}
main .slider-inner .slider-right .slider-right-strength p {
  text-align: center;
  color: #777777;
}
</style>
