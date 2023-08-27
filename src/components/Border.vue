<template>
    <div class="border-main">
        <div class="border-bar"></div>
    </div>
</template>

<style scoped]>
@keyframes anim_border {
    0%{
        transform: translateX(-100%);
    }
    50%{
        transform: translateX(500%)
    }
    100%{
        transform: translateX(-100%);
    }
}
.border-main {
    margin: 30px 0;
    width: 100%;
    height: 2px;
    background-color: rgba(255, 255, 255, 0.205);
    overflow: hidden;
    /* border: 1px solid white; */
}

.border-bar {
    width: 20%;
    height: 2px;
    background-color: var(--color-btn);
    animation: anim_border 6s infinite ease;
}
</style>