
# Vue Elements by LITS

A library for quick website development and works with bootstrap.

## LitsBootstrapNavbar

This is the navbar element and has some properties which we can use easily.

```bash
  <LitsBootstrapNavbar :options="options"></LitsBootstrapNavbar>
```

Add options object inside of script.

```bash
options : {
    title: "Title",
    container: "container",  // container | container-fluid
    navBg: "bg-primary",
    navMode: "navbar-dark", // navbar-dark | navbar-light
    brandClasses: "h3",     // try classes
    linkClasses: "",
    menuClasses: "",
    listClasses: "",
    expand: "navbar-expand-lg",
    logo: {
        src: "",
        alt: "",
        width: "",
        height: "",
        show: false,        // true | false
    },
    links: [
        {
            text: "Home",
            to: "/path",
            dropdown: [],   // Array of links if need dropdown
        }
    ],
};
```
## Special Thanks

 - [Leena IT Solutions](https://leenaitsolutions.com)
 - [README](https://github.com/sandeep8558)

 
 ## Authors

- [@sandeep8558](https://github.com/sandeep8558)
- [@leenaa-28](https://github.com/leenaa-28)
- [Sandeep Rathod](https://svrathod.com)