<template>
  <div class="food">
    <div class="conteainer">
      <h2 align="center">เลือกเมนูอาหาร</h2>
      <hr />
      <div class="row">
        <div class="col-md-3" v-for="item in product" v-bind:key="item">
          <div class="card h-50 w-40">
            <img :src="item.image" class="car-img-top" alt="" />
            <div class="card-body">
              <h4 class="card-title">{{ item.name }}</h4>
              <p class="card-text">ราคา {{ item.price }} บาท</p>
            </div>
            <div class="card-footer">
              <input type="checkbox" @change="selected(item)" />
            </div>
          </div>
        </div>
        <h2 style="margin: 30dp">ยอดชำระเงิน {{ total() }} บาท</h2>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "Food",
  data(): {
    product: {
      id: number;
      name: string;
      price: number;
      image: string;
      active: boolean;
    }[];
  } {
    return {
      product: [
        {
          id: 1,
          name: "กาแฟเย็น",
          price: 30,
          image:
            "https://cdn.pixabay.com/photo/2014/11/21/15/20/coffee-540653_960_720.jpg",
          active: false,
        },
        {
          id: 2,
          name: "ชาเย็น",
          price: 35,
          image:
            "https://cdn.pixabay.com/photo/2016/11/29/01/11/beverages-1866476_960_720.jpg",
          active: false,
        },
        {
          id: 3,
          name: "ชามะนาว",
          price: 40,
          image:
            "https://cdn.pixabay.com/photo/2018/01/11/17/29/ice-tea-3076517_960_720.jpg",
          active: false,
        },
      ],
    };
  },

  // methods: {
  //   selected: function (item: any) {
  //     item.active = !item.active;
  //   },
  //   total: function (): number {
  //     var sum = 0;
  //     this.product.forEach(function (item: any) {
  //       if (item.active) {
  //         sum += item.price;
  //       }
  //     });
  //     return sum;
  //   },
  // },
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
