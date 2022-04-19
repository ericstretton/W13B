<template>
    <div>
        <h1>Assignment Tweets</h1>
        <button 
            v-on:click="button_active_state = !button_active_state"
            name="button"
            >Change Tweet Display
        </button>
        <TweetCard v-for="post in posts"
        v-bind:class="{ 'grid': button_active_state }"
        :key="post.id"
        :user="post.user"
        :tweetContent="post.tweetContent"
        :id="post.id"
        :dateCreated="post.dateCreated"
        />
        
    </div>
</template>

<script>
import TweetCard from "./TweetCard.vue"
    export default {
        name: 'TweetContainer',
        components: {
            TweetCard
        },
        data () {
            return {
                button_active_state: false,
                posts: [
                    {
                        id : 1,
                        user : "Eric",
                        tweetContent : "What do sprinters eat before a race? Nothing, they fast!",
                        dateCreated : "04-14-2022",
                    },
                    {
                        id : 2,
                        user : "Ashley",
                        tweetContent : "I was really angry at my friend Mark for stealing my dictionary. I told him, 'Mark, my words!' ",
                        dateCreated : "03-26-2022",
                    },
                    {
                        id : 3,
                        user : "Eric",
                        tweetContent : "Do you know the last thing my grandfather said to me before he kicked the bucket? 'Grandson, watch how far I can kick this bucket' ",
                        dateCreated : "02-11-2022",
                    },
                    {
                        id : 4,
                        user : "Ashley",
                        tweetContent : "Why did the scarecrow win an award? Because he was outstanding in his field!",
                        dateCreated : "04-18-2022",
                    },
                    {
                        id : 5,
                        user : "Eric",
                        tweetContent : "What kind of music did the pilgrims listen to? Plymouth rock.",
                        dateCreated : "04-17-2022",
                    },
                    {
                        id : 6,
                        user : "Bob",
                        tweetContent : "What do you call it when Dwayne Johnson buys a cutting tool? Rock pay-for scissors.",
                        dateCreated : "08-16-2011",
                    },
                ]
            }
        }
    }
</script>

<style lang="sass" scoped>

</style>