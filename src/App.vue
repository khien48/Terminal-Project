
<template>
  <v-app id="inspire">

    <!-- SIDEBAR -->

    <v-navigation-drawer v-model="drawer">

      <Sidebar /> <!-- SIDEBAR COMPONENTS -->

    </v-navigation-drawer>

    <!-- ............................. -->

    <!-- APPBAR -->

    <v-app-bar :elevation="2">
      <template v-slot:prepend>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      </template>

      <v-app-bar-title>.....</v-app-bar-title>

      <Appbar /> <!-- APPBAR COMPONENTS -->

    </v-app-bar>

    <!-- ............................. -->


    <!-- MAIN -->

    <v-main>

      <RouterView /> <!-- ROUTERVIEW -->

    </v-main>

    <!-- ............................. -->

  </v-app>

</template>

<script setup>
import { ref } from 'vue'
import StudentList from './pages/StudentList.vue';
import Navbar from './components/Appbar.vue';


const drawer = ref(null)
</script>

<script>
export default {
  data: () => ({ drawer: null }),
}

</script>