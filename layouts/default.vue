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
              <NuxtLink to="/quill">Quill</NuxtLink>
              <NuxtLink to="/ckeditor">Ckeditor</NuxtLink>
            </nav>
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