<template>
    <div class="select">
        <label for="gender-select">Filter by gender: </label>
        <select name="gender" id="gender-select" v-model="selected" @change="$emit('changed', selected)">
            <option value="all">All</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'Select',
    data() {
            return {
                selected: 'all',
            }
        }
}
</script>

<style lang="scss" scoped>
.select {
    text-align: center;
    color: #fff;
    padding-top: 20px;
}

</style>