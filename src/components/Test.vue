<template>
  <div class="hello">
   
   
    <h1>{{message}}</h1>
    <p>
      
      
    </p>
    <div>
      <input style="width: 100px; margin: 10px;" type="text" v-model="item">
    </div>
    <div>
      <button style="height: 20px; background-color: rgba(68, 227, 255, 0.268);" v-on:click="tg(item)">Проверить ответ</button>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'AppsVue',
  props: {
    
    
    
    
  },

  data() {
    return {
      count: 1,
      strCount: "123123",
      message: '',
    };
  },
  methods: { tg(mes) {
    if (mes.length > 1)
    {
      return this.message = ' ТЫ ИДИОТ СКАЗАНО ЖЕ ЧИСЛО ОТ 1 ДО 5!!!'
    }
    switch (mes) {
      case '1':
      return this.message = ' ТЫ ЛОХ!!!'
      
      case '2':
      return this.message = ' ТЫ ПИДОР!!!'

      case '3':
      return this.message = ' ТЫ ЧЕ СУКА МОРКОВНЫЙ СБЛЕВЫШ!!!'

      case '4':
      return this.message = ' ТЫ ХУЕЕД!!!'
      
      case '5':
      return this.message = ' ТЫ ГОВНОЕД!!!'
    // if (mes == 1){
    //   return this.message = ' ТЫ ЛОХ!!!'
      
    }
    console.log(this.count)
    
  }
  
  }
}

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
  color: #680be2;
}
</style>
