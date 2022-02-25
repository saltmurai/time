<template>
     <div>
        <h1 class="pt-16 text-center">Nhập mã pin</h1>
        <p class="pt-3 text-center">Vui lòng nhập mã pin để đăng nhập</p>
        <PincodeInput class="pin-code" v-model="code" placeholder="" :length="6" autofocus="true" />
        <!-- <v-spacer />
        <v-btn to="/about" color="#6AA84F" large width="80%" class="white--text text-none mx-auto mt-16 mb-3">Đăng nhập</v-btn>
        <v-spacer />
        <v-btn width="20%" depressed class="mb-8 mx-auto text-none grey--text" small plain><v-icon left>mdi-bug</v-icon>Báo lỗi</v-btn> -->
      </div>
</template>

<script>
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

#pin-code input {
  position: relative;
  font-weight: bold;
}

</style>