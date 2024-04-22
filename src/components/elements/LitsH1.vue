<template>
    <h1 :class="classes">{{ text }}</h1>
</template>

<script lang="ts">
export default {
    props: [
        'text',
        'classes'
    ]
}
</script>