<script>

let blocks = [
    {
        "type": "h1",
        "data": {
            "text": "blabla"
        }
    },
    {
        "type": "h2",
        "data": {
            "text": "subtitulo....blabla"
        }
    },
    {
        "type": "p",
        "data": {
            "text": "Duis tempor do dolore velit."
        }
    },
    {
        "type": "p",
        "data": {
            "text": "Duis tempor do dolore velit."
        }
    },
    {
        "type": "img",
        "data": {
            "src": "http://fakeimg.pl/300x200",
            "alt": "img placeholder",
        }
    },
    {
        "type": "dl",
        "data": {
            "items": [
				{
					"dt": "termino1",
					"dd": "Proident magna aute ad ipsum cillum commodo aliquip voluptate incididunt.",
				},
				{
					"dt": "termino2",
					"dd": "Consequat aliqua ullamco pariatur aliquip commodo exercitation et ex veniam consectetur.",
				}
			]
        }
    }
]

</script>


<style>

	dl {
		display: grid;
		grid-template-columns: 1fr 1fr;
	}

</style>


{#each blocks as block, i (i) }


	{#if block.type == "h1" }
		<h1>
			{block.data.text}
		</h1>
	{/if}
	{#if block.type == "h2" }
		<h2>
			{block.data.text}
		</h2>
	{/if}
	{#if block.type == "p" }
		<p>
			{block.data.text}
		</p>
	{/if}
	{#if block.type == "img" }
		<img src={block.data.src} alt={block.data.alt}/>
	{/if}
	{#if block.type == "dl" }
		<dl>
		{#each block.data.items as item, j (j)}
			<dt>
				{item.dt}
			</dt>	
			<dt>
				{item.dd}
			</dt>	
		{/each}
		</dl>
	{/if}

{/each}