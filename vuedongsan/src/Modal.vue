<template>
    <div class="black-bg" v-if="모달창열렸니">
        <div class="white-bg">
            <h4>{{ 원룸들[누른거].title }}</h4>
            <img :src="원룸들[누른거].image" style="width:100%">
            <p>{{ 원룸들[누른거].content }}</p>
            <input v-model.number="month">
            <p> {{ month }}개월 선택함 : {{ 원룸들[누른거].price * month }}원</p>
            <button @click="$emit('closeModal')">닫기</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Modal',
    data() {
        return {
            month : 1,
        }
    },
    watch : {
        month(a) {
            if (isNaN(a)) {
                alert('글자 적지 마셈');
                this.month = 1;
            }
        }
    },
    props : {
        모달창열렸니 : Boolean,
        원룸들 : Array,
        누른거 : Number
    },
    beforeUpdate() {
        if (this.month == 2) {
            alert('2개월은 너무 적음.. 안팝니다');
            this.month = 3;
        }
    }
}
</script>

<style></style>