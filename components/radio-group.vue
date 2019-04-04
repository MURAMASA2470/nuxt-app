<template>
    <div>
        <div class="content-area" v-for="item in items" :key="item.id">
            <h2>{{ item.title }}</h2>
            <small>{{ item.description }}</small>
            <btn-style-radio :contents="item.contents"></btn-style-radio>
        </div>
    </div>
</template>

<script>
import BtnStyleRadio from '~/components/btn-style-radio.vue'

export default {
    components: {
        BtnStyleRadio
    },
    props: ['items'], 
    data() {
        return {

        }
    }     
}
</script>

<style lang="sass" scoped>

</style>
