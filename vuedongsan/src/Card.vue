<template>
    <div>
        <img :src="room.image" class="room-img">
        <!-- <h4 @click="모달창열렸니 = true; 누른거 = i">{{ room.title }}</h4> -->
        <p>{{ room.price }}원</p>
    </div>
</template>


<script>
export default {
    name: 'Card',
    props: {
        room: Object,
        i: Number,

    }
}
</script>

<style></style>