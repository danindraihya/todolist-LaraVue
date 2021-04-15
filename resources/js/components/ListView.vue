<template>
    <div>
        <div v-for="item in items" :key="item.id">
            <list-item 
                :item="item"
                class="item"
                :itemChanged="$emit('reloadList')"
             />
        </div>
    </div>
</template>

<script>
    import ListItem from './ListItem.vue'

export default {
    props: ['items'],
    components: {
        ListItem
    }
}
</script>