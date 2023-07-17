<script setup>
const title='Dow-Not'
const offerDate= ()=> new Date().toDateString()
const displayHtml= '<strong>'+offerDate()+'</strong>'
const img={
  src:"https://4.bp.blogspot.com/-ukjkhVazo5w/WstgxEHtg3I/AAAAAAABBEU/O4fHcqtSlFcE9zwjmol2nDZ4OhhVzNongCLcBGAs/s1600/perfect%2Bdark%2Bchocolate%2Bdonut.JPG",
  title:"This is a image title 1",
  alt:"",
  class:"w-full object-cover contrast-150"
}
const cssProperty={
 buttonCssProperty:"rounded-full bg-yellow-400 px-6 py-2 shadow-sm shadow-yellow-600 hover:bg-yellow-300",
 navbarCssProperty:"hover:text-grey-200 mx-3 underline decoration-pink-600 underline-offset-8 hover:no-underline" 
}
</script>

<template>
  
	<main class="bg-black text-white">
  <!--Navbar-->
  <header class="">
    <nav class="flex items-center justify-between border px-6 py-2">
      <!--logo text -->
      <div class="flex items-center">
        <span class="block h-4 w-4 rounded-lg bg-blue-400"></span>
        <div class="ml-2 text-3xl font-bold text-yellow-400">{{title}}</div>
      </div>
      <!--Menu Items-->
      <div class="text-gray-400 max-md:hidden">
        <a href="http://" target="_blank" rel="noopener noreferrer" :class="cssProperty.navbarCssProperty">Home</a>
        <a href="http://" target="_blank" rel="noopener noreferrer" :class="cssProperty.navbarCssProperty">About</a>
        <a href="http://" target="_blank" rel="noopener noreferrer" :class="cssProperty.navbarCssProperty">Shop</a>
        <a href="http://" target="_blank" rel="noopener noreferrer" :class="cssProperty.navbarCssProperty">Socials</a>
      </div>
      <!--login -->
      <div class="max-md:hidden">
        <a href="http://" target="_blank" rel="noopener noreferrer" class="mr-4 rounded-lg border bg-yellow-400 px-3 py-2 text-gray-900 shadow-sm shadow-yellow-400 hover:bg-yellow-300 hover:text-gray-800">Login</a>
      </div>
      <!--menu hamburger responsive-->
      <div class="hidden max-md:block">
        <span class="mb-2 block h-1 w-8 bg-pink-600"></span>
        <span class="mb-2 block h-1 w-8 bg-pink-600"></span>
        <span class="mb-2 block h-1 w-8 bg-pink-600"></span>
        <span class="mb-2 block h-1 w-8 bg-pink-600"></span>
      </div>
    </nav>
  </header>
  <!--hero-->
  <section class="flex h-screen items-center max-md:mt-10 max-md:flex-col">
    <div class="w-full px-4 py-4">
      <h1 class="max-md:text-1xl mb-10 text-3xl font-semibold capitalize text-blue-400">Have a donut in DowNut</h1>
      <p class="mb-4 text-xl text-gray-300 max-md:text-base">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias odio debitis vitae quia a nesciunt cumque ratione blanditiis eligendi sed mollitia, eum consequatur, illum perferendis quo nam illo! Incidunt, quia.</p>
      <p class="max=md:text-sm mb-6 text-yellow-400">Buy more and get more till <span v-html="displayHtml">  </span></p>
      <button :class="cssProperty.buttonCssProperty">Find more</button>
    </div>
    <div class="flex h-2/4 w-full items-center overflow-hidden">
      <img  v-bind="img"  />
    </div>
  </section>
</main>


</template>

<style scoped>

</style>
