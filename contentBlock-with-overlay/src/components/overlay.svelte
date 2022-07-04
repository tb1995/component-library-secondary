<script>
    import '../styles/global.css';
    export let heading3;
    export let heading1;
    export let text;
    export let button;

</script>

<div class="flex">
<div class="A">

</div>
<div class="B">
   <div class="positioning">
     <h3>{heading3}</h3>
     <h1>{heading1}</h1>
     <p>{text}</p>
     <button>{button}</button>
   </div>
</div>
</div>

<style>
    .A
    {
        width:50%;
        height:100%;
    }

    .B
    {
        width:50%;
        background-color:rgba(33, 102, 151, 0.81);
        position: absolute;
        top:0%;
        bottom:0%;
        right:0%;
        height:100%;
    }

    .positioning
    {
        position: absolute;
        top:11%;
        left:9%;
        color:white;
    }

    h3
    {
        font-weight:bold;
        font-size: 28px;
    }

    h1
    {
        font-size: 66px;
        font-weight: lighter;
        width:80%;
        margin-top: -2%;
      
    }

    p
    {
        font-size: 36px;
        margin-top: -5%;
        font-weight: lighter;
    }

    button
    {
        background-color: transparent;
        width:340px;
        font-size: 26px;
        padding-top: 35px;
        padding-bottom: 35px;
        border:white 5px solid;
        color:white;
        margin-top: 3%;
        font-weight: lighter;
    }

    .flex
    {
        display:flex;
    }

</style>