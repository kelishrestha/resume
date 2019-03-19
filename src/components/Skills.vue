<template>
  <v-container
    grid-list-xl
    fluid
    pa-0
  >
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
        <h1
          class="display-2 font-weight-bold mb-3 teal--text text-uppercase mt-5"
        >
          Skills
        </h1>
        <v-container
          fluid
          grid-list-sm
        >
          <div class="text-xs-center pl-5 pr-5">
            <v-carousel>
              <v-carousel-item
                v-for="(category,i) in skills"
                :key="i"
                height="300"
              >
                <v-container
                  fluid
                  grid-list-sm
                >
                  <h3 class="display-1 text-capitalize red--text">
                    {{ category.name }}
                  </h3>
                  <v-layout
                    row
                    wrap
                  >
                    <v-flex
                      v-for="(skill, j) in category.data"
                      :key="j"
                      xs2
                    >
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
                        xs12
                        text-uppercase
                        :class="skill.textcolor"
                        v-text="skill.name"
                      />
                    </v-flex>
                  </v-layout>
                </v-container>
              </v-carousel-item>
            </v-carousel>
          </div>
        </v-container>
      </v-layout>
    </v-parallax>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    skills: [
      {
        name: 'programming languages',
        data: [
          {
            name: 'Ruby',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'Javascript',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'JQuery',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'HTML',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'CSS',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'Golang(Basic)',
            color: 'teal',
            textcolor: 'teal--text',
            value: '30'
          },
          {
            name: 'AJAX',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'ReactJS(Basic)',
            color: 'teal',
            textcolor: 'teal--text',
            value: '30'
          },
          {
            name: 'VueJS(Basic)',
            color: 'teal',
            textcolor: 'teal--text',
            value: '30'
          }
        ]
      },
      {
        name: 'frameworks',
        data: [
          {
            name: 'Ruby on Rails',
            color: 'teal',
            textcolor: 'teal--text',
            value: '85'
          },
          {
            name: 'Sinatra',
            color: 'teal',
            textcolor: 'teal--text',
            value: '70'
          },
          {
            name: 'Grape',
            color: 'teal',
            textcolor: 'teal--text',
            value: '70'
          },
          {
            name: 'Node',
            color: 'teal',
            textcolor: 'teal--text',
            value: '60'
          },
          {
            name: 'React Native',
            color: 'teal',
            textcolor: 'teal--text',
            value: '30'
          },
          {
            name: 'Bootstrap',
            color: 'teal',
            textcolor: 'teal--text',
            value: '90'
          }
        ]
      },
      {
        name: 'database and web services',
        data: [
          {
            name: 'Postgres',
            color: 'teal',
            textcolor: 'teal--text',
            value: '70'
          },
          {
            name: 'Redis',
            color: 'teal',
            textcolor: 'teal--text',
            value: '70'
          },
          {
            name: 'MongoDB',
            color: 'teal',
            textcolor: 'teal--text',
            value: '70'
          },
          {
            name: 'MySQL',
            color: 'teal',
            textcolor: 'teal--text',
            value: '70'
          },
          {
            name: 'Redux',
            color: 'teal',
            textcolor: 'teal--text',
            value: '30'
          },
          {
            name: 'Amazon S3',
            color: 'teal',
            textcolor: 'teal--text',
            value: '30'
          }
        ]
      },
      {
        name: 'project management tools',
        data: [
          {
            name: 'Jira',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'Trello',
            color: 'teal',
            textcolor: 'teal--text',
            value: '90'
          },
          {
            name: 'Honeybadger',
            color: 'teal',
            textcolor: 'teal--text',
            value: '30'
          },
          {
            name: 'LogEntries',
            color: 'teal',
            textcolor: 'teal--text',
            value: '50'
          }
        ]
      },
      {
        name: 'version control tools',
        data: [
          {
            name: 'Github',
            color: 'teal',
            textcolor: 'teal--text',
            value: '90'
          },
          {
            name: 'Gitlab',
            color: 'teal',
            textcolor: 'teal--text',
            value: '90'
          },
          {
            name: 'Bitbucket',
            color: 'teal',
            textcolor: 'teal--text',
            value: '90'
          }
        ]
      },
      {
        name: 'software and operating systems',
        data: [{
          name: 'Support',
          color: 'teal',
          textcolor: 'teal--text',
          value: '30'
        }]
      },
      {
        name: 'software development methodology',
        data: [
          {
            name: 'Agile Methodology with Scrum Process',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'KanBan',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          },
          {
            name: 'Rapid Development',
            color: 'teal',
            textcolor: 'teal--text',
            value: '80'
          }
        ]
      }
    ],
    bgimage: 'https://images.unsplash.com/photo-1513542789411-b6a5d4f31634?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1567&q=80'
  })
}
</script>
<style scoped>
  .v-parallax {
    height: 90vh !important;
  }
</style>
