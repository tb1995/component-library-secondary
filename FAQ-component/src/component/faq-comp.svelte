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

 
    .blockP
    {
        font-size: 22px;
        float:right;
        margin-top:5.5%;
        padding-right: 15px;
        color:blue;
    }

    @media screen and (max-width:555px)
    {
        .flex
        {
            display:flex;
            flex-direction:column;
        }

        .blockA
        {
            width: 100%;
        }

        .blockB
        {
            width:100%;
        }

        .blockP
        {
         font-size:20px;
         float:none;
         text-align:center ;
        }

        .faqBlock
        {
            width:350px;
            margin-left: auto;
            margin-right: auto;
        }
    }

    @media screen and (min-width:556px) and (max-width:650px)
    {
        

        .blockP
        {
         font-size:16px;
         padding-right: 0px;
        }

        .faqBlock
        {
            width:320px;
            margin-left: auto;
            margin-right: auto;
        }

        

    }

    @media screen and (min-width:651px) and (max-width:800px)
    {
        

        .blockP
        {
         font-size:17px;
        }

        .faqBlock
        {
            width:400px;
         
        }

        

    }

    @media screen and (min-width:801px) and (max-width:900px)
    {
        

        .blockP
        {
         font-size:18px;
        }

        .faqBlock
        {
            width:460px;
         
        }

        

    }

    @media screen and (min-width:901px) and (max-width:1000px)
    {
        

        .blockP
        {
         font-size:20px;
        }

        .faqBlock
        {
            width:540px;
         
        }

        

    }




</style>