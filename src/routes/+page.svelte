<script lang="ts">
	const links = [
		{
			label: 'GitHub',
			url: 'https://github.com/scmurphy96',
			icon: 'github'
		},
		{
			label: 'LinkedIn',
			url: 'https://www.linkedin.com/in/scmurphy96/',
			icon: 'linkedin'
		},
		{
			label: 'Resume',
			url: 'https://drive.google.com/file/d/1O6o_gN4SQeO-OrHYdyy2U0aPSxUo4_tq/view?usp=sharing',
			icon: 'file'
		}
	];
</script>

<main>
	<section class="hero">
		<div class="headshot-wrapper">
			<img
				src="/headshot.jpg"
				alt="Sean Murphy"
				class="headshot"
			/>
		</div>

		<h1>Sean Murphy</h1>
		<p class="tagline">Software Engineer</p>

		<nav class="links">
			{#each links as link}
				<a
					href={link.url}
					target={link.url.startsWith('http') ? '_blank' : undefined}
					rel={link.url.startsWith('http') ? 'noopener noreferrer' : undefined}
					class="link-btn"
				>
					<svg class="icon" viewBox="0 0 24 24" aria-hidden="true">
						{#if link.icon === 'github'}
							<path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z" fill="currentColor"/>
						{:else if link.icon === 'linkedin'}
							<path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z" fill="currentColor"/>
						{:else if link.icon === 'file'}
							<path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8l-6-6z" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
							<path d="M14 2v6h6M16 13H8M16 17H8M10 9H8" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
						{/if}
					</svg>
					{link.label}
				</a>
			{/each}
		</nav>
	</section>

	<section class="about">
		<h2>About Me</h2>
		<p>
			I'm a software engineer passionate about building clean, performant, and user-friendly
			applications. I enjoy working across the full stack, from crafting intuitive interfaces to
			designing robust backend systems. I'm always looking to learn new technologies and take on
			challenging problems that push me to grow as a developer.
		</p>
	</section>

	<footer>
		<p>&copy; {new Date().getFullYear()} Sean Murphy</p>
	</footer>
</main>

<style>
	main {
		max-width: var(--max-width);
		margin: 0 auto;
		padding: 4rem 1.5rem 2rem;
	}

	.hero {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		margin-bottom: 3rem;
	}

	.headshot-wrapper {
		margin-bottom: 1.5rem;
	}

	.headshot {
		width: 160px;
		height: 160px;
		border-radius: 50%;
		object-fit: cover;
		border: 3px solid var(--color-border);
		box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
	}

	h1 {
		font-size: 2.25rem;
		font-weight: 700;
		letter-spacing: -0.02em;
		margin-bottom: 0.25rem;
	}

	.tagline {
		font-size: 1.125rem;
		color: var(--color-text-muted);
		margin-bottom: 1.5rem;
	}

	.links {
		display: flex;
		gap: 0.75rem;
		flex-wrap: wrap;
		justify-content: center;
	}

	.link-btn {
		display: inline-flex;
		align-items: center;
		gap: 0.5rem;
		padding: 0.6rem 1.25rem;
		border: 1px solid var(--color-border);
		border-radius: 8px;
		background: var(--color-card-bg);
		color: var(--color-text);
		font-size: 0.9rem;
		font-weight: 500;
		transition: all 0.2s ease;
	}

	.link-btn:hover {
		border-color: var(--color-accent);
		color: var(--color-accent);
		box-shadow: 0 2px 8px rgba(37, 99, 235, 0.1);
	}

	.icon {
		width: 18px;
		height: 18px;
		flex-shrink: 0;
	}

	.about {
		background: var(--color-card-bg);
		border: 1px solid var(--color-border);
		border-radius: 12px;
		padding: 2rem;
		margin-bottom: 3rem;
	}

	.about h2 {
		font-size: 1.25rem;
		font-weight: 600;
		margin-bottom: 0.75rem;
	}

	.about p {
		color: var(--color-text-muted);
		font-size: 1rem;
		line-height: 1.75;
	}

	footer {
		text-align: center;
		padding: 1.5rem 0;
		border-top: 1px solid var(--color-border);
	}

	footer p {
		font-size: 0.85rem;
		color: var(--color-text-muted);
	}

	@media (max-width: 480px) {
		main {
			padding: 2.5rem 1rem 1.5rem;
		}

		h1 {
			font-size: 1.75rem;
		}

		.headshot {
			width: 120px;
			height: 120px;
		}

		.links {
			flex-direction: column;
			align-items: center;
		}

		.link-btn {
			width: 100%;
			max-width: 200px;
			justify-content: center;
		}
	}
</style>
