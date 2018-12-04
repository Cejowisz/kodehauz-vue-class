<template>
    <div>

        <div>
            <h1>List of all student</h1>
            <student-list @sayname="alertName" :MoreNames="moreNames" :test="gibberish"></student-list>
        </div>

        {{ windowWidth }}

    </div>
</template>

<script>

    import StudentList from '@/components/studentList'

    export default {

        data() {
            return {
                moreNames: [
                    {name: 'Emeka', email: 'emeka@gmail.com'},
                    {name: 'Graces', email: 'grace@gmail.com'},
                    {name: 'Peace', email: 'peace@gmail.com'}
                ],
                gibberish: 'hjmghhgng'
            }
        },

        components: { StudentList },

        methods: {
            alertName(e) {
                alert(e)
            }
        },

        computed: {
            windowWidth() {
                return window.innerWidth
            }
        },

        mounted() {


                this.$on('say-name', function(e) {
                    alert(e)
                })



        }


    }
</script>