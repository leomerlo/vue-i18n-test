<template>
  <div>
    <p>{{ $t("hello", { name }) }}</p>
    <p>{{ $t("goodbye") }}</p>
    <p>{{ $tc("car", 2) }}</p>

    <p>{{ $d(new Date(), 'short') }}</p>

    <button @click="setLocale('en')">English</button>
    <button @click="setLocale('es')">Spanish</button>
    <button @click="setLocale('de')">German</button>
  </div>
</template>

<script>
export default {
  name: "HelloI18n",
  data() {
    return {
      name: 'Peter',
    };
  },
  methods: {
    setLocale(locale) {
      this.$i18n.locale = locale;
      localStorage.setItem('locale', locale);
    }
  }
};
</script>
