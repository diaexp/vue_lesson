<template>
    <div>
        <img :src="room.image" class="room-img">
        <h4 @click="$emit('openModal', room.id)">{{ room.title }}</h4>
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