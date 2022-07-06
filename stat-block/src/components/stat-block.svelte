<script>
   import '../styles/global.css';

   export let Stats;
   console.log("Stats: array of  objects" , Stats);

</script>

<div class="statBlock">
<div class="Flex-Container">
        {#each Stats as stat}
        <div class="a">
        <h1>{stat.EndingNumber} +</h1>
        <h2>{stat.title}</h2>    
        </div>    
        {/each}
    <!-- <div class="b">
        <h1>150+</h1>
        <h2>Product SkUs</h2>
    </div>
    <div class="c">
        <h1>300+</h1>
        <h2>Team Members</h2>
    </div> -->
</div>
</div>

<style>

    .statBlock
    {
        background-color: navy;
        margin-top: 5%;
    }

    .Flex-Container
    {
        display: flex;
        height:300px;
        text-align: center;
        width:85%;
        margin-left: auto;
        margin-right: auto;
        justify-content: space-evenly;
    }

    .a
    {
        width:33.33%;
        padding-top: 50px;
        color:white;
    }


    h1
    {
        font-size: 68px;
    }

    h2
    {
        font-size: 24px;
        font-weight: lighter;
        margin-top: -9%;
    }

    @media screen and (min-width:350px) and (max-width:530px)
    {
    
        
    .Flex-Container
    {
        display: flex;
        height:470px;
        width:100%;
        flex-direction: column;
        justify-content: center;
    }

    .a
    {
        width:98.7%;
        padding-top:0px;
    }

    h2
    {
        margin-top: -8%;
        font-size: 20px;
    }

    h1
    {
        font-size: 55px;
    }


    }
    

    @media screen and (min-width:531px) and (max-width:650px)
    {

    h2
    {
        font-size: 20px;
        margin-top: -17.5%;
    }

    h1
    {
        font-size: 58px;
    }

    }

    
    @media screen and (min-width:651px) and (max-width:796px)
    {

    h2
    {
        font-size: 22px;
        margin-top: -15.5%;
    }

    h1
    {
        font-size: 60px;
    }

    }


    @media screen and (min-width:797px) and (max-width:1000px)
    {

    h2
    {
        font-size: 24px;
        margin-top: -13.5%;
    }

    h1
    {
        font-size: 62px;
    }

    }

    @media screen and (min-width:1001px) and (max-width:1200px)
    {

    h2
    {
        font-size: 24px;
        margin-top: -12%;
    }

    h1
    {
        font-size: 64px;
    }

    }



</style>