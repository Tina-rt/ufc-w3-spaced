<script>
export default{
    props:{
        img: ''
    }
}
</script>

<template>
    <img :src="img" :alt="img">
</template>