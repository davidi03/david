<template>
  <v-form v-model="valid" @submit.prevent="submit">
    <v-container>
      <v-row>
        <v-col cols="12" md="4">
          <v-text-field
            v-model="firstname"
            :rules="nameRules"
            :counter="10"
            label="First name"
            required
          ></v-text-field>
        </v-col>

        <v-col cols="12" md="4">
          <v-text-field
            v-model="lastname"
            :rules="nameRules"
            :counter="10"
            label="Last name"
            required
          ></v-text-field>
        </v-col>

        <v-col cols="12" md="4">
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="12">
          <v-text-field
            v-model="message"
            :rules="messageRules"
            label="Leave your Message"
            required
          ></v-text-field>
        </v-col>
      </v-row>
    </v-container>
    <v-btn
      class="mr-4"
      type="submit"
      v-on:click="say('hi')"
      :disabled="invalid"
    >
      submit
    </v-btn>
    <v-btn @click="clear"> clear </v-btn>
    <div id="example-1">
      <button prevent v-on:click.prevent="counter += 1">Add 1</button>
      <p>The button above has been clicked {{ counter }} times.</p>
    </div>
  </v-form>
</template>

<script>
export default {
  data: () => ({
    counter: 0,
    valid: false,
    firstname: "",
    lastname: "",
    nameRules: [
      (v) => !!v || "Name is required",
      (v) => v.length <= 10 || "Name must be less than 10 characters",
    ],
    email: "",
    emailRules: [
      (v) => !!v || "E-mail is required",
      (v) => /.+@.+/.test(v) || "E-mail must be valid",
    ],
    message: "",
    messageRules: [
      (v) => !!v || "Message is required",
      (v) => v.length <= 50 || "Message must be less than 50 characters",
    ],
  }),
  methods: {
    say: function (message) {
      alert(message);
    },
    clear() {
      this.firstname = "";
      this.lastname = "";
      this.email = "";
      this.message = null;
    },
  },
};
</script>
