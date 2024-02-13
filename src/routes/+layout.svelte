<script>
</script>

<header class="header">
	<div class="header__logo">
		<h1 class="header__h1">TARIFICADOR</h1>
	</div>
</header>
<slot />

<footer class="footer">
	<div class="footer__div">
		<p class="footer__p">Todos los derechos reservador - 2024 - Tarficador</p>
        <a class="footer__a" href="http://rubenterre.com">Rubén Terré</a>
	</div>
</footer>

<style>
	:root {
		--color-principal: #66a9b9;
		--color-secundario: #172f58;
		--color-terciario: #d9ecf0;
		--fuente-principal: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
			Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
	}

	:global(*) {
		margin: 0;
		padding: 0;
		outline: 0;
		box-sizing: border-box;
	}

	:global(body) {
		background: white;
		color: var(--color-secundario);
		-webkit-font-smoothing: antialiased;
	}

	:global(body, input, button) {
		font-size: 100%;
		font-family: var(--fuente-principal);
	}

	:global(button) {
		cursor: pointer;
	}

	/* Header */

	.header {
		background: #172f58;
		width: 100%;
		height: 80px;
	}

	.header__logo {
		padding: 30px 0px;
	}

	.header__h1 {
		font-family: var(--fuente-principal);
		color: white;
		font-size: 1rem;
		text-align: center;
	}

	/* Footer */

	.footer {
		position: fixed;
		bottom: 0px;
        left: 50%;
        transform: translate(-50%,-50%);
	}

	.footer__div {
		text-align: center;
		font-family: var(--fuente-principal);
		font-size: 0.8rem;
	}

    .footer__a{
        text-decoration: none;
    }
</style>
