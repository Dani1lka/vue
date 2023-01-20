<template>
    <div class="card">
        <slot name="header"></slot>
        <slot name="default"></slot>
        <slot name="footer"></slot>
    </div>
</template>

<script>
export default{
    name:'appBlock'
}
</script>