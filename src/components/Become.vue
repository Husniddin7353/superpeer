<template>
    <div class="become">
        <img class="become-animation" src="@/assets/animation2.png" alt="">

        <div class="container">
            <img class="become-img" src="@/assets/hand.png" alt=""><br>
            <img class="become-img" src="@/assets/become.png" alt=""><br>

            <button class="become-btn btn">
                Create Account
            </button>
        </div>

    </div>
</template>

<script>
export default {
    name:'Become'
}
</script>

<style lang="scss">
.become{
    position: relative;
    text-align: center;
    overflow: hidden;
    &-animation{
        position: absolute;
        z-index: -1;
        left: 0;
        bottom: 0;
        top: 0;
        right: 0;
        animation-name: myanimation;
        animation-duration: 5s;
        animation-iteration-count: infinite;
        @keyframes myanimation {
        0%   {
            -webkit-transform: scale(1);
            -moz-transform: scale(1);
            -o-transform: scale(1);
            -ms-transform: scale(1);
            transform: scale(1)
        }
        50%  {
            -webkit-transform: scale(2);
            -moz-transform: scale(2);
            -o-transform: scale(2);
            -ms-transform: scale(2);
            transform: scale(2)
        }
        100%  {
            -webkit-transform: scale(1);
            -moz-transform: scale(1);
            -o-transform: scale(1);
            -ms-transform: scale(1);
            transform: scale(1)
        }
        }
    }

    &-img{
        margin: 30px 0;
    }
}

@media screen and (max-width:980px) {
    .become{
        img{
            max-width: 100%;
        }
    }
}
</style>