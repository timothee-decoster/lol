<template>
    <div class="info">
    <h1 class="title">
        <pre>&lt;zap-slideout&gt;</pre>
    </h1>
    <p class="description">Give it a jolt. Click <strong>Open</strong> at the top.</p>
    </div>
</template>

<script>
export default {
    name: 'Home'
};
</script>

<style>
.info {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%);
    text-align: center;
}

.title {
    font-size: 24px;
    font-weight: 600;
}

strong {
    font-weight: 600;
}

.description {
    margin-top: 20px;
}
</style>
