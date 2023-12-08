<script setup>
import { ref } from 'vue'
const brand = ref('MedEx WebPortal')
</script>

<template>
  <nav class="bg-blue-900">
    <div class="wrapper"> 
      <div class="brand">
        <span class="brand-title">{{ brand }}</span>
      </div>
      <div class="menu">
        <a href="#" class="menu-item"> Medical Staff </a>
        <a href="#" class="menu-item"> Patient Portal </a>
        <a href="#" class="menu-login"> Logout </a>
      </div>
    </div>
  </nav>
</template>

<style scoped lang="postcss">
nav {
  @apply flex h-20 bg-slate-900 text-slate-200;
  .wrapper {
    @apply container mx-auto flex w-full justify-between items-center;
    .brand {
      &-title {
        @apply text-2xl font-bold text-red-800;
      }
    }
    .menu {
      @apply flex gap-2;
      &-item {
        @apply rounded-md px-4 py-2 hover:bg-white hover:text-black;
      }
      &-login {
        @apply rounded-md px-4 py-2 bg-slate-500 hover:bg-pink-200 hover:text-black;

      }
    }
  }

  & .router-link-active {
    @apply underline underline-offset-4;
  }
}
</style>
