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
				Pensado e organizado por estudantes da Escola de Matemática Aplicada (EMAp) da Fundação Getúlio Vargas (FGV), no Rio de Janeiro, que trabalham no laboratório do professor Diego Mesquita. Nossos principais interesses se encontram na união de machine learning probabilístico, estatística e geometria. Somos um grupo diverso e inclusivo :)
			</p>
			<p>
				Começamos a realizar os encontros de maneira regular, a princípio presencialmente, em agosto de 2025, e começamos a documentar nossas atividades em maio de 2026. 
			</p>
			<p>
				Se você tiver interesse em participar, me mande um e-mail!
			</p>
		</div>
	</div>

	<div class="organizer">
		<img class="avatar" src={organizerImage} alt="Foto da organizadora (substitua pela foto real)" />
		<div class="text">
			<h2>Organização</h2>
			<h2>Larissa Lemos Afonso</h2>
			<p>
				Sou estudante de graduação em Ciência de Dados e Inteligência Artifical na FGV-EMAp. Sou apaixonada por geometria e estatística, e estou sempre querendo expandir meus horizontes matemáticos.
			</p>

			<div class="social-links">
                <a href="https://www.linkedin.com/in/larissa-lemos-afonso-087b78196/" target="_blank" rel="noopener noreferrer" class="social-link">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                    </svg>
                    LinkedIn
                </a>
                <a href="https://github.com/LarissaLAfonso" target="_blank" rel="noopener noreferrer" class="social-link">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
                    </svg>
                    GitHub
                </a>
            </div>
		</div>
	</div>
</section>

<style>
	.section h1 {
		margin: 0 0 14px;
		font-size: clamp(26px, 3.2vw, 36px);
		letter-spacing: -0.3px;
	}

	.split {
		display: grid;
		grid-template-columns: 1.1fr 1fr;
		gap: 18px;
		align-items: center;
		border: 1px solid var(--border);
		border-radius: 14px;
		background: var(--panel);
		box-shadow: var(--shadow);
		padding: 18px;
	}

	.photo {
		width: 100%;
		aspect-ratio: 16 / 10;
		object-fit: cover;
		border-radius: 12px;
		border: 1px solid var(--border);
		background: #f3f4f6;
	}

	.organizer {
		margin-top: 14px;
		display: grid;
		grid-template-columns: 120px 1fr;
		gap: 16px;
		align-items: center;
		border: 1px solid var(--border);
		border-radius: 14px;
		background: var(--panel);
		box-shadow: var(--shadow);
		padding: 18px;
	}

	.avatar {
		width: 120px;
		height: 120px;
		border-radius: 999px;
		border: 1px solid var(--border);
		background: #f3f4f6;
	}

	.text h2 {
		margin: 0 0 6px;
		font-size: 16px;
		letter-spacing: -0.15px;
	}

	.text p {
		margin: 0;
		color: var(--muted);
		line-height: 1.65;
		max-width: 80ch;
	}

	.text p + p {
		margin-top: 10px;
	}

	.social-link {
        display: inline-flex;
        align-items: center;
        gap: 6px;
        padding: 5px 12px;
        border-radius: 8px;
        border: 1px solid var(--border);
        font-size: 13px;
        font-weight: 500;
        color: var(--muted);
        text-decoration: none;
        transition: color 0.15s, border-color 0.15s, background 0.15s;
    }
    .social-link:hover {
        color: var(--foreground, #111);
        border-color: currentColor;
        background: var(--hover, rgba(0,0,0,0.04));
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
