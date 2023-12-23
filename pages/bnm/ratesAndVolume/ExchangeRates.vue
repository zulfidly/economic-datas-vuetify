<template>
    <v-card>
        <v-breadcrumbs :items="bcItems">
            <template v-slot:prepend>
                <v-icon size="small" icon="$vuetify"></v-icon>
            </template>
            <template v-slot:divider>
                <v-icon icon="mdi-chevron-right"></v-icon>
            </template>
        </v-breadcrumbs>

        exchange rates
    </v-card>
</template>

<script setup>
definePageMeta({
    group: 'BNM',
    category: 'Rates and Volume',
    title: 'Exchange Rates',
})

const bcItems = [
        {
          title: 'BNM',
          disabled: false,
          href: '',
        },
        {
          title: 'Rates and Volume',
          disabled: false,
          href: '',
        },
        {
          title: 'Exchange Rates',
          disabled: true,
          href: '',
        },
      ]
</script>