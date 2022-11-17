<template>
  <div class="form-content">
    <v-text-field
        v-model="email"
        label="E-mail"
        color="#975f9d"
        required
    ></v-text-field>
    <v-text-field
        v-model="password"
        label="Password"
        color="#975f9d"
        :type="show ? 'text' : 'password'"
        :append-inner-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
        @click:append-inner="show = !show"
        required
    ></v-text-field>
    <v-btn class="button"
           color="#975f9d"
           elevation="2"
           rounded
    >LOGIN
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "Login",
  data: () => ({
    email: '',
    password: '',
    show: false
  }),
}
</script>

<style>

.form-content {
  padding: 25px;
}

.button {
  color: white !important;
}

</style>