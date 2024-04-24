
# Vue Elements by LITS

A library for quick website development and works with bootstrap.
## How To Use

```bash
<script lang='ts'>
import { LitsBootstrapNavbar, LitsSimpleFooter } from 'lits-vue-elements/components/elements';  // Enter Correct Path

export default {

    components: {
        LitsBootstrapNavbar,
        LitsSimpleFooter
    },

    setup(){
    
        NavOptions : {
            title: "Title",
        };

        FooterOptions : {
            title: "Title",
        };

    }
}
</script>

<template>
    <div>
        <LitsBootstrapNavbar :options="NavOptions"></LitsBootstrapNavbar>
        <LitsSimpleFooter :options="FooterOptions"></LitsSimpleFooter>
    </div>
</template>
```
## LitsBootstrapNavbar

This is the navbar element and has some properties which we can use easily.

```bash
  <LitsBootstrapNavbar :options="options"></LitsBootstrapNavbar>
```

Example Code for Bootstrap Navbar

```bash
options : {
    title: "Title",
    container: "container", 
    links: [
        {
            text: "Home",
            to: "/",
        }
    ],
};
```

### Simple Properties
```bash
title: "Title",
container: "container",
brandClasses: "h3",
linkClasses: "",
menuClasses: "",
listClasses: "",
```

### Logo Property
```bash
logo: {
    src: "",
    alt: "",
    width: "",
    height: "",
    show: false,        // true | false
},
```

### Pages Links Property
```bash
links: [
    {
        text: "Home",
        to: "/path",
    },
    {
        text: "Products",
        dropdown: [],   // Array of links if need dropdown
    }
],
```
## LitsProfileNavbar

This is the profile navbar element and has some properties which we can use easily.

```bash
  <LitsProfileNavbar :options="options"></LitsProfileNavbar>
```

Example Code for Profile Navbar

```bash
options : {
    title: "Title",
    logo: "path",
    container: "",
    links: [
        {
            icon: "<i class="bi bi-facebook"></i>",
            href: "https://facebook.com",
        }
    ],
};
```
### Simple Properties
```bash
title: "Title",
logo: "path to image",
container: "",
```

### Links (array of object)
```bash
links: [
    {
        icon: "<i class="bi bi-facebook"></i>",
        href: "https://facebook.com",
    }
],
```
## LitsSimpleFooter

This is a simple footer which is most commanly used by many developers.
```bash
<LitsSimpleFooter :options="options"></LitsSimpleFooter>
```

### Simple Properties
```bash
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
```

### Array Properties
```bash
social: [
    {
        icon: '<i class="bi bi-facebook"></i>',
        href: 'https://www.facebook.com',
    },
],

links: [
    {
        text: "Home",
        to: "/path",
    },
],

bottomlinks: [
    {
        text: "Home",
        to: "/path",
    },
],
```
## Special Thanks

 - [Leena IT Solutions](https://leenaitsolutions.com)
 - [README](https://github.com/sandeep8558)
 ## Authors

- [@sandeep8558](https://github.com/sandeep8558)
- [@leenaa-28](https://github.com/leenaa-28)
- [Sandeep Rathod](https://svrathod.com)