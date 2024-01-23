<template>
  <div class="hello">
   
   
    <h1>{{message}}</h1>
    <p>
      
      
    </p>
    <div>
      <input style="width: 100px; margin: 10px;" type="text" v-model="item">
    </div>
    <div>
      <button class="glow-on-hover" v-on:click="tg(item)">Проверить ответ</button>
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
    console.log(mes?.length)
    if (mes?.length < 1 && mes == 0)
    {
      return this.message = ' ТЫ ЕБЛАН НИЧЕГО НЕ ВВЕЛ!!!'
    }
    else
    {
      if (mes?.length > 1)
      {
      return this.message = ' ТЫ ИДИОТ СКАЗАНО ЖЕ ЧИСЛО ОТ 1 ДО 5!!!'
      }
      else
      { 
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

      }
    }
    
    
    
    
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
.glow-on-hover {
    width: 220px;
    height: 50px;
    border: none;
    outline: none;
    color: #fff;
    background: #111;
    cursor: pointer;
    position: relative;
    z-index: 0;
    border-radius: 10px;
}

.glow-on-hover:before {
    content: '';
    background: linear-gradient(45deg, #ff0000, #ff7300, #fffb00, #48ff00, #00ffd5, #002bff, #7a00ff, #ff00c8, #ff0000);
    position: absolute;
    top: -2px;
    left:-2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    transition: opacity .3s ease-in-out;
    border-radius: 10px;
}

.glow-on-hover:active {
    color: #000
}

.glow-on-hover:active:after {
    background: transparent;
}

.glow-on-hover:hover:before {
    opacity: 1;
}

.glow-on-hover:after {
    z-index: -1;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: #111;
    left: 0;
    top: 0;
    border-radius: 10px;
}

@keyframes glowing {
    0% { background-position: 0 0; }
    50% { background-position: 400% 0; }
    100% { background-position: 0 0; }
}
</style>
