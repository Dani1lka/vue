<template>
    <button class="btn" :class="color" @click="$emit('action')">
        <slot />
    </button>
</template>

<script>
export default{
    name:"appButton",
    emits:['action'],
    props:{
        
        color:{
            type: String,
            default: '',
            validator(value){
                return ['','primary','danger'].includes(value)          
            }
        },
    }
}
</script>