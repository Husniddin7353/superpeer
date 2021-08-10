<template>
  <div class="slider">
      <div class="container">

          <h1 class="slider-title">
              Don’t just take our word for it
          </h1>
        <VueSlickCarousel class="slider-carousel" :arrows="true" :dots="false" v-bind="settings">
            <p class="text" v-for="(item, index) in slider" :key="index">
                {{item.text}}
            </p>
        </VueSlickCarousel>
        <img class="slider-profile" src="@/assets/just.png" alt="">
        <p class="slider-name">
            Janine Sickmeyer
        </p>

        <p class="slider-position">
            Tech entrepreneur & Angel investor
        </p>
      </div>
    
  </div>
</template>
 
<script>
  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
 
  export default {
    name: 'Slider',
    components: { VueSlickCarousel },

    props:[
        "slider"
    ],

    setting:{
    "arrows" : false , 
    "dots": false,
    "arrowsClass": "slick-arrow custom-arrow-class",
    "edgeFriction": 0.35,
    "infinite": true,
    "speed": 500,
    "slidesToShow": 4,
    "slidesToScroll": 4
    }
  }
</script> 

<style lang="scss">
.slider{
    margin: 100px 0;
   .container{
        background: linear-gradient(180deg, #FFFAEC 0%, rgba(255, 255, 255, 0) 100%);
   }
    text-align: center;
    &-title{
        font-size: 48px;
        line-height: 53px;
        text-align: center;
        letter-spacing: 1px;
        color: #222222;
        padding: 99px 0;
    }

    &-carousel{
        max-width: 776px;
        margin: 0 auto;
        .text{
            font-size: 32px;
            line-height: 40px;
            text-align: center;
            color: #222222;
            max-width: 725px;
            margin: 0 auto;
        }
    }

    &-name{
        font-size: 16px;
        line-height: 22px;
        text-align: center;
        color: #222222;
    }

    &-position{
        font-size: 12px;
        line-height: 17px; 
        text-align: center;
        color: #222222;
    }

    &-profile{
        margin: 88px 0 16px 0;
    }
    
    
        
}
.slick-arrow{
        padding: 30x;
        max-width: 30px;
        background:#EEEEEE ;
        &::before{
            color: #EEEEEE;
            border-radius: 27px;
            background: rgb(185, 184, 184);
            
        }

    
}
</style>