<template>
  <div class="home">
   
    <goods msg="Welcome to Your Vue.js App" />
  </div>
  
</template>

<script>
// @ is an alias to /src
import goods from "@/components/goods.vue";

export default {
  name: "Home",
  components: {
    goods
  },
  
  props: {
    n: String,
    price: Number,
    Amount: Number,
    Total:Number,
    Data: Array
},
};
</script>
