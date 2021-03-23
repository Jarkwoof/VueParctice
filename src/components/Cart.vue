<template>
  <div class="foot">
    <div class="item_container" v-for="(item , index) in list" :key="item.id">
      <div class="item_header item_body">
        <div class="item_detail">
          <img v-bind:src="item.thumb" alt="" />
          <div class="name">{{ item.name }}</div>
        </div>
        <div class="price"><span>$</span>{{ item.price }}</div>
        <div class="count">
          <button class="btn btn-primary" @click="handleSub(item)">-</button>
          {{ item.count }}
          <button class="btn btn-primary" @click="handlePlus(item)">+</button>
        </div>
        <div class="amount">{{ item.price * item.count }}</div>
        <div class="operate">
          <button @click="handledelete(index)">刪除</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      list: [
        {
          id: "2062",
          name: "Miss Dior 淡香水",
          price: 2900,
          thumb:
            "https://s5.pimg.tw/album/styleme/element/16810585_1450092930-1717385843/sresize/380x380.jpg",
          count: "1",
        },
        {
          id: "832",
          name: "All in one 亮彩膏",
          price: 1350,
          thumb:
            "https://s7.pimg.tw/album/styleme/element/89173767_1485853372-1511782940/sresize/380x380.jpg",
          count: "1",
        },
        {
          id: "16762",
          name: "超放電晶潤雙色唇膏",
          price: 850,
          thumb:
            "https://s8.pimg.tw/album/styleme/element/89516838_1486096498-3741399352/sresize/380x380.png",
          count: "1",
        },
        {
          id: "145",
          name: "奇蹟活源精露",
          price: 2100,
          thumb:
            "https://s.pimg.tw/album/styleme/element/62038610_1471836809-2423849843/sresize/380x380.jpg",
          count: "1",
        },
        {
          id: "16717",
          name: "奇蹟活源精露",
          price: 2100,
          thumb:
            "https://s1.pimg.tw/album/styleme/element/88472691_1485277468-753072152/sresize/380x380.png",
          count: "1",
        },
        {
          id: "103",
          name: "星鑽漾采眼影",
          price: 2600,
          thumb:
            "https://s.pimg.tw/album/styleme/element/62032760_1471833970-3752241194/sresize/380x380.jpg",
          count: "1",
        },
      ],
    };
  },
  methods: {
    handlePlus: function (item) {
      console.log(item);
      item.count++;
    },
    handleSub: function (item) {
      console.log(item);
      if (item.count > 1) {
        item.count--;
      }
    },
    handledelete: function (index) {
      this.list.splice(index,1);
    },
  },
};
</script>