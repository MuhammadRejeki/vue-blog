<template>
    <h1>Computed</h1>
    <input type="text" v-model="search">
    <p>search term - {{ search }}</p>
    <div v-for="name in MatchingName" :key="name">
        {{ name }}
    </div>
</template>

<script>
import { ref , computed} from 'vue'

export default {
    setup() {
        const search = ref(null)
        const names = ref(['mario','yoshi','toad','budi','lala','koopa','rainer','salsa'])

        const MatchingName = computed(() => {
            return names.value.filter((name) => name.includes(search.value));
        })

        return { search, names ,MatchingName}
    },
}
</script>