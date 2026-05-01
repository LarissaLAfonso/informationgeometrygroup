<script lang="ts">
	const groupImage = '/grupo.svg';
	const organizerImage = '/organizadora.svg';
</script>

<section class="section">
	<h1>Sobre nós</h1>

	<div class="split">
		<img class="photo" src={groupImage} alt="Foto do grupo de estudos (substitua pela foto real)" />
		<div class="text">
			<h2>O grupo</h2>
			<p>
				Nos reunimos para estudar Geometria da Informação com calma e consistência: lendo textos-base, discutindo
				dúvidas e registrando notas para consulta.
			</p>
			<p>
				A ideia é manter um ambiente acolhedor, com espaço para perguntas, exemplos e conexões com aplicações.
			</p>
		</div>
	</div>

	<div class="organizer">
		<img class="avatar" src={organizerImage} alt="Foto da organizadora (substitua pela foto real)" />
		<div class="text">
			<h2>Organização</h2>
			<p>
				Eu sou a organizadora do grupo. Se você quiser participar, sugerir temas ou contribuir com materiais, me
				mande uma mensagem.
			</p>
		</div>
	</div>
</section>

<style>
	.section h1 {
		margin: 0 0 14px;
		font-size: clamp(26px, 3.4vw, 36px);
		letter-spacing: -0.3px;
	}

	.split {
		display: grid;
		grid-template-columns: 1.1fr 1fr;
		gap: 14px;
		align-items: center;
		border: 1px solid var(--border);
		border-radius: 18px;
		background: rgba(255, 255, 255, 0.04);
		padding: 14px;
	}

	.photo {
		width: 100%;
		aspect-ratio: 16 / 10;
		object-fit: cover;
		border-radius: 14px;
		border: 1px solid var(--border);
		background: rgba(255, 255, 255, 0.03);
	}

	.organizer {
		margin-top: 14px;
		display: grid;
		grid-template-columns: 120px 1fr;
		gap: 14px;
		align-items: center;
		border: 1px solid var(--border);
		border-radius: 18px;
		background: rgba(255, 255, 255, 0.04);
		padding: 14px;
		text-align: center;
	}

	.avatar {
		width: 120px;
		height: 120px;
		border-radius: 999px;
		border: 1px solid var(--border);
		background: rgba(255, 255, 255, 0.03);
	}

	.text h2 {
		margin: 0 0 6px;
		font-size: 16px;
	}

	.text p {
		margin: 0;
		color: var(--muted);
		line-height: 1.6;
		text-align: center;
	}

	.text p + p {
		margin-top: 10px;
	}

	@media (max-width: 860px) {
		.split {
			grid-template-columns: 1fr;
		}
		.organizer {
			grid-template-columns: 1fr;
		}
		.avatar {
			justify-self: start;
		}
	}
</style>
