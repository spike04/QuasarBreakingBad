<template>
  <q-layout view="hHh Lpr fFf">
    <!-- Be sure to play with the Layout demo on docs -->

    <!-- (Optional) The Header -->
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>Breaking Bad API Example</q-toolbar-title>
        <q-tabs>
          <q-route-tab :to="{name: 'profile', params: {id: 1}}" replace label="Walter White" />
          <q-route-tab :to="{name: 'profile', params: {id: 2}}" replace label="Jesse Pinkman" />
          <q-route-tab :to="{name: 'profile', params: {id: 'random'}}" replace label="Random" />
        </q-tabs>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view :key="$route.params.id" />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  // name: 'LayoutName',
  meta: {
    title: 'Breaking Bad App'
  },
  data() {
    return {
      leftDrawer: true
    }
  }
}
</script>
