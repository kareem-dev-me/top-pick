<template>
  <v-row>
    <v-col v-for="feature in features" :key="feature.text" cols="12" md="3">
      <feature-card :icon="feature.icon" :text="feature.text"></feature-card>
    </v-col>
  </v-row>
</template>

<script>
import FeatureCard from './FeatureCard.vue'
export default {
  components: { FeatureCard },

  data() {
    return {
      features: [
        {
          text: 'نأسف لعدم وجود شغالات إيجار',
          icon: 'mdi-close-octagon-outline',
        },
        {
          text: 'هل لديكم عاملات مربيات ممرضات طباخات',
          icon: 'mdi-progress-question',
        },
        {
          text: 'شغالات رافضات العمل وتريدون التنازل عنهم بأسرع وقت وبدون خساره',
          icon: 'mdi-cash',
        },
        {
          text: 'يوجد لدينا مترجمين لسهوله اقناعهم من جميع الجنسيـات',
          icon: 'mdi-translate',
        },
        { text: 'قسم خاص لاستلام ورعاية الخدم', icon: 'mdi-account-group' },
        {
          text: 'لدينا عدد كبير من العملاء يثقون فى مكتبنا ويرغبون فى خادمات للتنازل',
          icon: 'mdi-account-box-multiple',
        },
        {
          text: 'نحن نقوم بجميع الأجراءات القانونيه',
          icon: 'mdi-scale-balance',
        },
        {
          text: '( نقل الكفاله ـ اصدار الاقامه ـ دفع الغرامه ـ وغيره)',
          icon: 'mdi-card-account-details-outline',
        },
        {
          text: 'عقود رسمية لضمان حقوق جميع الاطراف',
          icon: 'mdi-file-document-edit-outline',
        },
        {
          text: 'باعلي الاسعار تعوضك خسارة الاستقدام',
          icon: 'mdi-currency-usd',
        },
        { text: 'نقل الكفالة فى مدة وجيزة', icon: 'mdi-clipboard-text-clock' },
      ],
    }
  },
}
</script>

<style></style>
