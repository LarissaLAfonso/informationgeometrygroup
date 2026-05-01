<script lang="ts">
	type StudyLink = {
		title: string;
		date?: string;
		href: string;
		description?: string;
	};

	const links: StudyLink[] = [
		{
			title: 'Encontro 01: Conexões Duais',
			date: '2026-03-19',
			href: '#',
			description: 'Seções 6.1 a 6.3 do Information Geometry and Its Applications'
		},
		{
			title: 'Encontro 02: Variedades Dualmente Planas',
			date: '2026-04-02',
			href: '#',
			description: 'Seções 6.4 a 6.6 do Information Geometry and Its Applications'
		},
		{
			title: 'Encontro 03: Clusterização',
			date: '2026-04-17',
			href: '#',
			description: 'Seção 11.1 do Information Geometry and Its Applications'
		},
		{
			title: 'Encontro 04: SVMs',
			date: '2026-04-17',
			href: '#',
			description: 'Seção 11.2 do Information Geometry and Its Applications'
		}
	];
</script>

<section class="section">
	<h1>Notas</h1>
	<p class="lead">
		Aqui ficam as notas e as referências dos textos discutidos em cada encontro.
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
		border-radius: 14px;
		background: var(--panel);
		box-shadow: var(--shadow);
		padding: 16px 16px 14px;

		display: flex;
		flex-direction: column;
		justify-content: center;

		transition:
			background 0.15s ease,
			transform 0.15s ease;
	}

	.item:hover {
		background: var(--accent-soft);
		transform: translateY(-1px);
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

	.section h1,
	.title {
		font-family: Georgia, 'Times New Roman', Times, serif;
	}

	.desc,
	.lead,
	.hint,
	.date {
		font-family: Georgia, 'Times New Roman', Times, serif;
	}
</style>
