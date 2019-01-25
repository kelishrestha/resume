<template>
  <v-content>
    <v-container fluid>
      <welcome />
      <recent-projects />
      <services />
      <about-me />
      <get-in-touch />
    </v-container>
  </v-content>
</template>

<script>
export default {
  components: {
    AboutMe: () => import('@/components/AboutMe'),
    GetInTouch: () => import('@/components/GetInTouch'),
    RecentProjects: () => import('@/components/RecentProjects'),
    Services: () => import('@/components/Services'),
    Welcome: () => import('@/components/Welcome')
  }
}
</script>
