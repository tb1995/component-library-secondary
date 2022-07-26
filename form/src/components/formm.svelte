<script>

     let Fname = '';
     let Lname = '';
     let email ='';
     let phone = '';
     let text = '';


     function input()
     {
        if (Fname.length >= 1 || Lname.length >= 1 || email.length >= 1
           || phone.length >= 1 || text.length >= 1)
        {
            showFNMessage = false;
            showLNMessage  = false;
            showEmailMsg = false;
            showPhoneMsg = false;
            showText = false;
          
        } 
        /*

        for (var i=0; i < Fname.length; i++)
        {
            if ( ( Fname.charCodeAt(i) <= 65 && Fname.charCodeAt(i) >= 90)   ||
                 ( Fname.charCodeAt(i) <= 97 && Fname.charCodeAt(i) >= 122)   )
            {
                 document.getElementById('fn').style.display = 'block';
            }

            else
            {
                 document.getElementById('fn').style.display= 'none';
            }
        
        } 
     */
     }

     let showFNMessage = false;
     let showLNMessage = false;
     let showEmailMsg = false;
     let showPhoneMsg = false;
     let showText = false;
     let validatePh;
     let empty;

     function FNmessage()
     {
       showFNMessage = !showFNMessage;
     }

     function LNmessage()
     {
       showLNMessage = !showLNMessage;
     }

     function EmailMessage()
     {
        showEmailMsg = !showEmailMsg;
     }

     function PhoneMessage()
     {
        showPhoneMsg = !showPhoneMsg;
     }

     function Text()
     {
        showText = !showText;
     }


     var phoneResult;
     function validate()
     {
        var phoneRGEX = /^(\([0-9]{3}\) |[0-9]{3}-)[0-9]{3}-[0-9]{4}/;
        phoneResult = phoneRGEX.test(phone);
        console.log("phone:"+phoneResult );
        console.log("phone value" , phone);

        
        if (phoneResult && phone.length == 12)
        {
            validatePh = true;

        }

        if (phone.length > 12 || phone.length < 12)
        {
            validatePh =false;
        }

     /*    if ( !phoneResult && (phone.length > 12) )  
        {
            validatePh = false;
        }

         */
     }

        
</script>


