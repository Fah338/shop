<template>
  <div id="app">
  <div>
    <b-navbar toggleable="lg" type="dark" variant="danger">

    <div  id="nav" >
    <h2>
    <router-link to="/" >Shop</router-link> </h2>
    </div>
    
     
       <b-navbar-nav class="ml-auto">
        
       
      
<router-link to="/bill">
    <b-button variant="dark"
    type="button"
    @click="submit()">
        <b-icon icon="basket2-fill"></b-icon> ตะกร้า
      </b-button>
   <b-button 
    type="button"
    @click="cleardata()">
         ลบ
      </b-button>
      </router-link>   
      </b-navbar-nav>
    
    </b-navbar>
  </div>

    <router-view 
   />
  </div>
</template>
<script>
export default {
  data(){
    return{
      Total:0,
      Menuitem:[],
      select:[],
      Data:[]
    };
  },
  methods: {
    //คิดยอดรวม
    
    // menuorder(value){
    //   this.select = value;
    // },
    // AddMenu(value){
    //   this.Menuitem.push(value);
    // }
  }
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
