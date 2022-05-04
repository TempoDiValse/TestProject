<template>
    <div class="main">
        <Header />

        <div class="container">
            <Side />
            <Body />
        </div>
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
    .main { width: 100%; height: 100%; }
    .container { display: flex; width: 100%; height: 100%; }
</style>
