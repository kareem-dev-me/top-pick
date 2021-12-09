<template>
  <v-img
    :src="require('~/assets/hero.jpeg')"
    height="100vh"
    class="align-center"
    :gradient="
      md ? 'to right, #D7AF4D 30%, transparent 50%' : '#000000a0,#000000a0'
    "
    position="top"
    eager
  >
    <v-row class="text-center">
      <v-col cols="12" md="4">
        <v-img
          class="mx-auto"
          :src="md ? require('~/assets/grey-logo.png') : '/logo.png'"
          max-width="200"
          max-height="100"
        ></v-img>

        <p
          class="text-h5 font-weight-bold"
          :class="[md ? 'secondary--text' : 'primary--text']"
        >
          مكتب اختيار القمة للخادمات
        </p>

        <v-btn
          outlined
          :color="md ? 'secondary' : 'primary'"
          class="rounded-lg font-weight-bold"
          @click="$vuetify.goTo('#contact')"
          >اتصل بنا</v-btn
        >
      </v-col>
    </v-row>
  </v-img>
</template>

<script>
export default {
  computed: {
    md() {
      if (this.$vuetify.breakpoint.mdAndUp) {
        return true
      } else {
        return false
      }
    },
  },
}
</script>

<style></style>
