<script>
	export let data;
	const { image, date, place, city } = data;

	const options = {
		month: 'long',
		day: 'numeric',
		hour: 'numeric',
		minute: 'numeric'
	};
	const formatedDate = new Intl.DateTimeFormat('es-ES', options).format(new Date(date));
</script>

<article class="col">
	<img class="cover" src={image} alt={place} />
	<p class="time">{formatedDate}</p>
	<h3>{place}</h3>
	<p>{city}</p>
</article>

<style lang="scss">
	article {
		width: 260px;
		height: 350px;
		background: #fffce5;
		border-radius: 1em;
		padding: 15px;
	}

	img {
		width: 230px;
		height: 220px;
		border-radius: 0.5em;
	}

	p {
		font-family: var(--font-text);
	}

	.time {
		font-size: 12px;
		text-transform: uppercase;
		margin-top: 20px;
	}

	h3 {
		font-family: var(--font-title);
		font-size: 30px;
	}
</style>
