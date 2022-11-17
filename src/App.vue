<template>
  <v-app>
    <v-main>
      <div class="content">
        <v-card :elevation="5" class="card">
          <v-tabs
              v-model="tab"
              background-color="primary"
              fixed-tabs
              color="#975f9d"
          >
            <v-tab value="login">LOGIN</v-tab>
            <v-tab value="signup">SIGN UP</v-tab>
          </v-tabs>

          <v-card-text class="text-center">
            <v-window v-model="tab">
              <v-window-item value="login">
                <Login/>
              </v-window-item>

              <v-window-item value="signup">
                <SignUp/>
              </v-window-item>
            </v-window>
          </v-card-text>
        </v-card>
      </div>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import {defineComponent} from 'vue'
import Login from './components/Login.vue'
import SignUp from './components/SignUp.vue'

export default defineComponent({
  name: 'App',
  data: () => ({
    tab: null,
  }),

  components: {
    Login,
    SignUp
  }
})
</script>

<style>
main {
  background-image: url('@/assets/background-image.jpg');
  background-size: cover;
}

.content {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.card {
  width: 35%;
  height: 75%;
  min-width: 275px;
}

</style>