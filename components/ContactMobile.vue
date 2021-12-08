<template>
  <v-row>
    <v-col cols="12" md="6" order="2" order-md="1">
      <v-tooltip v-for="number in 5" :key="number" bottom>
        <template #activator="{ on, attrs }">
          <v-btn
            href="tel:0580393834"
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
        <span>للتواصل عن طريق الجوال</span>
      </v-tooltip>
    </v-col>

    <v-col cols="12" md="6" order="1" order-md="2">
      <v-img
        :src="require('~/assets/telephone.png')"
        max-width="300"
        class="mx-auto"
      ></v-img>
    </v-col>
  </v-row>
</template>

<script>
export default {}
</script>

<style></style>
