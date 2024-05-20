<template>
  <footer id="footer">
    <p>Make your Burguer {{ dataAtual }} - &copy; {{ ano }}</p>
  </footer>
</template>
  
  <script>
export default {
  name: "Footer",
  data() {
    return {
      dataAtual: null,
      ano: null,
    };
  },
  mounted() {
    this.atualizarAno();
  },
  methods: {
    atualizarAno() {
      this.dataAtual = new Date().toLocaleDateString();

      this.ano = new Date().getFullYear();
    },
  },
};
</script>
  
<style scoped>
#footer {
  height: 200px;
  background-color: #222;
  border-top: 4px solid #111;
  color: #fcba03;
  display: flex;
  align-items: center;
  justify-content: center;
  bottom: 0;
  width: 100%;
}
</style>
  