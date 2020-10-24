<template>
  <div class="text-center">
    <v-menu>
      <template v-slot:activator="{ on, attrs }">
        <v-btn depressed v-bind="attrs" v-on="on">
          Languages
        </v-btn>
      </template>
      <v-list>
        <v-list-item v-for="(lang, i) in langs" :key="i">
          <v-list-item-title @click.prevent="setLocale(lang.short)">
            {{ lang.full }}</v-list-item-title
          >
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>

<script>
export default {
  name: "LangSwitcher",
  data: () => ({
    langs: [
      { short: "fr", full: "Français" },
      { short: "en", full: "English" },
    ],
  }),
  methods: {
    setLocale(locale) {
      this.$i18n.locale = locale;
      this.$router.push({
        params: { lang: locale },
      });
    },
  },
};
</script>

<style scoped></style>
