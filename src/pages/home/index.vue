<template>
<div>
    <div id="home" class="page">
        <home-header/>
        <home-menu/>

        <keep-alive>
            <router-view class="home-content"/>
        </keep-alive>

    </div>
    <transition enter-active-class="slideInRight" leave-active-class="slideOutRight">
        <router-view name="subpage"/>
    </transition>

</div>
</template>

<script>
import homeHeader from '@components/home/home-header'
import homeMenu from '@components/home/home-menu'
export default {
    components: {
        homeHeader,
        homeMenu
    }
}
</script>

<style lang="scss" scoped>
.home-content{
    width: 100%;
    position: absolute;
    top: 71px;
    left: 0;
    bottom: 0;
    overflow: hidden;
}

</style>

