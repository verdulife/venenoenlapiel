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

	<footer class="col xfill">
		<p class="time">{formatedDate}</p>
		<h3>{place}</h3>
		<p>{city}</p>
	</footer>
</article>

<style lang="scss">
	article {
		position: relative;
		width: 260px;
		height: 500px;
		background: #fffce5;
		border-radius: 1em;
		padding: 15px;

		&:before {
			content: '';
			position: absolute;
			left: -10px;
			bottom: 102px;
			width: 15px;
			height: 15px;
			background: #000;
			border-radius: 50%;

			@media (max-width: 800px) {
				bottom: 92px;
			}
		}

		&:after {
			content: '';
			position: absolute;
			right: -10px;
			bottom: 102px;
			width: 15px;
			height: 15px;
			background: #000;
			border-radius: 50%;

			@media (max-width: 800px) {
				bottom: 92px;
			}
		}

		@media (max-width: 800px) {
			width: 220px;
			height: 400px;
			padding: 10px;
		}
	}

	img {
		width: 230px;
		height: 350px;
		border-radius: 0.5em;

		@media (max-width: 800px) {
			width: 200px;
			height: 265px;
		}
	}

	footer {
		width: calc(100% + 20px);
		margin-left: -10px;
		border-top: 2px dashed #000;
		margin-top: 25px;
		padding: 20px 15px 0 15px;

		@media (max-width: 800px) {
			padding: 20px 10px 0 10px;
		}
	}

	p {
		font-family: var(--font-text);
	}

	.time {
		font-size: 12px;
		text-transform: uppercase;
	}

	h3 {
		font-family: var(--font-title);
		font-size: 24px;
	}
</style>
