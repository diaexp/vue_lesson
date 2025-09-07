<template>
    <div class="black-bg" v-if="모달창열렸니">
        <div class="white-bg">
            <h4>{{ 원룸들[누른거].title }}</h4>
            <img :src="원룸들[누른거].image" style="width:100%">
            <p>{{ 원룸들[누른거].content }}</p>
            <p>{{ 원룸들[누른거].price }}원</p>
            <button @click="$emit('closeModal')">닫기</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Modal',
    props : {
        모달창열렸니 : Boolean,
        원룸들 : Array,
        누른거 : Number
    }
}
</script>

<style></style>