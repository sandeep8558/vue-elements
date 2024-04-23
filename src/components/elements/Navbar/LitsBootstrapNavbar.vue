<template>
    
    <nav class="navbar">
        <div class="" :class="container">

            <!-- Brand -->
            <a class="navbar-brand" :class="[brandClasses]" href="/">
                <img v-if="logo.show" :src="logo.src" :alt="logo.alt" :width="logo.width" :height="logo.height" class="me-2">
                {{ title }}
            </a>

            <!-- Toggle Button -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav" :class="[menuClasses]">
                    
                    <li v-for="link in links" :key="link.to" class="nav-item" :class="[listClasses, link.dropdown ? 'dropdown' : '']">

                        <router-link v-if="link.to" class="nav-link" :class="linkClasses" aria-current="page" :to="link.to">{{ link.text }}</router-link>

                        <a v-if="link.dropdown" class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                            {{ link.text }}
                        </a>

                        <ul  v-if="link.dropdown" class="dropdown-menu dropdown-menu-light">
                            <li v-for="dm, ind in link.dropdown" :key="ind"><router-link class="dropdown-item" :to="dm.to">{{ dm.text }}</router-link></li>
                        </ul>

                    </li>

                </ul>

            </div>
        </div>
    </nav>

</template>

<script lang="ts">
import { onMounted, ref } from 'vue';

export default {

    props: ['options'],

    setup(props){

        const title = ref("Business Name");

        const container = ref("container-fluid");

        const logo = ref({
            src: "",
            alt: "",
            width: "32",
            height: "32",
            show: false
        });

        const brandClasses = ref("");

        const linkClasses = ref("");

        const menuClasses = ref("ms-auto mb-lg-0");

        const listClasses = ref("");

        const links = ref([
            {
                text: "Home",
                to: '/'
            },
            {
                text: "About",
                dropdown: [
                    {
                        text: "Home",
                        to: '/'
                    },
                ]
            },
        ]);

        if(props.options){

            title.value = (props.options['title'] != null) ? props.options['title'] : '';

            if(props.options['logo']){
                if(props.options['logo'].show){
                    if(props.options['logo']['src']){
                        logo.value.src = props.options['logo']['src'];
                    }
                    if(props.options['logo']['alt']){
                        logo.value.alt = props.options['logo']['alt'];
                    }
                    if(props.options['logo']['width']){
                        logo.value.width = props.options['logo']['width'];
                    }
                    if(props.options['logo']['height']){
                        logo.value.height = props.options['logo']['height'];
                    }
                    if(props.options['logo']['show']){
                        logo.value.show = props.options['logo']['show'];
                    }
                }
            }

            if(props.options['container']){
                container.value = props.options['container'];
            }

            if(props.options['links']){
                links.value = props.options['links'];
            }

            if(props.options['brandClasses']){
                brandClasses.value = props.options['brandClasses'];
            }

            if(props.options['linkClasses']){
                linkClasses.value = props.options['linkClasses'];
            }

            if(props.options['listClasses']){
                listClasses.value = props.options['listClasses'];
            }

            if(props.options['menuClasses']){
                menuClasses.value = props.options['menuClasses'];
            }

        }
        

        onMounted:{
        };

        return {
            title,
            logo,
            container,
            links,
            brandClasses,
            linkClasses,
            menuClasses,
            listClasses,
        };

    },

};
</script>