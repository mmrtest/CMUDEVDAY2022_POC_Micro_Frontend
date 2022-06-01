<template>
  <v-row>
    <v-col class="text-center">
      <img src="/v.png" alt="Vuetify.js" class="mb-5" />
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <h1><em>App1 : inspire</em></h1>
            <v-btn depressed color="primary" @click="menuActionClick()">
              Back to Portal
            </v-btn>
          </small>
        </footer>
      </blockquote>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'InspirePage',
  methods: {
    menuActionClick() {
      window.location.href = 'http://localhost'
    },
  },
}
</script>
