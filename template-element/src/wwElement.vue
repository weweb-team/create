<template>
    <div class="my-element">
        <p :style="textStyle">I am a custom element !</p>
    </div>
</template>

<script>
export default {
    name: "__COMPONENT_NAME__",
    wwDefaultContent: {
        textColor: "#F23636",
    },
    props: {
        content: { type: "Object", required: true },
    },
    computed: {
        textStyle() {
            return {
                color: this.content.textColor,
            };
        },
    },
};
</script>

<style lang="scss" scoped>
.my-element {
    p {
        font-size: 18px;
    }
}
</style>
