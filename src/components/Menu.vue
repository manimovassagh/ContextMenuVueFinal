<template>
    <div @contextmenu="show" class="ma-0 pa-0">
        <slot></slot>

        <v-menu
            v-model="showMenu"
            :position-x="x"
            :position-y="y"
            absolute
            offset-y
            class="ma-0 pa-0"
        >
            <v-list>
                <v-list-item v-for="(item, index) in items" :key="index" link>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item>
            </v-list>
        </v-menu>
    </div>
</template>
<script>
export default {
    data: () => ({
        showMenu: false,
        x: 0,
        y: 0,
        items: [
            { title: 'Click Me' },
            { title: 'Click Me' },
            { title: 'Click Me' },
            { title: 'Click Me 2' }
        ]
    }),

    methods: {
        show(e) {
            e.preventDefault()
            this.showMenu = false
            this.x = e.clientX
            this.y = e.clientY
            this.$nextTick(() => {
                this.showMenu = true
            })
        }
    }
}
</script>
<style scoped>
</style>