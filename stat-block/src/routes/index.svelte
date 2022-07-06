<script>
    import StatBlock from '../components/stat-block.svelte';

    var Stats = [
        {
          'title' : 'Years of Excellence',
          'EndingNumber' : 110,
        },

        {
          'title' : 'Product SKUs',
          'EndingNumber' : 150,
        },

        {
          'title' : 'Team Members',
          'EndingNumber' : 300,
        } 

        
]

console.log("Stats title" , Stats[0].title);
console.log("Stats EndingNNumber" , Stats[0].EndingNumber);
</script>

<StatBlock {Stats} />
