<script>
    export let question;
    export let answer;
    let display = false;
</script>

             <p class="faqQues" on:click={ () => display = !display }>{question}</p>
              <div class={ display ? 'faqAns2' : 'faqAns'}>
                <p>{answer}</p>
              </div>

<style>
    .faqQues 
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
        padding-right: 25px;
        text-align: justify;
        display:block;
        font-weight: lighter;
        padding-top: 2px;
    }


    @media screen and (max-width:555px)
    {
        .faqQues, .faqAns2
        {
            font-size: 12px;
        }

        
    }

    @media screen and (min-width:556px) and (max-width:650px)
    {
        .faqQues, .faqAns2
        {
            font-size: 12px;
        }

        
    }

    @media screen and (min-width:651px) and (max-width:800px)
    {
        .faqQues, .faqAns2
        {
            font-size: 13px;
        }

        
    }

 

</style>