<template>
  <v-app id="inspire">
    <v-app-bar flat>
      <v-container class="my-auto d-flex align-center justify-center">
        <v-spacer></v-spacer>
        <v-btn
          v-for="link in links"
          :key="link"
          :text="link"
          variant="text"
        ></v-btn>
      </v-container>
    </v-app-bar>

    <v-main class="bg-grey-lighten-3">
      <v-container>
        <v-row>
          <v-col cols="12">
            <v-sheet min-height="70vh" rounded="lg" style="height: 100%;">
              <v-carousel height="100%" show-arrows="hover" cycle hide-delimiter-background>
                <v-carousel-item v-for="(image, i) in roomData.property.propertyImages" :key="i">
                  <v-sheet height="700px">
                    <img :src="image.url" :alt="'Slide ' + (i + 1)" class="d-block w-100" style="height: 100%;" />
                  </v-sheet>
                </v-carousel-item>
              </v-carousel>
            </v-sheet>
          </v-col>
          <v-col cols="4">
            <v-sheet min-height="70vh" rounded="lg">
              <v-carousel height="100%" show-arrows="hover">
                <v-carousel-item v-for="(image, i) in roomData.images" :key="i">
                  <v-sheet height="100%">
                    <img :src="image.url" :alt="'Slide ' + (i + 1)" class="d-block w-100" />
                  </v-sheet>
                </v-carousel-item>
              </v-carousel>
              <v-card>
                <v-card-title>{{ roomData.displayName }}</v-card-title>
                <v-card-text>
                  <p><strong>Address:</strong> {{ roomData.property.address }}</p>
                  <p><strong>City:</strong> {{ roomData.property.city }}</p>
                  <p><strong>Room Description:</strong> <span v-html="roomData.roomDescription"></span></p>
                  <p><strong>Max People:</strong> {{ roomData.maxPeople }}</p>
                  <p><strong>Rack Rate:</strong> ${{ roomData.rackRate }}</p>
                  <p><strong>Cleaning Fee:</strong> ${{ roomData.cleaningFee }}</p>
                </v-card-text>
              </v-card>
            </v-sheet>
          </v-col>
          <v-col cols="4" class="mx-auto">
            <v-sheet min-height="70vh" rounded="lg">
              <v-carousel height="100%" show-arrows="hover">
                <v-carousel-item v-for="(image, i) in roomData.images" :key="i">
                  <v-sheet height="100%">
                    <img :src="image.url" :alt="'Slide ' + (i + 1)" class="d-block w-100" />
                  </v-sheet>
                </v-carousel-item>
              </v-carousel>
              <v-card>
                <v-card-title>{{ roomData.displayName }}</v-card-title>
                <v-card-text>
                  <p><strong>Address:</strong> {{ roomData.property.address }}</p>
                  <p><strong>City:</strong> {{ roomData.property.city }}</p>
                  <p><strong>Room Description:</strong> <span v-html="roomData.roomDescription"></span></p>
                  <p><strong>Max People:</strong> {{ roomData.maxPeople }}</p>
                  <p><strong>Rack Rate:</strong> ${{ roomData.rackRate }}</p>
                  <p><strong>Cleaning Fee:</strong> ${{ roomData.cleaningFee }}</p>
                </v-card-text>
              </v-card>
            </v-sheet>
          </v-col>
          <v-col cols="4" class="mx-auto">
            <v-sheet min-height="70vh" rounded="lg">
              <v-carousel height="100%" show-arrows="hover">
                <v-carousel-item v-for="(image, i) in roomData.images" :key="i">
                  <v-sheet height="100%">
                    <img :src="image.url" :alt="'Slide ' + (i + 1)" class="d-block w-100" />
                  </v-sheet>
                </v-carousel-item>
              </v-carousel>
              <v-card>
                <v-card-title>{{ roomData.displayName }}</v-card-title>
                <v-card-text>
                  <p><strong>Address:</strong> {{ roomData.property.address }}</p>
                  <p><strong>City:</strong> {{ roomData.property.city }}</p>
                  <p><strong>Room Description:</strong> <span v-html="roomData.roomDescription"></span></p>
                  <p><strong>Max People:</strong> {{ roomData.maxPeople }}</p>
                  <p><strong>Rack Rate:</strong> ${{ roomData.rackRate }}</p>
                  <p><strong>Cleaning Fee:</strong> ${{ roomData.cleaningFee }}</p>
                </v-card-text>
              </v-card>
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
  import roomData from '../src/router/roomData.json'

  const links = ['Dashboard', 'Messages', 'Profile', 'Updates']

  const colors = [
    'indigo',
    'warning',
    'pink darken-2',
    'red lighten-1',
    'deep-purple accent-4',
  ]

  const slides = [
    'First',
    'Second',
    'Third',
    'Fourth',
    'Fifth',
  ]
</script>

<script>
  export default {
    data() {
      return {
        links: ['Dashboard', 'Messages', 'Profile', 'Updates'],
        colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
        ],
        slides: [
          'First',
          'Second',
          'Third',
          'Fourth',
          'Fifth',
        ]
      }
    }
  }
</script>
