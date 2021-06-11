<template>
    <li class="test">
        <h1> {{ title }}</h1>
    </li>
</template>

<script>

export default {
    name: 'Card',
    props: ['title']
}
</script>

<style scoped>
    h1 {
        color: red;
    }
    .test {
        border: 4px, double, black;
        padding: 20px;
    }
</style>
