<template>
  <v-container grid-list-xl fluid pa-0>
    <v-parallax
      dark
      :src="bgimage"
      gradient="to right, #2980b9, #6dd5fa, #ffffff"
    >
      <v-layout
        align-center
        column
        justify-center
      >
        <v-avatar
          :tile="tile"
          :size="200"
        >
          <img :src="profile" alt="avatar">
        </v-avatar>
        <h1 class="display-2 font-weight-thin mb-3">{{ name }}</h1>
        <h3 class="subheading">{{ title }}</h3>
      </v-layout>
    </v-parallax>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    name: 'Kelina Shrestha',
    title: 'Ruby on Rails Engineer',
    intro: "Self-motivated, dedicated and organized software engineer pursuing professional experience in technology with an aim to solve problems with technology. Collaborative team player uplifting performance of applications and team to achieve targeted goals accepting challenges.",
    bgimage: 'https://scontent.fktm3-1.fna.fbcdn.net/v/t1.0-9/32464466_10209916763430652_5090903458404368384_o.jpg?_nc_cat=103&_nc_ht=scontent.fktm3-1.fna&oh=5b20122aee9b6f22aca5b6e2e102a45d&oe=5D50A52E',
    profile: 'https://scontent.fktm3-1.fna.fbcdn.net/v/t31.0-8/22555553_10208674443253424_8742489099592047203_o.jpg?_nc_cat=102&_nc_ht=scontent.fktm3-1.fna&oh=a7e615831bf516f5d66f11541fc76db6&oe=5D0D31AC'
  }),
  computed: {
    binding () {
      const binding = {}

      if (this.$vuetify.breakpoint.mdAndUp) binding.column = true

      return binding
    }
  }
}
</script>
