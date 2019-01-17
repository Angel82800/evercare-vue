<template>
  <v-layout wrap>
    <v-flex md4 xs12>
      <v-card class="profile-card">
        <v-layout row md12 xs12 sm12 justify-center>
          <v-avatar
            size="150"
            color="grey lighten-4"
          >
            <img src="https://vuetifyjs.com/apple-touch-icon-180x180.png" alt="avatar">
          </v-avatar>
        </v-layout>
        <v-layout justify-center>
          <h2>Winnie W</h2>
        </v-layout>
        <v-layout justify-center>
          <h3>Registered Nurse</h3>
        </v-layout>
      </v-card>
    </v-flex>
    <v-flex md8 xs12 sm12>
      <v-card class="work-experience">
        <v-layout justify-space-between align-center>
          <h2>Work Experiences</h2>
          <v-btn color="success">+ Add Experience</v-btn>
        </v-layout>
        <Experience></Experience>
      </v-card>
    </v-flex>
  </v-layout>
</template>
<style lang="scss" scoped>
  .profile-card {
    padding: 20px;
    margin: 20px;
    .layout {
      margin: 10px 0;
    }
  }

  .work-experience {
    padding: 20px;
    margin: 20px;
  }
</style>
<script>
import Experience from '../components/experience';
export default {
  components: {
    Experience
  }
}
</script>

