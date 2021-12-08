<template>
  <v-row>
    <v-col cols="12" md="6" order="1" order-md="2">
      <v-img
        :src="require('~/assets/whatsapp.png')"
        max-width="300"
        class="mx-auto"
      ></v-img>
    </v-col>

    <v-col cols="12" md="6" order="1" order-md="2">
      <v-tooltip v-for="number in 5" :key="number" bottom>
        <template #activator="{ on, attrs }">
          <v-btn
            href="https://api.whatsapp.com/send?phone=0580393123"
            target="_blank"
            class="my-3 rounded-lg"
            x-large
            block
            color="primary"
            dark
            v-bind="attrs"
            v-on="on"
          >
            Button
          </v-btn>
        </template>
        <span>للتواصل عن طريق الواتس</span>
      </v-tooltip>
    </v-col>
  </v-row>
</template>

<script>
export default {}
</script>

<style></style>
