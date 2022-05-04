<template>
    <div>
        <Header />
        <Side />
        <Body />
    </div>
</template>

<script>
import Header from "./Header"
import Side from "./Side"
import Body from "./Body"

export default {
    name: "Main",
    components: { Header, Side, Body }
}
</script>

<style>

</style>
