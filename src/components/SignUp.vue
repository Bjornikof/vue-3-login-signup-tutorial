<template>
  <div class="form-content">
    <v-row class="pr-3 pl-3 pb-3">
      <v-text-field
          v-model="firstName"
          label="First Name"
          color="#975f9d"
          required
          class="mr-2"
      ></v-text-field>
      <v-text-field
          v-model="lastName"
          label="Last Name"
          color="#975f9d"
          required
      ></v-text-field>
    </v-row>
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
        :type="showPassword ? 'text' : 'password'"
        :append-inner-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
        @click:append-inner="showPassword = !showPassword"
        required
    ></v-text-field>
    <v-text-field
        v-model="passwordRepeat"
        label="Repeat Password"
        color="#975f9d"
        :type="showPasswordRepeat ? 'text' : 'password'"
        :append-inner-icon="showPasswordRepeat ? 'mdi-eye' : 'mdi-eye-off'"
        @click:append-inner="showPasswordRepeat = !showPasswordRepeat"
        required
    ></v-text-field>
    <v-btn class="button"
           color="#975f9d"
           elevation="2"
           rounded
    >SIGN UP
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "SignUp",
  data: () => ({
    password: '',
    passwordRepeat: '',
    email: '',
    firstName: '',
    lastName: '',
    showPasswordRepeat: false,
    showPassword: false
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