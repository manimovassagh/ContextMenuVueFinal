<template>
    <v-app>
        <v-main>
            <Menu>
                <v-container class="ma-0 pa-0" fluid>
                    <div>check</div>
                    <div>check</div>
                  
                </v-container>
            </Menu>
        </v-main>
    </v-app>
</template>

<script>
import Menu from '@/components/Menu.vue'
export default {
    components: {
        Menu
    },
    data: () => ({
        collapseOnScroll: true
    })
}
</script>

<style>
</style>
