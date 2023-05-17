<template>
    <div :class="open ? 'acord open' : 'acord'" @click="$emit('toggleOpen', index)">
        <div class="question">{{ acord.question }}</div>
        <div class="answer">{{ acord.answer1 }}</div>
        <div class="answer">{{ acord.answer2 }}</div>
        <div class="answer">{{ acord.answer3 }}</div>
    </div>
</template>

<script>
export default{
    name: 'FAQ',
    props: ['acord', 'index', 'open']
}
</script>

<style>

</style>