<template>
  <div class="404">
    <div class="error">404</div>
    <div class="error-text">Looks like you're lost...</div>
    <div class="back-home">
      <router-link class="links" :to="{ name: 'home' }">
        <a class="home">Back Home</a>
      </router-link>
    </div>
  </div>
</template>