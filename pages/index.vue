<template>
    <v-main>
        <v-container fluid>

            Index - landing page
            <v-list lines="one">
                <v-list-subheader>subheader</v-list-subheader>
                    <v-list-item
                        v-for="n in 30"
                        :key="n"
                        :title="'Item ' + n"
                        subtitle="Lorem ipsum dolor sit amet consectetur adipisicing elit"
                    ></v-list-item>
                </v-list>

        </v-container>
    </v-main>
</template>

<script setup>
import { useScreenOrientation } from '@vueuse/core'
const {
    isSupported,
    orientation,
    angle,
    lockOrientation,
    unlockOrientation,
} = useScreenOrientation()

const isPortrait = computed((()=> {
    if(orientation.value === 'landscape-primary' || orientation.value === 'landscape-secondary') {
        return true
    } 
    else return false
}))


</script>