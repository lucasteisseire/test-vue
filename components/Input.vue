<template>
  <div>
    <input
      v-autowidth="{ maxWidth: '960px', minWidth: '50px', comfortZone: 0 }"
      type="text"
      placeholder=""
      v-model="number"
    />
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      number: ""
    };
  },
  watch: {
    number() {
      this.number = this.number
        .replace(/[^\d]/g, "")
        .replace(/(\d)(?=(\d{3})+(?!\d))/g, "$1 ");
    }
  }
};
</script>
