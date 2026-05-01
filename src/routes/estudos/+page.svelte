<script lang="ts">
	type StudyLink = {
		title: string;
		date?: string;
		href: string;
		description?: string;
	};

	const links: StudyLink[] = [
		{
			title: 'Encontro 01 — Introdução e motivação',
			date: '2026-05-01',
			href: '#',
			description: 'O que é Geometria da Informação? Por que métricas e divergências aparecem em estatística.'
		},
		{
			title: 'Encontro 02 — Divergências e conexões',
			date: '2026-05-08',
			href: '#',
			description: 'Família exponencial, KL, e interpretação geométrica.'
		},
		{
			title: 'Encontro 03 — Métrica de Fisher',
			date: '2026-05-15',
			href: '#',
			description: 'Definição, exemplos e intuição.'
		}
	];
</script>

<section class="section">
	<h1>Notas</h1>
	<p class="lead">
		Aqui ficam as notas  e o material discutido em cada encontro.
	</p>

	<ul class="list">
		{#each links as item (item.title)}
			<li>
				<a
					class="item"
					href={item.href}
					target={item.href.startsWith('http') ? '_blank' : undefined}
					rel={item.href.startsWith('http') ? 'noreferrer' : undefined}
				>
					<div class="row">
						<strong class="title">{item.title}</strong>
						{#if item.date}
							<span class="date">{item.date}</span>
						{/if}
					</div>
					{#if item.description}
						<p class="desc">{item.description}</p>
					{/if}
				</a>
			</li>
		{/each}
	</ul>

	<p class="hint">
		Dica: você pode trocar os <code>href: '#'</code> pelos links reais (PDF, Notion, Google Docs, GitHub, etc.).
	</p>
</section>

<style>
	.section h1 {
		margin: 0 0 10px;
		font-size: clamp(26px, 3.4vw, 36px);
		letter-spacing: -0.3px;
	}

	.lead {
		margin: 0 0 14px;
		color: var(--muted);
		line-height: 1.6;
		max-width: 75ch;
	}

	.list {
		list-style: none;
		padding: 0;
		margin: 0;
		display: grid;
		gap: 10px;
	}

	.list li {
		margin: 0;
		padding: 0;
	}

	.item {
		text-decoration: none;
		border: 1px solid var(--border);
		border-radius: 16px;
		background: rgba(255, 255, 255, 0.04);
		padding: 12px 12px 10px;
	}

	.item:hover {
		background: rgba(255, 255, 255, 0.06);
		border-color: rgba(255, 255, 255, 0.18);
	}

	.row {
		display: flex;
		align-items: baseline;
		justify-content: space-between;
		gap: 10px;
	}

	.title {
		font-weight: 700;
	}

	.date {
		color: var(--muted);
		font-size: 12px;
		white-space: nowrap;
	}

	.desc {
		margin: 8px 0 0;
		color: var(--muted);
		line-height: 1.55;
	}

	.hint {
		margin-top: 14px;
		color: var(--muted);
	}

	code {
		background: rgba(255, 255, 255, 0.08);
		border: 1px solid var(--border);
		padding: 1px 6px;
		border-radius: 8px;
	}
</style>
