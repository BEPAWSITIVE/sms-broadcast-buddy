<script setup lang="ts">
import { mdiSend, mdiCow, mdiLeaf, mdiHeart } from '@mdi/js'

definePageMeta({
  layout: 'website',
  middleware: ['redirect-to-threads'],
})

useSeoMeta({
  title: 'Broadcast Buddy - by Peepal Farm',
  description: 'Broadcast Buddy is an SMS gateway tool built for Peepal Farm to manage communications and broadcasts.',
  ogTitle: 'Broadcast Buddy - by Peepal Farm',
  ogDescription: 'Broadcast Buddy is an SMS gateway tool built for Peepal Farm to manage communications and broadcasts.',
})

const runtimeConfig = useRuntimeConfig()
const appName = runtimeConfig.public.appName || 'Broadcast Buddy'
</script>

<template>
  <v-main class="bg-surface">
    <section class="py-16 text-center">
      <v-container>
        <v-row justify="center">
          <v-col cols="12" md="8">
            <v-img
              src="/logo.png"
              alt="Peepal Farm Logo"
              max-width="200"
              class="mx-auto mb-8"
            ></v-img>
            
            <h1 class="text-h2 font-weight-bold mb-4 text-green-darken-3">
              Broadcast Buddy
            </h1>
            <p class="text-h5 text-medium-emphasis mb-8">
              Empowering Peepal Farm with seamless SMS broadcasting using your own Android devices.
            </p>
            
            <v-btn
              color="green-darken-3"
              size="x-large"
              prepend-icon="mdi-login"
              to="/login"
              class="text-none mr-4"
              elevation="2"
            >
              Get Started
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="py-16 bg-grey-lighten-4">
      <v-container>
        <v-row>
          <v-col cols="12" md="4" class="text-center">
            <v-icon :icon="mdiHeart" size="64" color="green-darken-2" class="mb-4"></v-icon>
            <h3 class="text-h5 font-weight-bold mb-2">Connect Supporters</h3>
            <p class="text-body-1 text-medium-emphasis">Easily reach out to donors, volunteers, and supporters in seconds.</p>
          </v-col>
          <v-col cols="12" md="4" class="text-center">
            <v-icon :icon="mdiSend" size="64" color="green-darken-2" class="mb-4"></v-icon>
            <h3 class="text-h5 font-weight-bold mb-2">Instant Broadcasts</h3>
            <p class="text-body-1 text-medium-emphasis">Send bulk SMS messages instantly using your existing Android phones.</p>
          </v-col>
          <v-col cols="12" md="4" class="text-center">
            <v-icon :icon="mdiLeaf" size="64" color="green-darken-2" class="mb-4"></v-icon>
            <h3 class="text-h5 font-weight-bold mb-2">Cost Effective</h3>
            <p class="text-body-1 text-medium-emphasis">Utilize standard mobile carrier plans with no hidden API fees.</p>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </v-main>
</template>