<form action="">
    <label>Send us a message</label>
    <input type="text"
           placeholder="First Name" 
           bind:value={Fname} 
           on:keyup={FNmessage} 
           on:input={input}  required/>
    
    {#if showFNMessage}
    <p class="normalText">Please enter your First Name</p>
    {:else if !showFNMessage}
    <p class="Errormessage {Fname.length > 1 && Fname.length < 4 ? 'block' : 'none'}">First Name should contain  atleast 3 characters or more</p>
    <p class="Errormessage {Fname.length > 9? 'block' : 'none'} ">First Name should not contain more than 9 characters</p>  
    {/if}
    
   
                  <!-- xxxxxxxxxxxxxxxxxx -->


    <input type="text" 
           placeholder="Last Name" 
           bind:value={Lname} 
           on:focus="{LNmessage}" 
           on:input={input} required>

    {#if showLNMessage}
    <p  class="normalText">Please enter your Last Name</p>
    {:else if !showLNMessage}
    <p class="Errormessage {Lname.length > 1 && Lname.length < 3 ? 'block' : 'none'}">Last Name should contain  atleast 3 characters or more</p>
    <p class="Errormessage {Lname.length > 10 ? 'block' : 'none'}">Last Name should not contain more than 10 characters</p>  
    {/if} 


                  <!--  xxxxxxxxxxxxxxxxxxxx -->


    <input type="email" 
           placeholder="Email" 
           bind:value={email} 
           on:focus="{EmailMessage}" 
           on:input={input} required/>

    {#if showEmailMsg}
    <p  class="normalText">Please enter your Email address</p>
    {/if} 
                    <!--xxxxxxxxxxxxxxxxxxxx -->
    
    
    <input type="tel" 
           placeholder="xxx-xxx-xxxx" 
           bind:value={phone} 
           on:focus="{PhoneMessage}" 
           on:input="{validate}"
           on:input="{input}" required/>

    {#if showPhoneMsg}
    <p  class="normalText">Please enter your phone no.</p>
    {/if}
    <p class="message { validatePh ? 'block' : 'none'}">phone no. is valid</p>
 <!--    <p class="message { !validatePh ? 'block' : 'none'}">invalid phone no.</p>
 -->
 
                     <!--  xxxxxxxxxxxxxxxxxxxx -->

    
    <textarea cols="30"
              rows="5"
              placeholder="Message" 
              bind:value={text}
              on:focus="{Text}" 
              on:input="{input}"></textarea>

    {#if showText}
    <p  class="normalText">Please enter the message</p>
    {/if}
    

    <button>Send</button>
</form>



<style>
    form
    {
        width:67%;
        float:right;
        display:flex;
        flex-direction: column;
        margin-top: 12%;
        background-color:aliceblue;
    }

    input
    {
        width:85%;
        height:32px;
        margin-top: 17px;
        margin-left: auto;
        margin-right: auto;
        background-color: white;
        border: 0px;
    }

    input::placeholder
    {
        font-size: 12px;
        padding-left: 5px;
        color:gray;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    }

  
    textarea
    {
        width:87%;
        margin-top: 20px;
        margin-left: auto;
        margin-right: auto;
        border: 0px;
    }

    textarea::placeholder
    {
        font-size: 12px;
        padding-left: 8px;
        color:gray;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    }

    button
    {
        width:89%;
        margin-top: 20px;
        margin-left: auto;
        margin-right: auto;
        height: 30px;
        margin-bottom: 8%;
        border: 0px;
        color:white;
        font-weight: bold;
        background-color:steelblue;
    }

    label
    {
        font-size: 26px;
        text-indent: 40px;
        font-weight: bold;
        margin-top: 8%;
    }


    .message
    {
        font-size: 12px;
        color:green;
        margin-bottom: 0px;
        text-indent: 33px;
       
    }

    .Errormessage
    {
        font-size: 12px;
        color:red;
        margin-bottom: 0px;
        text-indent: 33px;
       
    }

    .normalText
    {
        font-size: 12px;
        color:black;
        margin-bottom: 0px;
        text-indent: 33px;
    }

    .block
    {
        display: block;
    }

    .none
    {
        display: none;
    }

    
    @media screen and (min-width:350px) and (max-width:460px)
    {
        form
        {
            float:none;
            margin-left: auto;
            margin-right: auto;
            margin-bottom: 10%;
            margin-top: 9%;
            width: 75%;
        }

        input
        {
            height:28px;
            margin-top: 13px;
        }

        label
        {
        font-size: 18px;
        text-indent: 26px;
        font-weight: bold;
        margin-top: 8%;
        }


        input::placeholder
        {
            font-size: 10px;
        }

        textarea
        {
            margin-top: 16px;
            height:44px;
        }

        textarea::placeholder
        {
            font-size: 10px;
        }

        button
        {
            font-size:11px;
        }
   }

   @media screen and (min-width:461px) and (max-width:600px)
    {

        form
        {
            float:none;
            margin-left: auto;
            margin-right: auto;
            margin-bottom: 6%;
            margin-top: 5%;
            width: 65%;
        }

        input
        {
            height:28px;
            margin-top: 13px;
        }

        label
        {
            font-size: 20px;
            text-indent: 28px;
            font-weight: bold;
            margin-top: 8%;
        }


        input::placeholder
        {
            font-size: 12px;
        }

        textarea
        {
            margin-top: 16px;
            height:46px;
        }

        textarea::placeholder
        {
            font-size: 12px;
        }

        button
        {
            font-size:13px;
        }
    
    }


    @media screen and (min-width:601px) and (max-width:800px)
    {

        form
        {
            width:92.5%;
            margin-top: 14%;

        }

        label
        {
            font-size: 20px;
            text-indent: 24px;

        }

        input
        {
            margin-top: 13px;
        }

        input::placeholder
        {
            font-size: 11px;
        }

        textarea::placeholder
        {
            font-size: 11px;
        }

        button
        {
            font-size: 13px;
        }


    }


    
    @media screen and (min-width:801px) and (max-width:1000px)
    {

        form
        {
            width:80%;
            margin-top: 14%;

        }

        label
        {
            font-size: 22px;
            text-indent: 28px;

        }

        input
        {
            margin-top: 15px;
        }

        input::placeholder
        {
            font-size: 12px;
        }

        textarea::placeholder
        {
            font-size: 12px;
        }

        button
        {
            font-size: 14px;
        }


    }

    @media screen and (min-width:1001px) and (max-width:1150px)
    {
        label
        {
            font-size: 23px;
            text-indent: 30px;

        }

        form
        {
            margin-top: 14%;
            width:80%;
        }

        button
        {
            font-size: 15px;
        }


    }
    
    
</style>