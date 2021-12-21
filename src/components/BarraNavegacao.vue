<template>
    <nav class="navbar navbar-expand-lg navbar-bytebank">
      <a class="navbar-brand" href="#">ByteBank</a>
      <button class="navbar-toggler" type="button">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <BarraNavegacaoQuandoLogado v-if="usuarioestaLogado"/>
        <BarraNavegacaoQuandoDeslogado v-else/>
      </div>
    </nav>
</template>

<script>
import BarraNavegacaoQuandoLogado from '../components/BarraNavegacaoQuandoLogado'
import BarraNavegacaoQuandoDeslogado from '../components/BarraNavegacaoQuandoDeslogado'

export default {
    components:{
        BarraNavegacaoQuandoLogado,
        BarraNavegacaoQuandoDeslogado
    },
    computed: {
        usuarioestaLogado() {
            return Boolean(this.$store.state.token)
        }
    }
}
</script>

<style>
.navbar {
  background: #27ae60;
}
.navbar-bytebank a {
  color: #fff;
}
.navbar-bytebank a:hover {
  color: #000;
}
</style>