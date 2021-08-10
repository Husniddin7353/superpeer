<template>
    <div class="magic">
        <svg class="linier" width="1422" height="152" viewBox="0 0 1422 152" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M1457 48.1832L1457 152L-13 152L-13 38.8338C7.46772 45.1145 31.6717 55.869 60.1427 72.6747C208.602 160.317 442.608 91.9468 628.951 21.1678C759.852 -28.561 885.721 18.2713 1023.96 69.6922C1082.5 91.4593 1143.25 114.058 1207.54 130.491C1307.75 156.101 1393.81 109.556 1457 48.1832Z" fill="#FFF7E0"/>
            
        </svg>

        <div class="container">
            <h1 class="magic-title ">
                See what magic our community is creating
            </h1>

            <p class="magic-text">
                Explore these examples of Series, created by our Superpeers, and reserve your spot today
            </p>

            <div class="magic-blog">
                <div class="magic-blog__item" v-for="(item, index) in magic" :key="index">
                    <div class="item-img">
                        <img class="item-img__main" :src="item.img"  alt="">
                        <img class="item-img__profile" :src="item.profile"  alt="">
                    </div>

                    <h3 class="magic-blog__item_title">
                        {{ item.title }}
                    </h3>

                    <p class="magic-blog__item_name">
                        {{ item.name }}
                    </p>

                    <p class="magic-blog__item_text">
                        {{ item.text }}
                    </p>

                    <div class="magic-blog__item_date"> Start <span> {{ item.date }}</span>  
                        <button class="btn" @click="toggleClick(item)"> {{ item.btn ? 'Notify me' : 'enrolled' }}</button>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>
<script>
export default {
    name:'Magic',
    props: [
        "magic"
    ],

    data: function () {
        return {
            text: 'Notify me',
            active: false
        }
    },
    methods: {
        toggleClick(d) {
            d.btn =! d.btn
        }
    },
	render: function(h) {
		return h(
			'button', {
				attrs: { class: this.active ? 'active' : ''},
				on: { click: this.toggleClick}
			},
			[ this.text ]
		)
	}
}

</script>

<style lang="scss" scoped>
.magic{
    background: linear-gradient(180deg, #FFF7E0 0%, #FFFFFF 100%);
    position: relative;
    
    .linier{
        position: absolute;
        left: 0;
        top:-9rem;
        z-index: -1;
        overflow: hidden;
        width: 100%;
    }

    &-title{
        padding: 100px 0 14px 0; 
        max-width: 540px;
        margin: 0 auto;
        font-weight: bold;
        font-size: 48px;
        line-height: 53px;
        text-align: center;
        letter-spacing: 1px;
        color: #222222;
    }
    &-text{
        font-size: 18px;
        line-height: 25px;
        text-align: center;
        color: #222222;
        max-width: 507px;
        margin: 0 auto;
    }

    &-blog{
        display: grid;
        grid-template-columns: 1fr 1fr;

       &__item{
           text-align: center;
           margin: 50px 0;
            .item-img{
                position: relative;

                &__profile{
                    position: absolute;
                    bottom: -20%;
                    left: 40%;
                    justify-content: center;
                }
            }

            &_title{
                font-size: 22px;
                line-height: 29px;
                text-align: center;
                color: #222222;
                margin: 47px auto 14px auto;
                max-width: 402px;
                
            }

            &_text{
                font-size: 16px;
                line-height: 22px;
                text-align: center;
                color: #555555;
                margin: 17px auto 21px auto;
                max-width: 402px;
            }

            &_name{
                font-size: 16px;
                line-height: 22px;
                text-align: center;
                color: #555555;
            }

            &_date{
                font-size: 16px;
                line-height: 22px;
                text-align: center;
                color: #98A3B6;

                span{
                    color: #000000;
                    margin: 0 16px 0 8px;
                }

                .btn{
                    background: #FFEDC2;
                    border-radius: 8px;
                    text-transform: uppercase;
                    color: #222222;
                    padding: 15px 30px;
                }

                .btn.active{
                    background: #FFD338 ;
                    padding: 15px 30px;
                    border-radius: 8px;
                    max-width: 141px;
                    margin: 0 auto;
                    width: 100%;
                }
            }
       }
    }
}

@media screen and (max-width:980px){
 .magic-blog{
     display: flex;
     flex-direction: column;
 }   

 .item-img__main{
     max-width: 100%;
 }
}
</style>