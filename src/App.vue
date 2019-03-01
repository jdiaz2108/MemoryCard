<template>
  <div id="app" class="container-fluid mx-0 px-0">
<header class="position-static p-1  mb-5"  style="background-color: #f2f2f2">
    <div class="container">
        <div class="row">
    <div class="col-sm my-auto">
      <h3 style="color: #ff0000">DIPLOMADO GESTIONANDO TU CANAL</h3>
    </div>
    <div class="col-sm">
      <img src="dist/universidad.png" class="img-fluid float-right" style="width: 100px" alt="">
    </div>
  </div>
    </div>
    
</header>

<div class="my-auto container-fluid">
    <div class="row">
        <div class="col-12">
    <section class="memory-game">
<!--         <div class="memory-card border border-light" :class="{flip: isActive}" @click="flipCard()">
            <img :src="back" class="front-face" alt="">
            <img src="./assets/casa-front.jpg" class="back-face" alt="">
        </div>

        <div class="memory-card border border-light" :class="{flip: isActive}" @click="flipCard()">
            <img src="./assets/logo-back.jpg" class="front-face" alt="">
            <img src="./assets/letra-front.jpg" class="back-face" alt="">
        </div> -->
 
        <div class="memory-card" v-for="(card, index) in cards" :class="{flip: card.isActive}" @click="flipCard2(card, index)" >
            <img :src="back" class="front-face shadow rounded" alt="">
            <img :src="card.image" class="back-face  shadow rounded" alt="">
        </div>

    </section>
    </div>
    </div>
</div>
<!--     <div class="container">
            <div class="row">
            <div class="col border position-relative memory-card m-2" :class="{flip: isActive}"  @click="flipCard()">
                <img src="./assets/logo-back.jpg" class="front-face" alt="">
                <img src="./assets/casa-front.jpg" class="back-face" alt="">
            </div>
            <div class="col">
                             <div class="bg-danger  position-absolute">
                  <h5 class="card-title ">Primary card title</h5>
                  <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                </div>

                <div class="bg-success position-absolute">
                  <h5 class="card-title">bg success card title</h5>
                  <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                </div>
            </div>
            <div class="col">
              3 of 3
            </div>
        </div>
    </div> -->


