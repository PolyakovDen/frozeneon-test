<script setup>
import meAvatar from '@/assets/images/me.png'
</script>

<template>
  <v-app>
   
    <v-main class="main">
      <div class="header_background" />
      <router-view />
    </v-main>
    
    <v-footer class="footer d-flex flex-column pa-0 mt-auto">
      <div class="footer__me d-flex w-100 justify-center align-center px-4">
        <v-avatar :image="meAvatar" />
        <strong class="ml-2 mr-10">Polyakov Denis</strong>
        <v-btn 
          class="mt-1"
          variant="text" 
          size="small"
          color="blue-accent-2"
          href="https://github.com/PolyakovDen"
          target="_blank"
        >
          GitHub Repo
        </v-btn>
      </div>

      <v-divider :thickness="3" color="info" class="w-100" />

      <div class="footer__rights px-4 py-2 text-center w-100">
        {{ new Date().getFullYear() }} — <strong>Frozeneon</strong>
      </div>
    </v-footer>
  </v-app>
</template>

<style scoped lang="scss">
  * {
    font-family: Roboto, sans-serif;
  }

  .header_background {
    width: 100%;
    height: 7px;
    background: rgb(191,52,194);
    background: linear-gradient(90deg, rgba(191,52,194,1) 0%, rgba(255,73,213,0.9738489145658263) 51%, rgba(255,39,39,1) 72%, rgba(254,67,2,0.9682466736694678) 100%);
  }

  .main {
    height: calc(100% - 120px);
  }

  .footer {
    background-color: #1B2431;
    color: #fff;

    &__me {
      height: 80px;
    }

    &__rights {
      opacity: .5;
    }
  }
</style>
