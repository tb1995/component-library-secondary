<script>
import '../styles/global.css';
  export /**
* @type {{ questionList: any; }}
*/
   let array;
  console.log("array is" , array);
</script>

<div class="section">

    <h1>FAQs</h1>
    <div class="block">

    </div>

    <div class="faqBlock">
        {#each array as arrayItem}
           {#each arrayItem.questionList as ques}
        <hr>
        <div class="faqText">
           <p>{ques.question}</p>
        </div>
        <!-- <div class="faqBody">
            <p>In publishing and graphic design, Lorem ipsum is a placeholder text commonly used to demonstrate the visual form of a document or a typeface without relying on meaningful content. Lorem ipsum may be used as a placeholder before final copy is available.</p>
        </div> -->
        {/each}
        {/each}
        <hr/>
    </div>
</div>

<style>

   .section
   {
    display:flex;
    flex-direction: column;
   }

   .faqBlock
   {
    width:600px;
    margin-left:auto;
    margin-right: auto;
    margin-top: 3%;
   }

   h1
   {
    text-align: center;
    margin-top: 0%;
   }

   p
   {
    font-size: 15px;
    text-indent: 20px;
    padding-top: 5px;
    padding-bottom:5px ;
   }



</style>