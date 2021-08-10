<template>
    <div class="foryou">
        <svg class="foryou-linier" width="1440" height="52" viewBox="0 0 1440 52" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M1440 16.4838L1440 52L0 51.9999L3.38454e-06 13.2852C20.0501 15.4339 43.76 19.113 71.65 24.8623C217.08 54.8451 446.31 31.4554 628.85 7.24164C757.08 -9.77081 880.38 6.25074 1015.8 23.8421C1073.14 31.2887 1132.65 39.0199 1195.63 44.6416C1293.8 53.403 1378.1 37.4795 1440 16.4838Z" fill="#FDE6E6"/>
        </svg>

        <div class="container">
            <h1 class="foryou-title">
                What can Superpeer do for you?
            </h1>

            <p class="foryou-text">
                Turn your audience into loyal, paying followers with our seamless video experience and subscriber management tools.
            </p>

            <div class="foryou-blog">
                <div class="foryou-blog_item" v-for="(item, index) in foryou" :key="index">
                    <img :src="item.img" alt="">
                    <p class="foryou-blog_item__title">
                       {{item.title}} 
                    </p>
                    <p class="foryou-blog_item__text">
                        {{item.text}}
                    </p>
                </div>
            </div>

            <button class="foryou-btn btn">All Features</button>
        </div>
    </div>
</template>

<script>
export default {
    name:'Foryou',

    props:[
        "foryou"
    ]
}
</script>

<style lang="scss" scoped>
 .foryou{
     margin-top:40%;
     position: relative;
     background: linear-gradient(180deg, #FDE6E6 0%, #FFFFFF 100%);
     text-align: center;
    &-linier{
        position: absolute;
        left: 0;
        top:-3rem;
        z-index: -1;
        overflow: hidden;
        width: 100%;
    }

    &-title{
        font-weight: bold;
        font-size: 48px;
        line-height: 53px;
        text-align: center;
        letter-spacing: 1px;
        color: #222222;
        padding: 130px 0 30px 0;
    }

    &-text{
        font-size: 18px;
        line-height: 25px;
        text-align: center;
        color: #222222;
        max-width: 588px;
        margin: 0 auto;
    }

    &-blog{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        &_item{
            margin: 50px 0;
            text-align: center;
            cursor: pointer;
            border: none;
            border-radius: 20px;
            &:hover{
                box-shadow: 0 10px 10px 10px #ffd43867;
                transition: all 0.2s;
            }
            &__title{
                font-size: 22px;
                line-height: 29px;
                text-align: center;
                color: #222222;
                margin: 24px 0 12px 0;
            }
            &__text{
                font-size: 16px;
                line-height: 22px;
                text-align: center;
                color: #555555;
                max-width: 266px;
                margin: 0 auto;
            }
        }
    }
    .btn{
        background: #FFEDC2;
        border-radius: 8px;
        text-transform: uppercase;
        color: #222222;
        padding: 15px 30px;
        &:hover{
            background: #FFD338 
        }
    }


}

@media screen and (max-width:980px) {
    .foryou-blog{
        display: flex;
        flex-direction: column;
    }
}
</style>