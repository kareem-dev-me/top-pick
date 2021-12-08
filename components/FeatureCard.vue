<template>
  <v-card elevation="5" class="feature-card rounded-lg" height="100%">
    <v-card-text class="text-center">
      <div class="card-flex">
        <v-icon size="60" color="primary">{{ icon }}</v-icon>

        <p class="end-flex mb-0 text-h6">{{ text }}</p>
      </div>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: '',
    },
    icon: {
      type: String,
      default: '',
    },
  },
}
</script>

<style scoped>
.feature-card {
  border-right: 5px solid var(--v-primary-base);
  border-bottom: 5px solid var(--v-primary-base);
}
.card-flex {
  display: flex;
  flex-direction: column;
}
</style>
