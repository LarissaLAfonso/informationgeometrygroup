<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import { base } from '$app/paths';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<meta name="viewport" content="width=device-width, initial-scale=1" />
	<meta name="description" content="Grupo de estudos em Geometria da Informação." />
</svelte:head>

<div class="app">
	<header class="top">
		<div class="brand">
			<a class="title" href={base + '/'}>Grupo de Estudos</a>
		</div>
		<nav class="nav">
			<a class="link" href={base + '/'}>Início</a>
			<a class="link" href={base + '/sobre-nos'}>Sobre nós</a>
			<a class="link" href={base + '/estudos'}>Estudos</a>
		</nav>
	</header>

	<main class="main">
		{@render children()}
	</main>

	<footer class="footer">
		<small>© {new Date().getFullYear()} • Grupo de Estudos</small>
	</footer>
</div>

<style>
	:global(:root) {
		color-scheme: light;
		--bg: #f6f7f9;
		--panel: #ffffff;
		--text: #111827;
		--muted: #4b5563;
		--border: #e5e7eb;
		--accent: #002147; /* Oxford-like blue */
		--accent-soft: #e6edf5;
		--shadow: 0 10px 24px rgba(17, 24, 39, 0.08);
	}

	:global(body) {
		margin: 0;
		font-family:
			ui-sans-serif,
			system-ui,
			-apple-system,
			Segoe UI,
			Roboto,
			Helvetica,
			Arial,
			'Apple Color Emoji',
			'Segoe UI Emoji';
		background: var(--bg);
		color: var(--text);
	}

	:global(a) {
		color: inherit;
	}

	.app {
		min-height: 100dvh;
		display: grid;
		grid-template-rows: auto 1fr auto;
	}

	.top {
		position: sticky;
		top: 0;
		z-index: 10;
		background: rgba(255, 255, 255, 0.92);
		backdrop-filter: blur(10px);
		border-bottom: 1px solid var(--border);
		padding: 14px 18px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 16px;
	}

	.title {
		text-decoration: none;
		font-weight: 750;
		letter-spacing: -0.2px;
	}

	.nav {
		display: flex;
		gap: 10px;
		flex-wrap: wrap;
	}

	.link {
		text-decoration: none;
		padding: 8px 10px;
		border-radius: 10px;
		border: 1px solid transparent;
		color: var(--muted);
	}

	.link:hover {
		color: var(--accent);
		border-color: var(--border);
		background: var(--accent-soft);
	}

	.main {
		width: min(980px, calc(100% - 36px));
		margin: 0 auto;
		padding: 28px 0 40px;
	}

	.footer {
		border-top: 1px solid var(--border);
		padding: 18px;
		color: var(--muted);
		text-align: center;
		background: var(--panel);
	}
</style>
