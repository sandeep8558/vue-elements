
# Vue Elements by LITS

A library for quick website development and works with bootstrap.
## LitsBootstrapNavbar

This is the navbar element and has some properties which we can use easily.

```bash
  <LitsBootstrapNavbar :options="options" class="navbar-expand-lg navbar-dark bg-primary sticky-top"></LitsBootstrapNavbar>
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

### Title
```bash
title: "Title",
```

### Container (container, container-fluid)
```bash
container: "container",
```

### Title Classes
```bash
brandClasses: "h3",
```

### Link Classes
```bash
linkClasses: "",
```

### Menu Classes
```bash
menuClasses: "",
```

### List Classes
```bash
listClasses: "",
```

### Logo
```bash
logo: {
    src: "",
    alt: "",
    width: "",
    height: "",
    show: false,        // true | false
},
```

### Pages Links
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
  <LitsProfileNavbar :options="options" class="sticky-top p-2 navbar-expand navbar-light bg-white"></LitsProfileNavbar>
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
### Title
```bash
title: "Title",
```

### Logo
```bash
logo: "path to image",
```

### Container (Add classes to Round bordered container).
```bash
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
## Special Thanks

 - [Leena IT Solutions](https://leenaitsolutions.com)
 - [README](https://github.com/sandeep8558)
 ## Authors

- [@sandeep8558](https://github.com/sandeep8558)
- [@leenaa-28](https://github.com/leenaa-28)
- [Sandeep Rathod](https://svrathod.com)