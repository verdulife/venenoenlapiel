<script>
	import Player from '$lib/components/Player.svelte';
</script>

<nav class="row jbetween acenter xfill">
	<a href="/" class="logo">
		<img class="fill contain" src="/logo.svg" alt="Veneno en la piel" />
	</a>

	<ul class="row acenter">
		<li>
			<a href="/">LA BANDA</a>
		</li>
		<li>
			<a href="/">GALERIA</a>
		</li>
		<li>
			<a href="/">CONCIERTOS</a>
		</li>
		<li>
			<a class="btn" href="/">CONTACTO</a>
		</li>
	</ul>
</nav>

<footer class="row jbetween aend xfill">
	<a href="/" class="social row fcenter">
		Síguenos en <img src="/facebook.svg" alt="Facebook" />
	</a>

	<Player />
</footer>

<style lang="scss">
	nav {
		position: fixed;
		top: 0;
		left: 0;
		padding: 30px 60px;
		z-index: 9;
		pointer-events: none;

		* {
			pointer-events: all;
		}

		@media (max-width: 800px) {
			padding: 20px;
		}
	}

	.logo {
		width: 150px;

		@media (max-width: 800px) {
			margin: 0 auto;
		}
	}

	ul {
		gap: 60px;

		@media (max-width: 800px) {
			display: none;
		}
	}

	a {
		color: #fff;
		font-family: var(--font-text);
		font-size: 12px;
	}

	.btn {
		background: rgba(255, 255, 255, 0.1);
		backdrop-filter: blur(10px);
		font-family: var(--font-text);
		color: #fff;
		font-size: 12px;
		padding: 16px 32px;
	}

	footer {
		position: fixed;
		bottom: 0;
		left: 0;
		padding: 30px 60px;
		z-index: 9;
		pointer-events: none;

		* {
			pointer-events: all;
		}

		@media (max-width: 800px) {
			padding: 20px;
		}
	}

	.social {
		gap: 10px;
	}
</style>
