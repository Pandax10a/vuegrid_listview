<template>
    <div>
        <button @click="change_on()">change view</button>
        <br><br>
        <section :class = "{section_container: isOn}">
            <article class = "article_container" v-for = "(person, index) in list_of_people" :key="index" >
                <p>{{list_of_people[index][`user`]}}</p>
                <p>{{list_of_people[index][`tweet`]}}</p>
                <p>{{list_of_people[index][`date`]}}</p>
            </article>
        </section>
        <p>{{this.$data[`list_of_people`][3][`tweet`]}}</p>
        <p>{{this.$data[`isOn`]}}
        
        <h1>testing</h1>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
            list_of_people: [{
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
                ],
                isOn: true
            }
            
        },
        methods: {
            list_all: function() {
                
                for (let i = 0; i<this.$data.length; i++){
                    document.this.$refs.toggle_change.insertAdjacentHTML(`beforeend`, `<div class = "change" <h3>user: ${this.$data[i][`user`]} <br>tweet: ${this.$data[i][`tweet`]}
                    <br>date: ${this.$data[i][`date`]}</h3> </div`)
                }
            },
            change_on: function() {
                if (this.$data[`isOn`]) {
               this.$data[`isOn`] = false;
               
                } else if (this.$data[`isOn`] === false) {
                    this.$data[`isOn`] = true
                    
                }
               
               
            }
        },
        mounted () {
        //    this.list_all();
            // document.body.querySelector(`#click_here`).addEventListener(`click`, this.grid_this)
            // this.change_on()
        },
        name: "the-tweets"
    }
</script>

<style scoped>
.section_container {
    display: grid;
    place-content: center;
    grid-template-columns:1fr 1fr 1fr ;
    row-gap: 20px;
    
}
.article_container {
    display: grid;
    place-content: center;
    background-color: grey;
    box-shadow: 5px 5px 5px 5px blue;
    
    
    
    
    
    width: 30vw;
}

</style>