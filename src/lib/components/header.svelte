<script>
	import Header from '$lib/img/header.jpeg';
</script>

<header>
	<div class="overlay"></div>
	<img src={Header} alt="Salle de bain" />
	<div class="articleHeader">
		<h1>Votre expert carreleur</h1>
		<h2>Salles de bains, cuisines, terrasses. Qualité & précision.</h2>
		<div class="buttons">
			<button class="contactButton"> Contacter pour un projet ! </button>
			<button class="reaButton"> Voir nos réalisation</button>
		</div>
	</div>
</header>

<style lang="scss">
	header {
		position: relative;
		height: 60vh;
		.overlay {
			position: absolute;
			inset: 0;
			background: rgba(0, 0, 0, 0.55);
			z-index: 1;
		}

		img {
			width: 100%;
			height: 100%;
			object-fit: cover;
			object-position: center;
		}

		.articleHeader {
			min-height: 12rem;
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			text-align: center;
			position: absolute;
			z-index: 2;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);

			h1 {
				color: var(--white);
			}
			h2 {
				color: #aeaeae;
			}

			.buttons {
				display: flex;
				justify-content: space-around;
				.contactButton {
					width: 12rem;
					padding: 0.8rem 1rem;
					background-color: var(--dark);
					color: var(--white);
					border-radius: 0.3rem;
					text-align: center;
					border: none;
					cursor: pointer;
					transition:
						background-color 200ms ease,
						transform 200ms ease;
					&:hover {
						transform: translateY(-2px);
					}
				}

				.reaButton {
					width: 12rem;
					padding: 0.8rem 1rem;
					background-color: var(--primary);
					color: var(--white);
					border-radius: 0.3rem;
					text-align: center;
					border: none;
					cursor: pointer;
					transition:
						background-color 200ms ease,
						transform 200ms ease;
					&:hover {
						transform: translateY(-2px);
					}
				}
			}
		}
	}

	@media (max-width: 800px) {
		header {
			.articleHeader {
				width: 100%;
				height: 45%;
				.buttons {
					height: 6rem;
					flex-direction: column;
					align-items: center;
				}
			}
		}
	}
</style>
