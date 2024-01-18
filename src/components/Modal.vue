<template>
    <div class="backdrop" @click.self="emitClose">
        <div class="modal">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
h1 {
    color: red;
}

.backdrop {
    background: #24242480;
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0
}

.modal {
    background: #FFF;
    padding: 20px;
    margin: 20px;
    border-radius: 10px;
    display: inline-block;
}
</style>

<script>

export default {
    props: ['header'],
    methods: {
        emitClose() {
            this.$emit("close");
        }
    }
}

</script>
