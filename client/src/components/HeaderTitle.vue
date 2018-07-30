<template>
  <div class="header">
    <img src="../assets/logo-abtasty.jpg" alt="Logo AB Tasty" class="logo">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HeaderTitle',
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
    .header {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: auto;
        max-width: 1000px;
        border-bottom: 2px solid #162a3b;
    }

    .logo {
        width: 100px;
        flex-direction: row;
    }

    h1 {
        margin-left: 30px;
        flex-direction: row;
    }
</style>
