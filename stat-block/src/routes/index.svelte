<script>
    import StatBlock from '../components/stat-block.svelte';

    let y;

    var Stats = [
        {
          'title' : 'Years of Excellence',
          'startingNumber' : 0,
          'endingNumber' : 110

        },

        {
          'title' : 'Product SKUs',
          'startingNumber' : 0,
          'endingNumber' :150
        },

        {
          'title' : 'Team Members',
          'startingNumber' : 0,
          'endingNumber' : 130
        } 

        
]



</script>
 
<svelte:window bind:scrollY={y} />

 <div class={ y > 500 ? 'div' : 'div2'}>


 </div>

<StatBlock {Stats} />




<style>
  div
  {
    height:150vh;
    background-color: darkolivegreen;
  }

  .div2
  {
    background-color: khaki;
  }
</style>
