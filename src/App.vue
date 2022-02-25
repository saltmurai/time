<template>
  <v-app>
    <v-app-bar v-if="!$route.meta.hideNav" color="#6AA84F" app>
      <v-spacer />
      <v-img class="mr-3" contain height="50px" src="@/assets/time.png"> </v-img>
      <v-spacer />
    </v-app-bar>
    <v-main>
     <v-container fluid>
       <router-view></router-view>
     </v-container>
    </v-main>
    <div v-if="$route.meta.showLogin">
      <v-btn to="/menu" max-width="400" color="#6AA84F" large width="80%" class="white--text text-none mx-auto mb-3">Đăng nhập</v-btn>
      <v-spacer />
      <v-btn width="20%" depressed class="mb-8 mx-auto text-none grey--text" small plain><v-icon left>mdi-bug</v-icon>Báo lỗi</v-btn>
    </div>
  </v-app>
</template>


<script>
export default {
  data() {
    return {
    }

  },
  method: {
  }
  
}
</script>

<style>
#app {
  text-align: center;
}
</style>

<!-- <script>
// mport loader from './components/Loading.vue'
import PincodeInput from 'vue-pincode-input'
export default {
  name: 'App',
  mounted() {
    this.delay(1000);
  },  
  components: {
    // loader
    PincodeInput,
  },

  data: () => ({
    //
  }),
  methods: {
    delay(ms) {
      const startPoint = new Date().getTime();
      while (new Date().getTime() - startPoint <= ms) {
        /* wait */
      }
    }
  }
}
</script>

<style scoped>
#app {
  text-align: center;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  height: 100%;
}

#pin-code input {
  position: relative;
  font-weight: bold;
}
</style> -->