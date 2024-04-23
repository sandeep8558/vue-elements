<template>
    <!-- Navbar -->
    <div class="navbar">
        <div class="container shadow border my-2 py-2" :class="[container]" style="border-radius: 200px;">

            <a class="navbar-brand" href="/" style="width: 50px;">
                <div class="image image-cover image-s rounded-circle">
                    <img :src="logo" class="me-2" :alt="title">
                </div>
            </a>

            <div class="navbar-collapse collapse" id="navbarNavAltMarkup">
                <div class="navbar-nav ms-auto">

                    <a v-for="link,ind in links" :key="ind" class="btn-round ms-2 m-0" aria-current="page" target="_blank" :href="link.href" v-html="link.icon"></a>

                </div>
            </div>

        </div>
    </div>
</template>

<script lang="ts">
import { ref } from 'vue';

export default {

    props: ['options'],

    setup(props){

        const logo = ref("/images/lits.png");

        const container = ref("bg-light");

        const title = ref("Business");

        const links = ref([
            {
                icon: '<i class="bi bi-facebook"></i>',
                href: 'https://www.facebook.com'
            },
            {
                icon: '<i class="bi bi-twitter"></i>',
                href: 'https://twitter.com'
            },
        ]);

        if(props.options){

            if(props.options['logo']){
                logo.value = props.options['logo'];
            }

            if(props.options['container']){
                container.value = props.options['container'];
            }

            if(props.options['title']){
                title.value = props.options['title'];
            }

            if(props.options['links']){
                links.value = props.options['links'];
            }

        }

        return {
            logo,
            container,
            title,
            links,
        };
    },
}
</script>

<style scoped>
.btn-round {
    width: 50px !important;
    height: 50px !important;
    color: #333333 !important;
    text-align: center;
    line-height: 50px;
    font-size: 24px;
    transition: font-size .3s ease-in-out;
    backface-visibility: hidden;

}
.btn-round:hover {
    font-size: 40px;
}
</style>