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
		--bg: #0b1020;
		--panel: rgba(255, 255, 255, 0.06);
		--text: rgba(255, 255, 255, 0.92);
		--muted: rgba(255, 255, 255, 0.68);
		--border: rgba(255, 255, 255, 0.12);
		--accent: #7c3aed;
		--accent2: #22c55e;
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
		background:
			radial-gradient(1200px 800px at 10% 10%, rgba(124, 58, 237, 0.35), transparent 60%),
			radial-gradient(1000px 700px at 90% 30%, rgba(34, 197, 94, 0.25), transparent 55%),
			var(--bg);
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
		backdrop-filter: blur(12px);
		background: rgba(11, 16, 32, 0.72);
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
		letter-spacing: 0.2px;
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
		color: var(--text);
		border-color: var(--border);
		background: var(--panel);
	}

	.main {
		width: min(980px, calc(100% - 36px));
		margin: 0 auto;
		padding: 28px 0 32px;
	}

	.footer {
		border-top: 1px solid var(--border);
		padding: 18px;
		color: var(--muted);
		text-align: center;
	}
</style>
