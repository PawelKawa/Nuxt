<template>
    <div>
        <header>
          <NuxtLogo />
            <nav>
              <NuxtLink to="/">Home</NuxtLink>
              <NuxtLink to="/about">About</NuxtLink>
              <NuxtLink to="/components">Components</NuxtLink>
              <NuxtLink to="/fetch">Fetch</NuxtLink>
              <NuxtLink to="/functions">Functions</NuxtLink>
            </nav>
            <p>BODY background color from main.css that need to be included in nuxt.config.js</p>
            <p>Body background color override by styles in pages functions.vue</p>
            <p>default layer ends here</p>
        </header>
        <Nuxt />
        <footer>
            <p>default layer starts here</p>
            <p>footer</p>
        </footer>
    </div>
  </template>
  
  <style scoped>

  header, footer{
    background-color: antiquewhite;
  }
  
  </style>