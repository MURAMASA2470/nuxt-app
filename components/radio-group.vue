<template>
    <div>
        <v-card class="content-area mb-3" v-for="(item) in items" :key="item.id">
            <v-card-title>
                <div>
                    <h2 v-html="item.title"></h2>
                    <small v-html="item.description"></small>
                </div>
            </v-card-title>
            <v-card-text>
                <btn-style-radio :contents="item.contents" :groupName="item.groupName"></btn-style-radio>
            </v-card-text>
            <v-car-action>

            </v-car-action>
        </v-card>
    </div>
</template>

<script>
import BtnStyleRadio from '~/components/btn-style-radio.vue'

export default {
    components: {
        BtnStyleRadio
    },
    props: { items : Object }, 
    data() {
        return {

        }
    }     
}
</script>

<style lang="scss" scoped>
    .content-area {
        width: 500px;
    }
</style>
