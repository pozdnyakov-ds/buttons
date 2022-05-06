<template>
    <button class="btn" :class="color" @click="$emit('action')">
        {{ text }}
    </button>
</template>

<script>
    export default {
        emits: ['action'],
        props: {
            text: String,
            color: {
                type: String,
                default: '',
                validator(value) {
                    return ['', 'primery', 'danger'].includes(value)
                }
            }
        }
        
    }
</script>

<style lang="scss" scoped>

</style>