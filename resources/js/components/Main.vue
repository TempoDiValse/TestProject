<template>
    <div>
        <sub-1 :title="sub1" />
        <sub-2 :name="sub2" />
        <sub-3 ref="sub3" />
        <button @click="onMessage">가져오기</button>
        <radio-group v-model="radioValue" /> {{ radioValue }}
    </div>
</template>

<script>
import Sub1 from "./Sub1"
import Sub2 from "./Sub2"
import Sub3 from "./Sub3"

import RadioGroup from './widget/RadioGroup.vue'

export default {
    name: "Main",
    components: { Sub1, Sub2, Sub3, RadioGroup },
    data(){
        return {
            sub1: "received from parent",
            sub2: "이종일",
            radioValue: '',
        }
    },

    methods: {
        onMessage(){
            this.sub1 = this.$refs.sub3.getMessage()
        }
    }
}
</script>
