<template>
  <v-app id="app" dark>
    <app-header></app-header>
    <v-content>
      <v-container fluid fill-height>
        <v-layout justify-center align-center>
          <router-view/>
        </v-layout>
      </v-container>
    </v-content>
    <v-footer app fixed>
      <span>&copy; Yar-ua 2018</span>
    </v-footer>
  </v-app>
</template>

<script>
import { mapState } from 'vuex'
import Header from '@/components/Header'

export default {
  name: 'App',
  components: {
    'app-header': Header
  },
  computed: {
    ...mapState(['isAuth'])
  }
}
</script>
