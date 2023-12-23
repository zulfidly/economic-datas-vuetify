
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
            <v-main>
                <slot />
            </v-main>
            <v-navigation-drawer
                location="left"
                :permanent="true"
                >
                <NavItems />
            </v-navigation-drawer>
        </v-app>
</template>

<script setup>
</script>