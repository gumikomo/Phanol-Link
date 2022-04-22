<template>
  <main>
    <section class="first">
      <Slider/>
    </section>
    <section class="container second">
      <CardProductType :data="productTypes"/>
    </section>
  </main>
</template>

<script>
import CardProductType from "../Cards/CardProductType.vue";
import Slider from '../Slider/Slider.vue';

export default {
  name: "PhanolLinkBody",
  components: {
    CardProductType,
    Slider, 

  },
  data() {
    return {
      productTypes: [
        {
          urlIcon: require("../../assets/imgs/Body-product-type/01-icon.png"),
          urlBg: require("../../assets/imgs/Body-product-type/01-bg.png"),
          title: "thuốc không kê đơn",
        },
        {
          urlIcon: require("../../assets/imgs/Body-product-type/01-icon.png"),
          urlBg: require("../../assets/imgs/Body-product-type/02-bg.png"),
          title: "thực phẩm chức năng",
        },
        {
          urlIcon: require("../../assets/imgs/Body-product-type/03-icon.png"),
          urlBg: require("../../assets/imgs/Body-product-type/03-bg.png"),
          title: "hàng tiêu dùng",
        },
        {
          urlIcon: require("../../assets/imgs/Body-product-type/04-icon.png"),
          urlBg: require("../../assets/imgs/Body-product-type/04-bg.png"),
          title: "mỹ phẩm",
        },
        {
          urlIcon: require("../../assets/imgs/Body-product-type/05-icon.png"),
          urlBg: require("../../assets/imgs/Body-product-type/05-bg.png"),
          title: "dụng cụ y tế"
        },
      ],
    };
  },
};
</script>

<style>
@import "../../assets/css/main.css";

.second{
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 2rem auto;


}
</style>
