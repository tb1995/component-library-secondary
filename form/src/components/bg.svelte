<script>
    import Form from '../components/formm.svelte';
    import Other from '../components/other.svelte';

</script>

<div class="bg">
    <div class="flex">
      <div class="formBlock">  
        <slot name="A">
            <Form />
        </slot>
      </div>
      <div class="dummyBlock">
        <slot name="B">
            <Other />
         </slot>

      </div>
    </div>
</div>

<style>
    .bg
    {
        background-image: url('../../bg.jpg');
        position: absolute;
        top:0%;
        left: 0%;
        right: 0%;
        height: 100%;
        background-size: cover;
        z-index: -2;
    }

  

    .flex
    {
        display:flex;
        font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    }

    .formBlock
    {
        width:50%;
        height:100%;
    }

    .dummyBlock
    {
        width:50%;
        height:100%;
    }

    @media screen and (min-width:350px) and (max-width:600px)
    {

    .formBlock , .dummyBlock
    {
        width:100%;
    
    }

    .flex
    {
        display:flex;
        flex-direction: column;
    }

    }


       
</style>