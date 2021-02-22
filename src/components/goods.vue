<template>
  
  <div class="hello">

  <b-card-group deck>
<div class="col-md-2" v-for="it in props" :key="it.it">
  <div class="card h-100">
    <img :src="it.image" class="car-img-top">
    <div class="card-body">
      <h4 class="card-title">{{it.n}}</h4>
      <p class="card-text">ราคา {{it.price}} บาท</p>
    </div>
    <div class="card-footer">
      <b-form-spinbutton 
  id="sb-small"
  size="sm"
  v-model="it.Amount"
  class="mb-2"></b-form-spinbutton>
  
      <button class="btn btn-dark" @click="Order(it)">หยิบลงตะกร้า</button>
      <div>
    </div>
    </div>
  </div>
  </div> 
  </b-card-group>
 


</div>

</template>

<script>
export default {
  name: 'App',
data(){
return{
  
  props:[
{
id:1,
n:"ครอปแขนบอลลูน3ส่วน",
price:139,
image:"https://cf.shopee.co.th/file/13a3f417c8544e8d47d20bb4263c4c2d_tn",
Amount:null,
active:false
},
{
id:2,
n:"เสื้อครอปไหมพรมฉลุลาย",
price:119,
image:"https://cf.shopee.co.th/file/a0cb44aa36e935bb4d2e92016ac52483",
Amount:null,
active:false
},
{
id:3,
n:"เสื้อครอปกระดุมหน้า",
price:99,
image:"https://cf.shopee.co.th/file/7acec4597073b47d5c0db7f12877e5f3",
Amount:null,
active:false
},
{
id:4,
n:"เสื้อสายเดี่ยวเอวลอย",
price:140,
image:"https://cf.shopee.co.th/file/b84a1f135d07de2f24b13d3e29a00764",
Amount:null,
active:false
},
{
id:5,
n:"เดรสชีฟอง รูดหน้า 2 ข้าง",
price:390,
image:"https://cp.lnwfile.com/9cgt1c.jpg",
Amount:null,
active:false
},
{
id:6,
n:"จั้มสูทสายเดียว ขาสั้น",
price:250,
image:"https://www.chrisvun.com/wp-content/uploads/2019/10/O1CN01JZZKC01ze3EUZgrJy_1057066738.jpg",
Amount:null,
active:false
},],
 
//  props:{
//    NameProduct:String,
//    img:String,
//    Price:Number
//  },
//  data(){
//    return{
//      Amount:1
//    };
//  },
 methods: {
   Order(){
   
     this.$emit("props",{
       n: this.n,
       price: this.price,
       Amount:this.Amount,
       Total:this.price*this.Amount

     });
   }
 },
}
},
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
