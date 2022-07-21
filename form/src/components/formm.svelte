<script>

</script>

<form action="">
    <label>Send us a message</label>
    <input type="text" placeholder="Name"/>
    <input type="email" placeholder="Email"/>
    <input type="tel" placeholder="Phone"/>
    <textarea cols="30" rows="5" placeholder="Message"></textarea>
    <button>Send</button>
</form>



<style>
    form
    {
        width:70%;
        float:right;
        display:flex;
        flex-direction: column;
        margin-top: 10%;
        margin-bottom: 24.5%;
        background-color:aliceblue;
    }

    input
    {
        width:390px;
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
        width:392px;
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
        width:397px;
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
</style>