<template>
    <div>
        <p v-for="(student, i) in students">
            <span>{{ i + 1 }}</span>
            <span>{{ student.name }}</span>
        </p>
        <button @click="$emit('sayname', students[0].name)">Say name</button>
        {{test}}
    </div>
</template>

<script>

    export default {


        /*
        *
        * Communicate from parent to child component using props.
        * Communicate from child to parent component using events.
        *
        * */

        props: ['MoreNames', 'test'],

        data() {
            return {
                students: [
                    {name: 'Janet', email: 'janet@gmail.com', phone: 8098090},
                    {name: 'John', email: 'john@gmail.com', phone: 8098090},
                    {name: 'James', email: 'james@gmail.com', phone: 8098090},
                    {name: 'James', email: 'james@gmail.com', phone: 8098090},
                ]
            }
        },

        methods: {
            /*addMoreNames() {
                this.students = [...this.students, ...this.MoreNames]
            }*/
        },

        mounted() {
            this.students = [...this.students, ...this.MoreNames]
        },

        created() {

        }
    }

</script>