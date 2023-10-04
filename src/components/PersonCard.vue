<template>
    <div class="container">
        <img :src="person.image" alt="">
        <div class="person-details">
            <div>
                <strong>Last Name</strong> {{person?.lastName}}
            </div>
            <div>
                <strong>First Name</strong> {{person?.firstName}}
            </div>
            <div>
                <strong>Email</strong> {{ person?.email }}
            </div>
        </div>
        <div class="buttons">
            <SpecialButton style="flex: 1" title="Like" type="primary" />
            <SpecialButton style="flex: 1" title="Dislike" type="danger" />
        </div>
    </div>
</template>

<script>
import SpecialButton from './SpecialButton.vue';

export default {
    props: {
        person: Object
    },
    components: {
        SpecialButton,
    }
}

</script>

<style scoped>
img {
    width: 100%;
}

.buttons {
    display: flex;
    gap: 4px;
}
.container {
    max-width: 200px;
    border: 1px solid #888;
    padding: 12px;
    border-radius: 8px;
    box-shadow: 0px 0px 5px #888;
    margin: 16px 0;
}

</style>