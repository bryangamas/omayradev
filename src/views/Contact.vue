<template>
  <Slug>
    <template #header>
      <h1 id="contact"></h1>
    </template>
    <template #content>
      <v-container class="d-flex flex-column text-center align-center">
        <div class="text-center text-h4 text-sm-h2">
          {{ isEnglish ? 'Get in touch' : 'Contáctame' }}
        </div>
        <div
          class="grey--text ma-5 pa-5 align-center text-center text-h5 text-sm-h4"
          style="max-width: 85%"
        >
          {{
            isEnglish
              ? "I'm actively looking for interesting job opportunities where I can share and improve my skills further."
              : 'Estoy buscando oportunidades de trabajo donde pueda compartir y mejorar mis habilidades.'
          }}
        </div>
        <v-btn
          class="amber"
          large
          outlined
          href="mailto:omairapalaciosanchez@gmail.com"
          target="_blank"
        >
          <v-icon class="mr-4">fa-envelope</v-icon>
          {{ isEnglish ? 'CONNECT' : 'Contáctame' }}</v-btn
        >
        <SocialIcons :isDark="isDark" class="mt-5 pt-5 hidden-sm-and-up" />
      </v-container>
    </template>
  </Slug>
</template>
<script>
const Slug = () => import('@/views/Slug.vue');
const SocialIcons = () => import('@/components/SocialIcons.vue');

export default {
  name: 'Contact',
  components: {
    Slug,
    SocialIcons,
  },
  props: { isDark: Boolean, isEnglish: Boolean },
};
</script>
