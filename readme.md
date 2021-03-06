# NUXT JS (https://distracted-bartik-b0f511.netlify.com/)
> Nuxt.js project [Nuxt.js docs](https://github.com/nuxt/nuxt.js)

![NUXT JS HOW IT WORKS](https://nuxtjs.org/nuxt-schema.png)



#### Install Vue Command Line Interface Globally.
```bash
$ npm install -g vue-cli

```

#### Install Nuxt.js.
```bash

$ vue init nuxt/starter project-name
$ cd project-name 
$ npm run dev

```
#### Creating a Mater Page.
Master layout will will be inherited by all our pages(`layout\default.vue`).
```
<template>
    <div>
        <navbar></navbar>
        <nuxt/>
    </div>
</template>
<script>
    import Navbar from '../components/Navbar.vue'

    export default {
        components: {
            Navbar
        }
    }
</script>

<style>
    html {
        font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
    }
</style>
```    
Here the `<nuxt/>` tag is dynamic which will help us render each page in our app.  
**To create different pages(contact,home,about)** add your pages to `pages` directory in the root folder.
The nuxt.js will automatically create a route to open each of your page eg: **if the name of our page is about.vue nuxt will create a route /about automatically**
  
  
Here we are also import the `Navbar` component in the master layout.
    
Checkout the `nuxt.config.js` which can be found in project root directory this is the config for our nuxt.js app
**You can edit the global html content like css links, title, meta etc in here**
> Here we have added a google font and bulma css framework into our project



### Build Project
``` bash
$ npm run generate (The command above will run nuxt generate which will in turn start building the application and generate the static files in the dist folder.)
```

### Deploying (https://distracted-bartik-b0f511.netlify.com/)
This site has been deployed in  [Netlify](https://app.netlify.com)
1) Login to netlify
2) Click the `New site from Git` button
3) Complete the 3 Steps.
    1) Select Git hub account
    2) Select Project and folder to be diployed in github.
    3) Select Repo > build command (`npm run generate`) > publish directory (dist) 
    4) Deploy Site button to deploy

### Install This Project.
``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

