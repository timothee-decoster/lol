<template>
    <div class="content">
        <router-view/>
    </div>
</template>

<script>
export default {
    name: 'Content'
};
</script>

<style>
.content {
    top: 65px;
    left: 100px;
    position: absolute;
}
</style>
