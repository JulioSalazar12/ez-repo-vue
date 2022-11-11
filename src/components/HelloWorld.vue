<template>
  <div class="courses">
    <v-row class="pt-4">
      <v-col cols="12" class="pb-0">
        <h1 class="pl-5">Courses</h1>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <div class="d-flex flex-wrap justify-center mb-8">
          <v-card v-for="course in [{'id':1,'name':'sample','description':'sample2' },{'id':2,'name':'sample','description':'sample2' }, {'id':3,'name':'sample','description':'sample2' }]" :key="course.id" class="pb-2 ma-3" width="290" max-height="450">
            <div class="indigo accent-3">
              <v-card-subtitle class="pb-0 white--text">
                Course
              </v-card-subtitle>
              <v-card-title class="pb-1 pt-0 white--text font-weight-bold">
                {{course.name}}
              </v-card-title>
            </div>
            <v-card-text class="text-justify pb-1 text--secondary text-truncate">
              <strong>Description:</strong> {{course.description}}
            </v-card-text>
            <v-card-actions>
              <v-btn text color="indigo accent-4" class="font-weight-bold te" :to="`/courses/${course.id}`">see more</v-btn>
            </v-card-actions>
          </v-card>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      ecosystem: [
        {
          text: 'vuetify-loader',
          href: 'https://github.com/vuetifyjs/vuetify-loader',
        },
        {
          text: 'github',
          href: 'https://github.com/vuetifyjs/vuetify',
        },
        {
          text: 'awesome-vuetify',
          href: 'https://github.com/vuetifyjs/awesome-vuetify',
        },
      ],
      importantLinks: [
        {
          text: 'Documentation',
          href: 'https://vuetifyjs.com',
        },
        {
          text: 'Chat',
          href: 'https://community.vuetifyjs.com',
        },
        {
          text: 'Made with Vuetify',
          href: 'https://madewithvuejs.com/vuetify',
        },
        {
          text: 'Twitter',
          href: 'https://twitter.com/vuetifyjs',
        },
        {
          text: 'Articles',
          href: 'https://medium.com/vuetify',
        },
      ],
      whatsNext: [
        {
          text: 'Explore components',
          href: 'https://vuetifyjs.com/components/api-explorer',
        },
        {
          text: 'Select a layout',
          href: 'https://vuetifyjs.com/getting-started/pre-made-layouts',
        },
        {
          text: 'Frequently Asked Questions',
          href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
        },
      ],
    }),
  }
</script>
