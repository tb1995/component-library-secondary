<script>

    import '../styles/global.css';
    //vanila js
    /* window.onmousemove(e) = function()
    {
        console.log(e.pageY);
    } */
    
  let y;
  function OnMouseMove(e)
  {
    y = e.pageY;
    console.log(y);
  }
 
    
</script>
<svelte:window on:mousemove={OnMouseMove}/>

<nav>
<ul>
    <li>
        <a href="#">Home</a>
    </li>

    <li>
        <a href="">About</a>
    </li>

    <li>
        <a class="logo"><img src="http://i.imgur.com/WwCbbpG.jpg" alt="luxor"></a>
    </li>

    <li>
        <a href="">Contact</a>
    </li>

    <li>
        <a href="">Gallery</a>
    </li>
</ul>
</nav>
<p>you have scrolled {y} pixels</p>

{#if y > 85}
console.log('sdf');
{/if}


<style>
    nav
    {
        background-color:cornflowerblue;
        width: 100%;
        position:sticky;
        height:10vh;
        
    }

    nav ul
    {
        
        list-style-type: none;
        height:10vh;
        margin-top: 0px;
        text-align: center;
      
    } 

    nav ul li
    {
        display: inline-block;
        height:6vh;
        width:115px;
    }

    nav ul li a
    {
       text-decoration:none;
       color:black;
       font-size: 18px;
    }

    .logo img {
    margin-top:0px;
    display: block;
    width:100px;
    height:10vh;
    object-fit:cover;
    margin-left: auto;
    margin-right: auto;
    }
</style>