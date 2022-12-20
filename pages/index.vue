<template>
	<main>
		<div class="card">
			<div class="card-images">
				<picture>
					<source srcset="../assets/images/image-product-desktop.jpg" media="(min-width: 600px)" />
					<img src="../assets/images/image-product-mobile.jpg" alt="Product Image" />
				</picture>
			</div>
			<div class="card-description">
				<p class="subtitle">Perfume</p>
				<h1>Gabrielle Essence Eau De Parfume</h1>
				<p>A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer-Creator for the House of CHANEL.</p>
				<div class="card-price">
					<h1>$149.99</h1>
					<p><s>$169.99</s></p>
				</div>
				<button class="btn">Add to Cart</button>
			</div>
		</div>
	</main>
</template>

<script setup lang="ts"></script>

<style>
	/*
	  1. Use a more-intuitive box-sizing model.
	*/
	*,
	*::before,
	*::after {
		box-sizing: border-box;
	}
	/*
	  2. Remove default margin
	*/
	* {
		margin: 0;
		--primary-dark-cyan: hsl(158, 36%, 37%);
		--primary-cream: hsl(30, 38%, 92%);

		--neutral-very-dark-blue: hsl(212, 21%, 14%);
		--neutral-very-dark-grayish-blue: hsl(228, 12%, 48%);
		--neutral-white: hsl(0, 0%, 100%);

		--fw-reguler: 500;
		--fw-bold: 700;

		--ff-base: 'Montserrat', sans-serif;
		--ff-accent: 'Fraunces', serif;
	}
	/*
	  3. Allow percentage-based heights in the application
	*/
	html,
	body {
		height: 100%;
	}
	/*
	  Typographic tweaks!
	  4. Add accessible line-height
	  5. Improve text rendering
	*/
	body {
		line-height: 1.5;
		-webkit-font-smoothing: antialiased;
		background-color: var(--primary-cream);

		font-family: var(--ff-base);
		font-weight: var(--fw-reguler);
		font-size: 0.83rem;

		color: var(--neutral-very-dark-grayish-blue);

		display: grid;
		place-content: center;
		margin: 1rem;
	}
	/*
	  6. Improve media defaults
	*/
	img,
	picture,
	video,
	canvas,
	svg {
		display: block;
		max-width: 100%;
	}
	/*
	  7. Remove built-in form typography styles
	*/
	input,
	button,
	textarea,
	select {
		font: inherit;
	}
	/*
	  8. Avoid text overflows
	*/
	p,
	h1,
	h2,
	h3,
	h4,
	h5,
	h6 {
		overflow-wrap: break-word;
	}

	h1 {
		font-family: var(--ff-accent);
		color: var(--neutral-very-dark-blue);
		font-size: 1.9rem;
		line-height: 2rem;
	}
	/*
	  9. Create a root stacking context
	*/
	#root,
	#__next {
		isolation: isolate;
	}

	.card {
		border-radius: 10px;
		overflow: hidden;
		background-color: var(--neutral-white);
        max-width: 600px;
	}


	.card-description {
		display: grid;
		gap: 0.5rem;
		padding: 1.5rem;
	}

	.card-price {
		display: flex;
		align-items: center;
		gap: 2em;
	}

	.card-price h1 {
		color: var(--primary-dark-cyan);
	}

	.subtitle {
		letter-spacing: 5px;
		text-transform: uppercase;
	}

	.btn {
		display: inline-flex;
		padding: 0.8rem 0.8rem;
		justify-content: center;
		align-items: center;
		border: 0;
		border-radius: 8px;
		background-color: var(--primary-dark-cyan);
		color: var(--neutral-white);
		gap: 0.5rem;
	}

	.btn::before {
		content: '';
		background-image: url('../assets/images/icon-cart.svg');
		width: 15px;
		height: 16px;
	}

    
	@media screen and (min-width: 600px) {
		.card {
            display: grid;
			grid-template-columns: 1fr 1fr;
		}

        .btn {
		    padding: 0rem 0.8rem;
        }
	}
</style>
