<template>
  <div>
      <header>
        <NuxtLogo />
          <nav>
            <NuxtLink to="/">Home</NuxtLink>
            <NuxtLink to="/about">About</NuxtLink>
          </nav>
      </header>
      <p class="main">home</p>
  </div>
</template>

<style scoped>
header{
  background-color: antiquewhite;
  height: 10vh;
}
.main{
  text-align: center;
  font-size: 36px;
  text-transform: uppercase;
}

</style>