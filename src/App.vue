<script setup>
import HelloWorld from './components/HelloWorld.vue'
import WelcomeItem from './components/WelcomeItem.vue'
import Headerproject from './components/Headerproject.vue'
import Footproject from './components/Footproject.vue';

</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

      <div class="welcome-item"> <!-- agrega la clase "welcome-item" -->
          <WelcomeItem>
              <template v-slot:icon>
                  <i class="fas fa-rocket"></i>
              </template>

              <template v-slot:heading>
                  Welcome to My Site
              </template>

              <p>Thank you for visiting my site. Please take a look around and let me know if you have any questions.</p>
          </WelcomeItem>
      </div>
      <div>
          <ImageFrame imageUrl="https://media.tenor.com/Vi3igSsjtdMAAAAi/hu-tao-music.gif" />
      </div>
  </header>

  <main>
   <Headerproject/>
   <Headerproject name="componente 1"/>
   <Headerproject name="componente 2"/>
   <Headerproject name="componente 3"/>
   <Footproject email="correo"/>
  </main>
</template>

<style scoped>

.welcome-item {
    margin-top: 2rem;
    display: flex;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
<script>
import ImageFrame from "@/components/ImageFrame.vue";

export default {
    name: "MyComponent",
    components: {
        ImageFrame,
    },
};
</script>