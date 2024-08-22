<template>
  <div class="pt-10 pb-10 pa-md-10">
    <div>
      <h2 class="text-h4 text-md-h3 text-center font-weight-bold team-title">Our Team</h2>
    </div>
    <div>
      <p class="text-md-h6 text-center pa-10 team-paragraph">
        Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat.
      </p>
    </div>

    <v-container max-width="1280">
      <v-row align-content="center">
        <v-col v-for="(member, index) in teamMembers" :key="index" cols="12" sm="6" md="4">
          <v-card class="mx-auto pa-2 rounded-te-xl" max-width="400" height="auto">
            <v-img :src="member.image" aspect-ratio="1/1"></v-img>
            <v-card-text class="text-subtitle-1 font-weight-bold text-uppercase member-subtitle">{{
              member.title
            }}</v-card-text>
            <v-card-title class="text-h4 text-sm-h5 text-md-h4">{{ member.name }}</v-card-title>
            <v-card-text class="member-description">{{ member.description }}</v-card-text>

            <div class="d-flex justify-center pa-2 mt-4">
              <a
                v-for="(social, i) in member.socialIcons"
                :key="i"
                :href="social.link"
                target="_blank"
                rel="noopener noreferrer"
              >
                <img :src="social.icon" alt="Social Icon" class="mr-5" width="50" />
              </a>
            </div>
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
import image4 from '../assets/images/yy.jpg'
import image5 from '../assets/images/gffgfgg.jpg'
import image6 from '../assets/images/hghg.jpg'
import facebookIcon from '../assets/images/1384005.png'
import instaIcon from '../assets/images/1362894.png'

const teamMembers = [
  {
    name: 'Dr. Bob Brown',
    title: 'General Dentist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum',
    image: image1,
    socialIcons: [
      { icon: facebookIcon, link: 'https://www.facebook.com/drbobbrown' },
      { icon: instaIcon, link: 'https://twitter.com/drbobbrown' }
    ]
  },
  {
    name: 'Dr. Mary Smith',
    title: 'General Dentist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum.',
    image: image2,
    socialIcons: [
      { icon: facebookIcon, link: 'https://www.facebook.com/drmarysmith' },
      { icon: instaIcon, link: 'https://twitter.com/drmarysmith' }
    ]
  },
  {
    name: 'Dr. Nick Dark',
    title: 'Orthodontist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum',
    image: image3,
    socialIcons: [
      { icon: facebookIcon, link: 'https://www.facebook.com/drnickdark' },
      { icon: instaIcon, link: 'https://twitter.com/drnickdark' }
    ]
  },
  {
    name: 'Dr. May Dowson',
    title: 'Endodontist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum',
    image: image4,
    socialIcons: [
      { icon: facebookIcon, link: 'https://www.facebook.com/drmaydownson' },
      { icon: instaIcon, link: 'https://twitter.com/drmaydownson' }
    ]
  },
  {
    name: 'Dr. Betty Nilson',
    title: 'Pediatric Dentist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum',
    image: image5,
    socialIcons: [
      { icon: facebookIcon, link: 'https://www.facebook.com/drbettynilson' },
      { icon: instaIcon, link: 'https://twitter.com/drbettynilson' }
    ]
  },
  {
    name: 'Dr. Adrian Scold',
    title: 'Orthodontist',
    description:
      'Glavi amet ritnisl libero molestie ante ut fringilla purus eros quis glavrid from dolor amet iquam lorem bibendum',
    image: image6,
    socialIcons: [
      { icon: facebookIcon, link: 'https://www.facebook.com/dradrianscold' },
      { icon: instaIcon, link: 'https://twitter.com/dradrianscold' }
    ]
  }
]
</script>
