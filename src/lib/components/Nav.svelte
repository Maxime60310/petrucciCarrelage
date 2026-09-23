<script lang="ts">
	import logo from '$lib/img/logo.svg';

	let menuOpen = $state(false);

	const toggleMenu = () => {
		menuOpen = !menuOpen;
	};

	const closeMenu = () => {
		menuOpen = false;
	};
</script>

<header>
	<nav class:menuOpen>
		<div class="top-nav">
			<a href="/" class="logo" onclick={closeMenu}>
				<img src={logo} alt="Logo de Petrucci Carrelage" />
			</a>

			<button
				class="burger"
				class:active={menuOpen}
				onclick={toggleMenu}
				aria-label={menuOpen ? 'Fermer le menu' : 'Ouvrir le menu'}
				aria-expanded={menuOpen}
			>
				<div></div>
			</button>
		</div>

		<ul class:active={menuOpen}>
			<li>
				<a href="#about" onclick={closeMenu}> À Propos de nous </a>
			</li>

			<li>
				<a href="#projects" onclick={closeMenu}> Réalisations </a>
			</li>

			<li>
				<a href="#reviews" onclick={closeMenu}> Avis </a>
			</li>

			<li>
				<a href="#contact" class="contactButton" onclick={closeMenu}>
					Contacter pour un projet !
				</a>
			</li>
		</ul>
	</nav>

	<button class="closeNav" class:active={menuOpen} onclick={closeMenu} aria-label="Fermer le menu"
	></button>
</header>

<style lang="scss">
	:root {
		--primary: #356ecc;
		--dark: #1e293b;
		--white: #ffffff;
		--text: #475569;
	}

	header {
		height: 10vh;
		width: 100%;
	}

	nav {
		height: 4rem;
		width: calc(100% - 1rem);
		padding: 0 0.5rem;

		position: fixed;
		top: 0;
		left: 0;
		z-index: 10;

		display: flex;
		justify-content: space-between;
		align-items: center;

		box-shadow: 0 0 8px 0 rgba(0, 0, 0, 0.12);

		&::before {
			content: '';
			position: absolute;
			z-index: -1;
			inset: 0;

			background: rgba(255, 255, 255, 0.85);
			backdrop-filter: blur(15px);
		}

		.top-nav {
			height: 100%;

			display: flex;
			align-items: center;

			.logo {
				display: flex;
				align-items: center;

				img {
					height: 3rem;
					width: auto;
					display: block;
				}
			}
		}

		.burger {
			height: 2rem;
			width: 3rem;

			display: none;

			border: none;
			background: none;
			cursor: pointer;

			div {
				width: 2.5rem;
				height: 0.2rem;

				position: relative;

				border-radius: 0.08rem;
				background: var(--dark);

				transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);

				&::before,
				&::after {
					content: '';

					width: 100%;
					height: 100%;

					position: absolute;
					left: 0;

					border-radius: 0.08rem;
					background: var(--dark);

					transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
				}

				&::before {
					bottom: 250%;
				}

				&::after {
					top: 250%;
				}
			}

			&.active {
				div {
					transform: rotate(45deg);

					&::before {
						bottom: 0;
					}

					&::after {
						top: 0;
						transform: rotate(-90deg);
					}
				}
			}
		}

		ul {
			width: 45rem;
			height: 100%;

			margin: 0;
			padding: 0;

			display: flex;
			justify-content: space-between;
			align-items: center;

			list-style: none;

			li {
				margin-left: 1.5rem;

				a {
					color: var(--text);

					text-decoration: none;
					font-size: 1rem;

					position: relative;

					/* Soulignement animé */
					&:not(.contactButton)::after {
						content: '';

						position: absolute;
						left: 0;
						bottom: 0;

						width: 100%;
						height: 0.1em;

						background-color: var(--primary);

						opacity: 0;

						transform: translate3d(0, 0, 0);

						transition:
							opacity 300ms,
							transform 300ms;
					}

					&:not(.contactButton):hover::after,
					&:not(.contactButton):focus::after {
						opacity: 1;
						transform: translate3d(0, 0.2em, 0);
					}
				}

				.contactButton {
					display: inline-block;

					padding: 0.8rem 1rem;

					background-color: var(--dark);
					color: var(--white);

					border-radius: 0.3rem;

					text-align: center;

					transition:
						background-color 200ms ease,
						transform 200ms ease;

					&:hover {
						background-color: var(--primary);
						transform: translateY(-2px);
					}
				}
			}
		}
	}

	.closeNav {
		height: 80vh;
		width: 100%;

		border: none;
		background: transparent;

		position: fixed;
		z-index: 5;

		top: -100vh;
		left: 0;

		display: none;
	}

	@media (max-width: 850px) {
		nav {
			height: auto;
			min-height: 4rem;

			flex-direction: column;
			align-items: stretch;

			.top-nav {
				width: 100%;
				height: 4rem;

				display: flex;
				justify-content: space-between;
				align-items: center;

				.burger {
					display: block;
				}
			}

			ul {
				width: 100%;
				height: auto;

				max-height: 0;

				flex-direction: column;
				justify-content: flex-start;

				overflow: hidden;

				transition: max-height 500ms ease;

				li {
					margin: 1rem 0;

					&:first-child {
						margin-top: 1.5rem;
					}

					&:last-child {
						margin-bottom: 1.5rem;
					}
				}

				&.active {
					max-height: 25rem;
				}
			}
		}

		.closeNav {
			display: block;

			&.active {
				top: 15rem;
			}
		}
	}
</style>
