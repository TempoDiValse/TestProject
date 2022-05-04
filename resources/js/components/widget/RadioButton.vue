<template>
    <label :for="id">
        <input type="radio" :id="id" :name="name" :value="data" @change="$emit('change', data)" />
        {{ text }}
    </label>
</template>

<script>

export default {
    name: "RadioButton",
    props: [ "id", "value", "text", "name", "data" ],
    model: {
        event: 'change',
        prop: 'value'
    }
}

</script>
