<template>
    <h2 :class="classes">{{ text }}</h2>
</template>

<script lang="ts">
export default {
    props: [
        'text',
        'classes'
    ]
}
</script>