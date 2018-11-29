<template>
    <div>
        <p>This is about page</p>
        <profile></profile>
        <my-button></my-button>
        <MyButton/>
    </div>
</template>

<script>

    import Profile from '../components/myInfo'
    import MyButton from '../components/button'

    export default {
        components: {Profile, MyButton}
    }
</script>