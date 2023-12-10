<template>
  <div>
    <v-btn-toggle v-model="isDark">
      <v-btn
        size="48px"
        rounded="pill" 
        variant="tonal"
        >
        <v-icon
          color="primary"
          :icon="isDark ? 'mdi-weather-night' : 'mdi-weather-sunny'" 
        />
      </v-btn>
    </v-btn-toggle>
  </div>
</template>

<script setup>
import { useTheme } from 'vuetify'
const theme = useTheme()

const isDark = computed({
  get () {
    return theme.global.current.value.dark
  },
  set () {
    theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
  }
})
</script>