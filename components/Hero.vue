<template>
  <v-img
    :src="
      require('~/assets/young-attractive-maid-uniform-showing-ok-gesture-while-standing.jpeg')
    "
    max-height="100vh"
    class="align-center"
    gradient="to right, #D7AF4D 30%, transparent 50%"
    position="right top"
  >
    <v-row class="text-center">
      <v-col cols="12" md="4">
        <v-img
          class="mx-auto"
          :src="require('~/assets/grey-logo.png')"
          max-width="200"
          max-height="100"
        ></v-img>
        <p class="secondary--text text-h5">مكتب اختيار القمة للخادمات</p>
        <v-btn outlined color="secondary">اتصل بنا</v-btn>
      </v-col>
    </v-row>
  </v-img>
</template>

<script>
export default {}
</script>

<style></style>
