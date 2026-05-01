<script lang="ts">
	import { base } from '$app/paths';
</script>

<section class="hero">
	<h1>Grupo de Estudos de Geometria da Informação</h1>
	<p>
		Um grupo de estudos aberto a todos aqueles interessados em entender melhor temas relacionados à geometria informação, campo que trata da interseção de probabilidade e estatística.
	</p>
	<p>
		Uma vez a cada duas semanas, nos reunimos para ler textos dos mais variados: capítulos de livros ou artigos, recentes ou antigos, mas todos com alguma ideia interessante para os participantes, atualmente todos da área de machine learning probabilístico.
	</p>

	<div class="cta">
		<a class="primary" href={base + '/estudos'}>Estudos</a>
		<a class="secondary" href={base + '/sobre-nos'}>Sobre nós</a>
	</div>
</section>

<section class="cards">
	<article class="card">
		<h2>Como funciona</h2>
		<p>A cada duas semanas, é escolhido um texto para discurtirmos. Os encontros são realizados online em horários votados pelos participantes cada semana.</p>
	</article>
	<article class="card">
		<h2>Para quem é</h2>
		<p>Qualquer um interessado em geometria da informação. Atualmente, a maioria dos participantes são da área de machine learning probabilístico, e portanto os artigos são pensados para pessoas com esse tipo de background. Se você tiver interesse, me mande um e-mail!</p>
	</article>
	<article class="card">
		<h2>Materiais</h2>
		<p>As notas de aula e links ficam organizados na página <a href={base + '/estudos'}>Estudos</a>.</p>
	</article>
</section>

<style>
	.hero {
		padding: 26px 22px;
		border: 1px solid var(--border);
		border-radius: 14px;
		background: var(--panel);
		box-shadow: var(--shadow);
		text-align: center;

		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	h1 {
		margin: 0 0 10px;
		font-size: clamp(28px, 3.2vw, 42px);
		line-height: 1.1;
		letter-spacing: -0.3px;
		font-family: Georgia, 'Times New Roman', Times, serif;
	}

	p {
		margin: 0;
		color: var(--muted);
		font-size: 16px;
		line-height: 1.6;
		max-width: 70ch;
		font-family: Georgia, 'Times New Roman', Times, serif;
	}

	p + p {
		margin-top: 10px;
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
		padding: 10px 14px;
		border-radius: 10px;
		border: 1px solid var(--border);
		font-weight: 650;
		letter-spacing: -0.1px;
	}

	.primary {
		background: var(--accent);
		border-color: var(--accent);
		color: white;
	}

	.primary:hover {
		filter: brightness(1.05);
	}

	.secondary {
		color: var(--accent);
		background: white;
	}

	.secondary:hover {
		background: var(--accent-soft);
	}

	.cards {
		margin-top: 18px;
		display: grid;
		grid-template-columns: 1fr;
		gap: 12px;
	}

	.card {
		border: 1px solid var(--border);
		border-radius: 14px;
		background: var(--panel);
		padding: 16px 16px 14px;
		text-align: center;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	.card h2 {
		margin: 0 0 6px;
		font-size: 16px;
		letter-spacing: -0.15px;
		text-align: center;
		font-family: Georgia, 'Times New Roman', Times, serif;
	}

	.card p {
		font-size: 14px;
		text-align: center;
		font-family: Georgia, 'Times New Roman', Times, serif;
	}
</style>
