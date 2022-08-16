<script>
	import Video from '$lib/components/Video.svelte';
</script>

<section id="home" class="viewport col fcenter">
	<Video />

	<img src="/logo.svg" alt="Veneno en la piel" class="logo" />

	<h1 class="title tcenter">
		El mejor pop <strong>español</strong>
		<br />
		de los <strong>80</strong> y <strong>90’s</strong>
	</h1>

	<div class="cta row acenter">
		<a href="#events" class="btn">PRÓXIMOS CONCIERTOS</a>
		<a href="/">CONTRATAR</a>
	</div>

	<a href="#events" class="scroller col"><span class="col" /></a>

	<div class="gradient row" />
</section>

<style lang="scss">
	section {
		background: #000;
		padding: 20px;

		* {
			z-index: 1;
		}
	}

	.logo {
		@media (max-width: 800px) {
			display: none;
		}
	}

	h1 {
		color: #fff;
		font-size: 4em;
		margin-top: 20px;

		@media (max-width: 800px) {
			font-size: 3em;

			br {
				display: none;
			}
		}
	}

	strong {
		font-weight: bold;
	}

	.btn {
		background: rgba(#fff, 0.1);
		backdrop-filter: blur(10px);
		color: #fff;
		font-family: var(--font-text);
		font-size: 12px;
		margin-top: 20px;
		padding: 16px 32px;
	}

	a {
		color: #fff;
		font-family: var(--font-text);
		font-size: 12px;
		margin-top: 20px;
		padding: 16px 32px;
	}

	.scroller {
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
		width: 2px;
		margin: 0 auto;
		animation: bounce 1500ms infinite;
		padding: 30px;

		span {
			width: 2px;
			height: 80px;
			background: #fff;
		}
	}

	.gradient {
		position: absolute;
		bottom: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: linear-gradient(to top, #000 10%, rgba(0, 0, 0, 0) 100%);
		z-index: 0;
	}

	@keyframes bounce {
		0%,
		50%,
		100% {
			transform: translateY(0);
		}
		10% {
			transform: translateY(-5px);
		}
		15% {
			transform: translateY(10px);
		}
	}
</style>
