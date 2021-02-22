<template>
  <!-- <div class="orders">
    <div class="row">
     <product > -->
  <div class="container fluid">
    <br />
    <div>
      <div class="orders">
        <div class="card-header">
          <h2>รายการสินค้า</h2>
        </div>
        <div class="card-body">
          <table class="table table-hover">
            <thead>
              <tr>
                <th style="width: 58.33%">ชื่อ</th>
                <th style="width: 13.5%%">ราคา</th>
                <th style="width: 13.5%%">จำนวน</th>
                <th style="width: 14.66%">รวม</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td></td>
                <td></td>
                <td></td>
                <td></td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'App',
     methods: {
  submit(){
      this.Data = this.select;
      this.Total = 0;
      for(var i = 0; i < this.Data.length; i++){
        this.Total = this.Total+this.Data[i].Total;
      }
    },
    cleardata(){
      this.Total = 0;
      this.Data = [{}];
      this.select = [{}];

    },
   pushOrder(){
    this.$emit.push({
        n:this.n,
        price:this.price,
        Amount:this.Amount,
        total:this.price
  }
    )
  },

    


} 
};

</script>


