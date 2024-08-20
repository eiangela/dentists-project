<template>
  <div>
    <div class="pt-10">
      <h2 class="text-h4 text-md-h3 text-center font-weight-bold team-title">Our Team</h2>
    </div>
    <div>
      <p class="text-md-h6 text-center pt-10 team-paragraph">
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat.
      </p>
    </div>

    <v-container>
      <v-row>
        <v-col v-for="(member, index) in teamMembers" :key="index" cols="12" md="2">
          <v-card class="mx-auto" max-width="344">
            <v-img :src="member.image" height="200px" cover></v-img>
            <v-card-text>{{ member.title }}</v-card-text>
            <v-card-title>{{ member.name }}</v-card-title>
            <v-card-text>{{ member.description }}</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script setup>
import image1 from '../assets/images/1.jpg'
import image2 from '../assets/images/2.jpg'
import image3 from '../assets/images/jhhhj6.jpg'

const teamMembers = [
  {
    name: 'Dr. Bob Brown',
    title: 'General Dentist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum',
    image: image1
  },
  {
    name: 'Dr. Mary Smith',
    title: 'General Dentist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum.',
    image: image2
  },
  {
    name: 'Dr. Nick Dark',
    title: 'Orthodontist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum',
    image: image3
  }
]
</script>
