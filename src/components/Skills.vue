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
        <h1 class="display-2 font-weight-bold mb-3">Skills</h1>
        <h3 class="subheading">{{ title }}</h3>
        <div class="text-xs-center">
          <v-container fluid grid-list-sm>
            <v-layout row wrap>
              <v-flex v-for="(skill, i) in skills" :key="i" xs3>
                <v-progress-circular
                  :rotate="360"
                  :size="100"
                  :width="15"
                  :value="skill.value"
                  :color="skill.color"
                >
                  {{ skill.value }}
                </v-progress-circular>
                <v-flex
                  xs6
                  text-uppercase
                  v-text="skill.name"
                  :color="skill.color"
                />
              </v-flex>
            </v-layout>
          </v-container>
        </div>
      </v-layout>
    </v-parallax>
  </v-container>

</template>

<script>
export default {
  data: () => ({
    skills: [
      {
        name: 'Research',
        color: 'teal',
        value: '30'
      },
      {
        name: 'Design',
        color: 'red',
        value: '30'
      },
      {
        name: 'Development',
        color: 'red',
        value: '30'
      },
      {
        name: 'Support',
        color: 'red',
        value: '30'
      }
    ],
    bgimage: 'https://images.unsplash.com/photo-1470790376778-a9fbc86d70e2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=698&q=80'
  })
}
</script>
