<template>
    <div class="image-container">
        <div class="image-frame">
            <img class="image" :src="imageUrl" alt="Hu Tao">
        </div>
        <p class="text">Hu Tao estuvo aquí</p>
    </div>
</template>

<script>
export default {
    name: "ImageFrame",
    props: {
        imageUrl: {
            type: String,
            required: true,
        },
    },
};
</script>

<style scoped>
.image-container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.image-frame {
    width: 320px;
    height: 320px;
    border-radius: 50%;
    border: 8px solid #eee;
    overflow: hidden;
}

.image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.text {
    font-size: 24px;
    font-weight: bold;
    margin-top: 16px;
}
</style>
