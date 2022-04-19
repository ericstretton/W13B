<template>
    <div >
        <p>{{tweetContent}}</p>
        <h3>{{user}}</h3>
        <h6>{{dateCreated}}</h6>
        
    </div>
</template>

<script>
    export default {
        name: "TweetCard",
        props: {
            id: Number, 
            user: String,
            tweetContent: String, 
            dateCreated: String,
        },
        data() {
            return {
                
            }
        },
        
    }
</script>

<style lang="scss" scoped>
div{
    position: relative;
    left: 10vw;
    background-color: rgb(194, 171, 171);
    border: solid 2px white;
    margin: 10px;
    width: 80%;
    p{
        font-size: 1.5em;
    }
}
.grid{
    display: grid;
    position: relative;
    grid-template-rows: 1fr 1fr 1fr;
    grid-template-columns:  1fr 2fr;
    p{
        grid-row-start: 1;
        grid-row-end: 3;
        grid-column-start: 2;
        grid-column-end: 2;
        
    }
    h3{
        grid-row-start: 1;
    }
    h6{
        grid-row-start: 3;
        grid-column-start: 2;
    }
    button{
        grid-row-start: 3;
        grid-column-start: 2;
        width: 15vw;
        
    }
}

</style>