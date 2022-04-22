<template>
  <div class="card-product-type" v-for="(item, index) in data" :key="index" :style="{'margin-right' : '1rem'}">
    <img :src="item.urlBg" alt="" />
    <div class="card-info">
      <img :src="item.urlIcon" alt="" />
      <p>{{item.title}}</p>
    </div>
  </div>

</template>

<script>
export default {
  name: "CardProductType",
  props: {
    data: Array,

  },
  data() {
    return {};
  },
};
</script>

<style>
@import "../../assets/css/main.css";

.card-product-type {
  font-family: "Neosanintel";
  box-sizing: border-box;
  width: 230px;
  height: 160px;
  border-radius: 16px;
  display: flex;
  align-items: center;
  cursor: pointer;
  
  transition: 0.5s ease-in-out;
  position: relative;
  overflow: hidden;
}
.card-product-type:hover {
  transform: translateY(10px);
}
.card-product-type::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: #120f0f;
  opacity: 0;
  top: 0;
  left: 0;
  display: block;
  transition: 0.5s all;
  z-index: 2;
}
.card-product-type:hover::before {
  opacity: 0.5;
}

.card-product-type img {
  object-fit: cover;
  width: 100%;
  height: 100%;
}
.card-product-type .card-info {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  position: absolute;
  z-index: 4;
  width: 100%;
  height: 100%;
}

.card-product-type .card-info img {
  width: 4rem;
  height: 4rem;
  display: none;
  transition: 0.5s ease-out;
}
.card-product-type:hover .card-info img {
  display: block;
}

.card-product-type .card-info p {
  display: block;
  transition: 0.5s ease-out;
  margin: 0;
  color: white;
  font-weight: bold;
  text-shadow: 0px 4px 3px rgba(0,0,0,0.4),
             0px 8px 13px rgba(0,0,0,0.1),
             0px 18px 23px rgba(0,0,0,0.1);
  display: none;
  text-transform: capitalize;
}
.card-product-type:hover .card-info p {
  display: block;
}
</style>
