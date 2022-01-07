<template>
  <div>
    <p>{{ $t("hello") }}</p>
    <p>{{ $t("goodbye") }}</p>
    <button @click="setLocale('en')">English</button>
    <button @click="setLocale('es')">Spanish</button>
    <button @click="setLocale('de')">German</button>
  </div>
</template>

<script>
export default {
  name: "HelloI18n",
  methods: {
    setLocale(locale) {
      this.$i18n.locale = locale;
      localStorage.setItem('locale', locale);
    }
  }
};
</script>
