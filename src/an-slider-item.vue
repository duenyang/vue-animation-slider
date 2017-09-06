<template>
    <div class="an-slider-item" @click="animation">
        <transition :css="false" 
            :before-enter="beforeEnter" 
            :enter="enter" 
            :after-enter="afterEnter" 
            :enter-cancelled="enterCancelled" 
            :before-leave="beforeLeave" 
            :leave="leave" 
            :after-leave="afterLeave" 
            :leave-cancelled="leaveCancelled">
            <div class="box" v-show="show">
                <slot></slot>
            </div>
        </transition>
    </div>
</template>
<script>
export default {
    name: "an-slider-item",
    data() {
        return {
            show: true
        }
    },
    created() {

    },
    methods: {
        // --------
        // 进入中
        // --------
        beforeEnter: function(el) {
            // ...
            console.log('beforeEnter');
        },
        // 此回调函数是可选项的设置
        // 与 CSS 结合时使用
        enter: function(el, done) {
            // ...
            console.log('enter');
            done()
        },
        afterEnter: function(el) {
            // ...
            console.log('afterEnter');
        },
        enterCancelled: function(el) {
            // ...
            console.log('enterCancelled');
        },
        // --------
        // 离开时
        // --------
        beforeLeave: function(el) {
            // ...
            console.log('beforeLeave');
        },
        // 此回调函数是可选项的设置
        // 与 CSS 结合时使用
        leave: function(el, done) {
            // ...
            console.log('leave');
            done()
        },
        afterLeave: function(el) {
            // ...
            console.log('afterLeave');
        },
        // leaveCancelled 只用于 v-show 中
        leaveCancelled: function(el) {
            // ...
            console.log('leaveCancelled');
        },
        animation(){
            // document.querySelector('.box').style.transform = 'translateX(-100px)';
            this.show = !this.show;
        }
    },
    mounted() {

    }
}
</script>
<style scoped>
.an-slider-item,
.box {
    float: left;
    width: 100%;
    height: 100%;
    position: relative;
    overflow: hidden;
}
</style>

