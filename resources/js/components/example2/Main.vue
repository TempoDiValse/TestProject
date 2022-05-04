<template>
    <div>
        <div v-for="({ text, data }, index) in items" :key="index">{{ index + 1 }} : {{ text }} {{ data }}</div>

        <button @click="onClick">Click</button>

        <radio-group :items="items" />

        <span>{{ num }}</span>
    </div>
</template>

<script>
import RadioGroup from '../widget/RadioGroup.vue';

export default {
  components: { RadioGroup },
    props: {
        num: {
            type: Number,
            default: 100
        },

        isEnabled: {
            type: Boolean,
            default: true
        },

        arr: {
            type: Array,
            default(){
                return []
            }
        },

        o : {
            type: Object,
            default() {
                return {
                    id: "radio",
                    text: "과일",
                    data: "fruits"
                }
            }
        }
    },

    name: "Main",

    data(){
        return {
            doToggle: false,
            items : [
                { id: "radio1", text: "사과", data: "apple" },
                { id: "radio2", text: "바나나", data: "banana" },
                { id: "radio3", text: "포도", data: "grape" },
            ],
        }
    },

    methods: {
        onClick(){
            this.items.forEach(({ id, text, data }) => {
                console.log(id+" "+text+" "+data)
            });

            this.doToggle = !this.doToggle
        }
    }
}
</script>
