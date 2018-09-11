<template>
  <transition name="slide-down">
            <div class="title-wrapper" v-show="ifTitle">
                <div class="left">
                    <span class="icon-arrow-left2 icon"></span>
                </div>
                <div class="right">
                    <div class="icon-wrapper">
                        <span class="icon-cart icon"></span>
                    </div>
                    <div class="icon-wrapper">
                        <span class="icon-accessibility icon"></span>
                    </div>
                    <div class="icon-wrapper">
                        <span class="icon-cog icon"></span>
                    </div>
                </div>
            </div>
        </transition>
</template>

<script>
export default {
    props:{
        ifTitle:{
            type:Boolean,
            default:false
        }
    }
}

</script>
<style lang='scss' scoped>
@import '../assets/styles/global';
.title-wrapper {
        position: absolute;
        top:0;
        left:0;
        width:100%;
        display:flex;
        height:px2rem(48);
        z-index: 101;
        background: white;
        box-shadow: 0 px2rem(8) px2rem(8) rgba(0,0,0,0.15);
        
        .left{
            flex:0 0 px2rem(60);
            @include center;
        }
        .right{
            flex:1;
            display:flex;
            justify-content: flex-end;
            .icon-wrapper{
                flex:0 0 px2rem(40);
                @include center;
            }
        }
    }
</style>