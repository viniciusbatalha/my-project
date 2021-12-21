<template>
    <div class="container jumbotron mt-2">
      <h1 class="display-4">Bem-vindo!</h1>
      <p>Aplição disponível para listagem dos gerentes do nosso banco.</p>
      <button class="btn btn-danger" @click="logoutMixin">Vo da o fora daqui tlgd mermao</button>
    </div>
</template>

<script>
import {logoutMixin} from '../mixins'

export default {
  name: 'home',
  mixins: [logoutMixin]
}
</script>
