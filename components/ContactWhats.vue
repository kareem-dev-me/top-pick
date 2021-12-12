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
      <v-tooltip v-for="number in numbers" :key="number.id" bottom>
        <template #activator="{ on, attrs }">
          <v-btn
            :href="`https://api.whatsapp.com/send?phone=${number.num}`"
            target="_blank"
            class="my-3 rounded-lg"
            x-large
            block
            color="primary"
            dark
            v-bind="attrs"
            v-on="on"
          >
            {{ number.num }}
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
      numbers: [],
    }
  },
  mounted() {
    const requestOptions = {
      method: 'GET',
      redirect: 'follow',
    }

    fetch(
      'http://alqimaforservices.com/pagepanel/api/v1/numbers?type=whats',
      requestOptions
    )
      .then((response) => response.json())
      .then((result) => (this.numbers = result.data))
  },
}
</script>

<style></style>
