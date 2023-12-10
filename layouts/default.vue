
<template>
        <v-app>
            <v-app-bar >
                <v-toolbar>
                    <v-toolbar-title>
                        logo
                    </v-toolbar-title>
                    <ColorModeSwitch />
                </v-toolbar>
            </v-app-bar>
            <slot />
            <v-navigation-drawer
                location="left"
                :permanent="true"
                >
                <v-card title="BNM">
                    <v-list>
                            <v-list-item title="Home" prepend-icon="mdi-home"></v-list-item>

                            <v-list-group value="Group">
                                <template v-slot:activator="{ props }">
                                    <v-list-item
                                        v-bind="props"
                                        prepend-icon="mdi-account-circle"
                                        title="Users"
                                    ></v-list-item>
                                </template>

                                <v-list-group value="Admin">
                                    <template v-slot:activator="{ props }">
                                        <v-list-item
                                        v-bind="props"
                                        title="Admin"
                                        ></v-list-item>
                                    </template>

                                    <v-list-item
                                        v-for="([title, icon], i) in data.admins"
                                        :key="i"
                                        :title="title"
                                        :prepend-icon="icon"
                                        :value="title"
                                    ></v-list-item>
                                </v-list-group>
                            </v-list-group>
                    </v-list>
                </v-card>
            </v-navigation-drawer>
        </v-app>
</template>

<script setup>
 const titles = ref(
     [
        {
            "group": "BNM",
            "category": "Other Indicators",
            "title": "Government Securities Yield"
        },
        {
            "group": "Benk",
            "category": "Payment Statistic",
            "title": "Basic Payment Indicator"
        },
        {
            "group": "BNM",
            "category": "Rates and Volume",
            "title": [
                "Exchange Rates",
                "Financial Consumer Alert"
            ]  
        },
    ])

    const data = {
      open: ['Users'],
      admins: [
        ['Management', 'mdi-account-multiple-outline'],
        ['Settings', 'mdi-cog-outline'],
      ],
      cruds: [
        ['Create', 'mdi-plus-outline'],
        ['Read', 'mdi-file-outline'],
        ['Update', 'mdi-update'],
        ['Delete', 'mdi-delete'],
      ],
    }
</script>