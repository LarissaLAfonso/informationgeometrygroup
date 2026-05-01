<script lang="ts">
	import { base } from '$app/paths';
</script>

<section class="hero">
	<h1>Grupo de Estudos em Geometria da Informação</h1>
	<p>
		Um espaço aberto para ler, discutir e construir intuição sobre geometria diferencial aplicada a probabilidade,
		informação e estatística — com encontros periódicos, notas de aula e referências comentadas.
	</p>

	<div class="cta">
		<a class="primary" href={base + '/estudos'}>Ver estudos</a>
		<a class="secondary" href={base + '/sobre-nos'}>Conhecer o grupo</a>
	</div>
</section>

<section class="cards">
	<article class="card">
		<h2>Como funciona</h2>
		<p>Em cada encontro escolhemos um tópico, fazemos uma leitura guiada e registramos um resumo com referências.</p>
	</article>
	<article class="card">
		<h2>Para quem é</h2>
		<p>Para pessoas curiosas — estudantes, pesquisadores e profissionais — com vontade de estudar em grupo.</p>
	</article>
	<article class="card">
		<h2>Materiais</h2>
		<p>As notas de aula e links ficam organizados na página “Estudos”.</p>
	</article>
</section>

<style>
	.hero {
		padding: 22px 18px;
		border: 1px solid var(--border);
		border-radius: 18px;
		background: linear-gradient(180deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.03));
	}

	h1 {
		margin: 0 0 10px;
		font-size: clamp(28px, 4vw, 44px);
		line-height: 1.05;
		letter-spacing: -0.4px;
	}

	p {
		margin: 0;
		color: var(--muted);
		font-size: 16px;
		line-height: 1.6;
		max-width: 70ch;
	}

	.cta {
		margin-top: 16px;
		display: flex;
		gap: 10px;
		flex-wrap: wrap;
	}

	.primary,
	.secondary {
		text-decoration: none;
		padding: 10px 12px;
		border-radius: 12px;
		border: 1px solid var(--border);
		font-weight: 650;
	}

	.primary {
		background: rgba(124, 58, 237, 0.22);
		border-color: rgba(124, 58, 237, 0.55);
	}

	.primary:hover {
		background: rgba(124, 58, 237, 0.28);
	}

	.secondary {
		color: var(--muted);
		background: rgba(255, 255, 255, 0.04);
	}

	.secondary:hover {
		color: var(--text);
		background: rgba(255, 255, 255, 0.06);
	}

	.cards {
		margin-top: 18px;
		display: grid;
		grid-template-columns: repeat(3, minmax(0, 1fr));
		gap: 12px;
	}

	.card {
		border: 1px solid var(--border);
		border-radius: 16px;
		background: rgba(255, 255, 255, 0.04);
		padding: 14px 14px 12px;
	}

	.card h2 {
		margin: 0 0 6px;
		font-size: 16px;
	}

	.card p {
		font-size: 14px;
	}

	@media (max-width: 860px) {
		.cards {
			grid-template-columns: 1fr;
		}
	}
</style>
