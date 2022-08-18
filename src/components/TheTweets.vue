<template>
    <div>
        <button onclick = "this.grid_this()">change view</button>
        <h1>testing</h1>
    </div>
</template>

<script>
    export default {
        data: function() {
            return [{
                tweet: `Your tweet here!`,
                user:  `some_user`,
                date: `Jun 1, 2021`
            },
            {
                tweet: `Your tweet here too!`,
                user:  `some_user_2`,
                date: `Jun 2, 2021`
            },
            {
                tweet: `Your tweet here too too!`,
                user:  `some_user_3`,
                date: `Jun 3, 2021`
            },
            {
                tweet: `Your tweet here too now!`,
                user:  `some_user_4`,
                date: `Jun 4, 2021`
            },
            {
                tweet: `Your tweet here next!`,
                user:  `some_user_5`,
                date: `Jun 5, 2021`
            },
            {
                tweet: `Your tweet here next next!`,
                user:  `some_user_6`,
                date: `Jun 6, 2021`
            },
            {
                tweet: `Your tweet here blah!`,
                user:  `some_user_7`,
                date: `Jun 7, 2021`
            },
            ]
        },
        methods: {
            list_all: function() {
                
                for (let i = 0; i<this.$data.length; i++){
                    document.body.insertAdjacentHTML(`beforeend`, `<h3>tweet: ${this.$data[i][`tweet`]}</h3>`)
                }
            }
        },
        mounted () {
            this.list_all();
        },
        name: "the-tweets"
    }
</script>

<style scoped>

</style>