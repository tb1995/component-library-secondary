<script>

  
        
</script>

<form action="">
    <label>Send us a message</label>
    <input type="text" placeholder="First Name"/>
    <input type="text" placeholder="Last Name"/>
    <input type="email" placeholder="Email"/>
    <input type="tel" placeholder="Phone"/>
    <textarea cols="30" rows="5" placeholder="Message"></textarea>
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
        margin-bottom: 24.5%;
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
        color:darkslategray;
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
        color:darkslategray;
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