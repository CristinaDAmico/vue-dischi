<template>
  <div class="loader">
        <img src="https://static.vecteezy.com/system/resources/previews/001/826/348/non_2x/progress-loading-bar-buffering-download-upload-and-loading-icon-vector.jpg" alt="loader">
  </div>
</template>

<script>
export default {
    name: 'Loader',
}
</script>

<style lang="scss" scoped>
.loader {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: black;
}

img {
    width: 200px;
    animation: pulse 0.7s infinite alternate;
}

@keyframes pulse {
    from {
        transform:scale(1);
    }
    to {
        transform: scale(1.2);
    }
}

</style>