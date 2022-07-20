<script>
    import Ques from '../component/question.svelte';
    export let array;
    console.log("array iss" , array);
    //let display = false;
</script>

<div class="section">
    <h1>FAQS</h1>
    <div class="flex">

        <div class="blockA">
           <p class="blockP">
              Most Common Questions
           </p>
        </div>

        <div class="blockB">
        <div class="faqBlock">
            {#each array as arrayItem}
              {#each arrayItem.questionList as ques}
              <hr>
              <Ques question={ques.question} answer={ques.answer}/>
              {/each}
              {/each}
              <hr>
        </div>
        </div>

    </div>
</div>

<style>
  
    .flex
    {
        display:flex;
    }

    .blockA
    {
        width:35%;
        margin-top: 3%;
    }

    .blockB
    {
        width:65%;
        margin-top: 3%;
    }

    .faqBlock
    {
        width:600px;
    }

    .section
    {
        margin:0;
        padding:0;
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    }

    h1
    {
        text-align: center;
        margin-top: 0%;
        font-size:40px;
    }

    /* .faqQues 
    {
        font-size: 14px;
        padding-left: 25px;
        display: flex;
        cursor: pointer;
    }

    .faqQues:after 
    {
        margin-left: auto;
        content: "❯";
        width: 1em;
        height: 1em;
        transition: all 0.35s;
        color:black;
        text-align: center;
        margin-right: 5px;
        cursor: pointer;
        font-weight: bold;
    }
 
 

    .faqAns
    {
        font-size: 14px;
        padding-left: 25px;
        padding-bottom:0px ;
        padding-right: 15px;
        text-align: justify;
        display:none;
      
    }

    .faqAns2
    {
        font-size: 14px;
        padding-left: 25px;
        padding-bottom:0px ;
        padding-right: 25px;
        text-align: justify;
        display:block;
        font-weight: lighter;
        padding-bottom:2px;

    }
 */
    .blockP
    {
        font-size: 22px;
        float:right;
        margin-top:5.5%;
        padding-right: 15px;
        color:blue;
    }



</style>