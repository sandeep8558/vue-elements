<template>
    <div class="shadow">
        
        <div class="container-fluid pt-5" :class="[bg1]">
            <div class="container">
                <div class="row">
    
                    <div class="col-12 col-lg-5 mb-5" :class="[text1]">
                        <h6 class="fw-bold text-uppercase" :class="[texttitle]">{{ title }}</h6>
                        <hr class="w-25 border-3" :class="[border]">
                        <p class="">{{ description }}</p>
                    </div>
    
                    <div class="col-12 col-lg-3 mb-5" :class="[text1]">
                        <h6 class="fw-bold text-uppercase" :class="[texttitle]">Best of us</h6>
                        <hr class="w-25 border-3" :class="[border]">
                        <p v-for="link, ind in links" :key="ind"><router-link class="nav-link ms-2" :to="link.to">{{ link.text }}</router-link></p>
                    </div>
    
                    <div class="col-12 col-lg-4 mb-5" :class="[text1]">
                        <h6 class="fw-bold text-uppercase" :class="[texttitle]">Get in touch</h6>
                        <hr class="w-25 border-3" :class="[border]">
                        <p class=""><i class="bi bi-geo me-3"></i> {{ address }}</p>
                        <p class=""><i class="bi bi-envelope-at me-3"></i> {{ email }}</p>
                        <p class=""><i class="bi bi-telephone me-3"></i> {{ phone }}</p>
                        <p class="">
                            <a v-for="soc, ind in social" :key="ind" class="btn btn-clear ps-0 me-2 border-0" :class="[text1]" target="_blank" :href="soc.href" v-html="soc.icon"></a>
                        </p>
                    </div>
    
                </div>
            </div>
        </div>

        <div class="container-fluid p-2" :class="[bg2]">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <router-link v-for="blin, ind in bottomlinks" :key="ind" class="btn btn-sm btn-clear border-0" :class="[text2]" :to="blin.to">
                            <span class="small">{{ blin.text }}</span>
                        </router-link>
                    </div>
                    <div class="col-auto">
                        <a class="btn btn-sm btn-clear border-0" :class="[text2]" target="_blank" href="https://leenaitsolutions.com"><small>Developed By LITS</small></a>
                    </div>
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

        const year = ref(new Date().getFullYear());
        const title = ref("Title");
        const description = ref("Lorem ipsum dolor, sit amet consectetur adipisicing elit. Rem nam rerum fugit nisi optio, eum expedita voluptatum dicta assumenda eaque.");
        const address = ref("Mumbai Maharashtra India");
        const phone = ref("Phone");
        const email = ref("Email");
        const bg1 = ref("bg-dark");
        const bg2 = ref("bg-light");
        const texttitle = ref("text-warning");
        const text1 = ref("text-light");
        const text2 = ref("text-dark");
        const border = ref("border-warning");
        const social = ref([
            {
                icon: '<i class="bi bi-facebook"></i>',
                href: 'https://www.facebook.com',
            },
            {
                icon: '<i class="bi bi-instagram"></i>',
                href: 'https://www.instagram.com',
            },
        ]);
        const links = ref([
            {
                text: 'Home',
                to: '/',
            },
            {
                text: 'About us',
                to: '/',
            },
        ]);
        const bottomlinks = ref([
            {
                text: 'Terms & Conditions',
                to: '/',
            },
            {
                text: 'Privacy',
                to: '/',
            },
        ]);


        if(props.options){

            if(props.options['title']){
                title.value = props.options['title'];
            }

            if(props.options['description']){
                description.value = props.options['description'];
            }

            if(props.options['address']){
                address.value = props.options['address'];
            }

            if(props.options['phone']){
                phone.value = props.options['phone'];
            }

            if(props.options['email']){
                email.value = props.options['email'];
            }

            if(props.options['bg1']){
                bg1.value = props.options['bg1'];
            }

            if(props.options['bg2']){
                bg2.value = props.options['bg2'];
            }

            if(props.options['border']){
                border.value = props.options['border'];
            }

            if(props.options['texttitle']){
                texttitle.value = props.options['texttitle'];
            }

            if(props.options['text1']){
                text1.value = props.options['text1'];
            }

            if(props.options['text2']){
                text2.value = props.options['text2'];
            }

            if(props.options['social']){
                social.value = props.options['social'];
            }

            if(props.options['links']){
                links.value = props.options['links'];
            }

            if(props.options['bottomlinks']){
                bottomlinks.value = props.options['bottomlinks'];
            }

        }


        return {
            year,
            title,
            description,
            address,
            phone,
            email,
            bg1,
            bg2,
            border,
            texttitle,
            text1,
            text2,
            social,
            links,
            bottomlinks,
        };

    },

}
</script>