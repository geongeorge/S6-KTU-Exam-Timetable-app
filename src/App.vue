<template>
  <v-app dark>
    <v-toolbar app color="light-blue" dark>
      <v-toolbar-title class="headline text-uppercase">
        <span>TIME</span>
        <span class="font-weight-light">TABLE</span>
      </v-toolbar-title>
    </v-toolbar>

    <v-content mt-4>
      <TimeTable />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import TimeTable from './components/TimeTable'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TimeTable
  },
  data () {
    return {
      //
    }
  }
}
</script>
