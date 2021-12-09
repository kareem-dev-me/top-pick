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
      <v-tooltip v-for="(number, index) in numbers" :key="index" bottom>
        <template #activator="{ on, attrs }">
          <v-btn
            :href="`https://api.whatsapp.com/send?phone=${number}`"
            target="_blank"
            class="my-3 rounded-lg"
            x-large
            block
            color="primary"
            dark
            v-bind="attrs"
            v-on="on"
          >
            {{ number }}
          </v-btn>
        </template>
        <span>للتواصل عن طريق الواتس</span>
      </v-tooltip>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      numbers: ['0580381135', '0580393834', '0580393123', '0580381152'],
    }
  },
}
</script>

<style></style>
