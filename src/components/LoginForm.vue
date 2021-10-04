<template>
    <div>
        <h1>
        {{email}}
        </h1>
        <label for="email">email</label>
        <input v-model="email" type="email" name="email" id="email" :placeholder="emailPlaceholder">
        <br>
        <label for="password">password</label>
        <input v-model="password" type="password" name="pass" id="pass">
        <input type="submit" value="">
    </div>
</template>

<script lang="ts">
export default {
    data() {
        return {
            email: '',
            password: '',
        }
    },
    props: {
        emailPlaceholder: String
    }
};
</script>

<style scoped>

</style>