<template>
  <v-layout wrap justify-center align-center>
    <v-flex md12 xs12 sm12>
      <v-layout class="container-layout">
        <filterContainer />
      </v-layout>
      <v-layout>
        <profileContainer />
      </v-layout>
    </v-flex>
  </v-layout>
</template>
<style lang="scss">
span {
  color: #A1A1A1;
}

.v-btn__content {
  text-transform: none;
}

.container-layout {
  margin-bottom: 50px;
}
</style>
<script>
import profileContainer from '~/containers/list/profileContainer';
import filterContainer from '~/containers/list/filter';
export default {
  components: {
    profileContainer,
    filterContainer
  }
}
</script>
