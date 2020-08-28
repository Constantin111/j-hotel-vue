<template>
    <div>
        <swiper-desck v-if="userWidth > 770"></swiper-desck>
        <swiper-mob v-else></swiper-mob>
    </div>
</template>

<script>
    import SwiperDesck from "@/components/SwiperDesck";
    import SwiperMob from "@/components/SwiperMob";


    export default {
        name: "SwiperWrap",
        components: {SwiperMob, SwiperDesck},
        data(){
            return{
                userWidth: window.innerWidth,
            }
        },
        /*computed: {
            controluserwidth: function () {
                this.userWidth = document.body.clientWidth;
                return this.userWidth
            }

        },*/
    }
</script>

<style scoped>



</style>