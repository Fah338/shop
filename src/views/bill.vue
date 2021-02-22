<template>
  <div class="bill">
   
    <orders msg="Welcome to Your Vue.js App" />
  </div>
 
  
</template>

<script>
// @ is an alias to /src
import orders from "@/components/orders.vue";

export default {
  name: "bill",
  components: {
    orders
  }
};
</script>