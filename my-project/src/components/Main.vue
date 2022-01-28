<template>
    <div>
        <div class="container">
            <my-header></my-header>
            <card-block></card-block>
        </div>
    </div>
</template>

<script>
import CardBlock from './Card.vue'
import MyHeader from './Header.vue';
export default {
    components: { MyHeader, CardBlock }
}
</script>