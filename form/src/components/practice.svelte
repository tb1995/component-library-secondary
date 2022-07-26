<script>
    let name = ''
</script>

<label for="name">
    Enter your name
    <input type="text" bind:value={name}>
</label>

<h2>hello {name} !</h2>