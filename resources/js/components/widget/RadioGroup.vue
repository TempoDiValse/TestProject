<template>
    <div>
        <radio-button v-for="(item, index) in items" :key="index"
            :id="item.id"
            :name="name"
            v-model="selected"
            :text="item.text"
            :data="item.data" />
    </div>
</template>

<script>

import RadioButton from './RadioButton.vue'

export default {
    name: "RadioGroup",

    props: {
        value: String,
        items: Array,
    },

    components: { RadioButton },
    data(){
        return {
            name: "group",
            selected: null,
        }
    },

    watch: {
        selected(val){
            this.$emit('change', val);
        }
    },

    model: {
        event: 'change',
        prop: 'value'
    }
}

</script>
