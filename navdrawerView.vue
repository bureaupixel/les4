<script setup>
import { Navbar, NavbarLogo, NavbarCollapse, NavbarLink } from 'flowbite-vue'
import { RouterLink, RouterView } from 'vue-router'
import footerView from './footerView.vue';
</script>
<template>

<!-- drawer init and toggle -->
<div class="text-right">
   <button 
    class="overflow-y-auto font-medium px-5 py-2.5 mr-2 mb-2" 
    type="button" 
    data-drawer-target="drawer-top-example" 
    data-drawer-show="drawer-top-example" 
    data-drawer-placement="top" 
    aria-controls="drawer-top-example">
    <svg 
      xmlns="http://www.w3.org/2000/svg" 
      fill="currentColor"
      height="1em" 
      viewBox="0 0 448 512">
      <!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
      <path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg>
   </button>
</div>

<!-- drawer component -->
<div id="drawer-top-example" 
      class="fixed top-0 left-0 right-0 z-40 w-full p-4 
      transition-transform -translate-y-full
     bg-white dark:bg-gray-800" 
      tabindex="-1" 
      aria-labelledby="drawer-top-label">

    <button 
      type="button" 
      data-drawer-hide="drawer-top-example" 
      aria-controls="drawer-top-example" 
      class="w-8 h-8 absolute top-2.5 right-2.5 inline-flex items-center justify-center " >
      <span class="sr-only">Close menu</span>
      <svg 
        xmlns="http://www.w3.org/2000/svg" 
        fill="currentColor"
        height="1em" 
        viewBox="0 0 384 512"><!--! Font Awesome Free 6.4.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. -->
        <path d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"/></svg>
   </button>

   <div class="nav">
    <div>
      <li>
          <ul><p class="title text-4xl font-extrabold font-sans pb-5 mb-5">MIND Creative Coding sessions</p></ul>
      </li>      
    </div>
    <div>

      <div class="container flex flex-wrap pb-5 mb-5">

        <div class="w-64 md:w-1/3">
          <p class="title text-xl font-extrabold font-sans">Front end & interfaces</p>
          <li class="text-left">
            <ul ><RouterLink to="/">Home</RouterLink></ul>
            <ul ><RouterLink to="/googlefonts">Google fonts</RouterLink></ul>
            <ul><RouterLink to="/tailwindextend">Extend Tailwind</RouterLink></ul>
            <ul><RouterLink to="/flexboxes">Flexboxes and grids</RouterLink></ul>
          </li>
        </div>

        <div class="w-64 md:w-1/3">
          <p class="title text-xl font-extrabold font-sans">Variables and data</p>
          <li>
            <ul><RouterLink to="/varsanddata">Variables and data</RouterLink></ul>
            <ul><RouterLink to="/filterdata">Filter data</RouterLink></ul>
            <ul><RouterLink to="/importdata">Import data</RouterLink></ul>
            <ul><RouterLink to="/loaddata">Load JSON data</RouterLink></ul>
          </li>
        </div>

        <div class="w-64 md:w-1/3">
          <p class="title text-xl font-extrabold font-sans">Data visualizations</p>
          <li>
            <ul><RouterLink to="/exampleleaflet">Maps and JSON data</RouterLink></ul>
            <ul><RouterLink to="/examplecharts">Charts and JSON data</RouterLink></ul>
            <ul><RouterLink to="/examplerelations">Data relations</RouterLink></ul>
          </li>
        </div>

      </div>


      <div class="flex">
        <div class="flex-4">
          <footerView /> 
        </div>
      </div>    

    </div>
   </div>
</div>
</template>