<!--     <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <ul>
      <li><a href="https://vuejs.org" target="_blank">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank">Twitter</a></li>
    </ul>
    <h2>Ecosystem</h2>
    <ul>
      <li><a href="http://router.vuejs.org/" target="_blank">vue-router</a></li>
      <li><a href="http://vuex.vuejs.org/" target="_blank">vuex</a></li>
      <li><a href="http://vue-loader.vuejs.org/" target="_blank">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank">awesome-vue</a></li>
    </ul> -->
    <footer class="position-static p-4 mt-5" style="background-color: #f2f2f2">
        <div class="container-fluid">
            <div class=" text-center ">
            <img src="dist/escuela.png" alt="">
            </div>
        </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app',
  created(){
    this.randi();
  },
  mounted(){
    this.randi();
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      isActive: false,
      back: './dist/atras.jpg',
      par1: {
        par: null,
        obj: null,
      },
      value: null,
      par2: {
        par: null,
        obj: null,
      },
      lockBoard: false,
      cards: [
          {
            id: 1,
            par: 1,
            nombre: 'casa',
            image: './dist/1.1.jpg',
            isActive: true,
            random: null
          },
          {
            id: 2,
            par: 1,
            nombre: 'casa',
            image: './dist/1.2.jpg',
            isActive: true,
            random: null
          },
          {
            id: 3,
            par: 2,
            nombre: 'casa',
            image: './dist/2.1.jpg',
            isActive: true,
            random: null
          },
          {
            id: 4,
            par: 2,
            nombre: 'casa',
            image: './dist/2.2.jpg',
            isActive: true,
            random: null
          },
          {
            id: 5,
            par: 3,
            nombre: 'casa',
            image: './dist/3.1.jpg',
            isActive: true,
            random: null
          },
          {
            id: 6,
            par: 3,
            nombre: 'casa',
            image: './dist/3.2.jpg',
            isActive: true,
            random: null
          },
          {
            id: 7,
            par: 4,
            nombre: 'casa',
            image: './dist/4.1.jpg',
            isActive: true,
            random: null
          },
          {
            id: 8,
            par: 4,
            nombre: 'casa',
            image: './dist/4.2.jpg',
            isActive: true,
            random: null
          },
          {
            id: 9,
            par: 5,
            nombre: 'casa',
            image: './dist/5.1.jpg',
            isActive: true,
            random: null
          },
          {
            id: 10,
            par: 5,
            nombre: 'casa',
            image: './dist/5.2.jpg',
            isActive: true,
            random: null
          },
          {
            id: 11,
            par: 6,
            nombre: 'casa',
            image: './dist/6.1.jpg',
            isActive: true,
            random: null
          },
          {
            id: 12,
            par: 6,
            nombre: 'casa',
            image: './dist/6.2.jpg',
            isActive: true,
            random: null
          },
          {
            id: 13,
            par: 7,
            nombre: 'casa',
            image: './dist/7.1.jpg',
            isActive: true,
            random: null
          },
          {
            id: 14,
            par: 7,
            nombre: 'casa',
            image: './dist/7.2.jpg',
            isActive: true,
            random: null
          },
          {
            id: 15,
            par: 8,
            nombre: 'casa',
            image: './dist/8.1.jpg',
            isActive: true,
            random: null
          },
          {
            id: 16,
            par: 8,
            nombre: 'casa',
            image: './dist/8.2.jpg',
            isActive: true,
            random: null
          },
      ]
    }
  },
  methods: {
        randi: function () {
            console.log(this.cards.length);
            for (var i = 0; i < this.cards.length; i++) {
                this.cards[i].random = Math.random() * 12;
              console.log(this.cards[i].id);
            }
                this.cards.sort(function(a, b) {
    return parseFloat(b.random) - parseFloat(a.random);
});
          },
    flipCard: function(val, de) {

        if (this.isActive == false) {this.isActive = true}
            else {this.isActive = false;}
        
        console.log('i was clicked');
        console.log(this);
    },
    flipCard2: function(val, de) {
        // val.isActive == true ? val.isActive = false : val.isActive = true;
        if(this.lockBoard) return;
        if(val.isActive == true) {
            val.isActive = false;
            if (this.par1.par == null) { 
                    this.par1 = {
                        par: val.par,
                        obj: de
                    }
                }
            // else if (this.par2.par == null) { 
            //     this.par2.par = val.par;
            //     if (this.par1.par != this.par2.par) {
            //         this.par1.par = null;
            //         this.par2.par = null;
            //     }
            // }
            else {
                this.lockBoard = true;

                if (this.par1.par != val.par) {
                    this.par2 = {
                        par: val.par,
                        obj: de
                    }
                    var self = this;
                    setTimeout(function(){
                        self.cards[self.par1.obj].isActive = true;
                        self.cards[self.par2.obj].isActive = true;
                    self.par1 = {
                        par: null,
                        obj: null
                    },
                    self.par2 = {
                        par: null,
                        obj: null
                    },
                    self.lockBoard = false;
                    }, 1500);
                } else {
                    this.par1 = {
                        par: null,
                        obj: null
                    },
                    this.par2 = {
                        par: null,
                        obj: null
                    },
                    this.lockBoard = false;
                }
            }
        }
       
        console.log('i was clicked');
        console.log(de);
    }
  }
}
</script>

<style>
body {
    height: 100vh;
    display: flex;
    background-color: #fff;
}

.memory-game {
    width: 1800px;
    height: 650px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    perspective: 1000px;
}

.memory-card {
    width: calc(12.5% - 10px);
    height: 45%;
    position: relative;
    margin: 5px;
    transform: scale(1);
    transform-style: preserve-3d;
    transition: transform .5s;
}

.img {
    width: 100px;
}

.row {
    perspective: 1000px;
}


.memory-card:active {
    transform: scale(.97);
    transition: transform .2s;
}

.memory-card.flip {
    transform: rotateY(180deg);
}

.front-face,
.back-face {
    width: 100%;
    height: 100%;
    position: absolute;
    padding: 10px;
/*    border: 2px solid lime;*/
    backface-visibility: hidden;
}

.front-face {
    transform: rotateY(180deg);
}
</style>
