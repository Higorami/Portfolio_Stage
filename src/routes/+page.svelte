<svelte:head>
	<title>Accueil</title>
	<meta name="description" content="Portfolio de stage Fyléas QUAILE" />
</svelte:head>

<section>
	<h1>
		<span class="welcome">
			<span>
				<h1>Portfolio</h1>
				<h2 style="color: rgb(97, 97, 97);">de stage</h2>
			</span>
			<h1 style="color: rgb(255, 72, 0);">Fyléas QUAILE</h1>
		</span>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
		font-size: 2em;
		color: black;
	}

	h2{
		font-size: 1em;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}
</style>
