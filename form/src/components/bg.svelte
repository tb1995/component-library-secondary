<script>
    import Form from '../components/formm.svelte';
    import Other from '../components/other.svelte';

</script>

<div class="bg">
    <div class="flex">
      <div class="A">  
        <slot name="A">
            <Form />
        </slot>
      </div>
      <div class="B">
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

    .A
    {
        width:50%;
        height:100%;
    }

    .B
    {
        width:50%;
        height:100%;
    }
</style>