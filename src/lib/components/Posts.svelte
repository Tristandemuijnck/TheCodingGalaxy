<section id="posts">
	<h2>Latest Posts</h2>
	<hr />
	<article>
		<h3>Toegankelijkheid</h3>
		<p>
			Toegankelijkheid op het web betekent dat iedereen, ongeacht beperking, een website kan
			gebruiken...
		</p>
		<a href="#">Read more</a>
	</article>
    <hr />
    <article class="alt">
		<h3>Toegankelijkheid</h3>
		<p>
			Toegankelijkheid op het web betekent dat iedereen, ongeacht beperking, een website kan
			gebruiken...
		</p>
		<a href="#">Read more</a>
	</article>
    <hr />
    <article>
		<h3>Toegankelijkheid</h3>
		<p>
			Toegankelijkheid op het web betekent dat iedereen, ongeacht beperking, een website kan
			gebruiken...
		</p>
		<a href="#">Read more</a>
	</article>
    <hr />

    <a class="page-link" href="/posts">All Posts</a>
</section>

<style>
	section {
		position: relative;
		padding: 1.5rem;
		width: 100%;
		height: 100vh;
	}

	h2 {
		color: var(--primary-white);
		font-weight: bold;
		font-family: var(--title-font);
		-webkit-text-stroke: 1px var(--primary-black);
		font-size: 3rem;
		text-shadow: 0px 4px 0px #090909 !important;
		text-transform: uppercase;
        padding: 1rem 0;
	}

	hr {
		margin: 0.8rem 0;
		border: solid 1px rgb(132, 132, 132);
		background: rgb(132, 132, 132);
		width: 100%;
	}

	article {
		display: flex;
		row-gap: 0.8rem;
		flex-direction: column;
		padding: 1.4rem 0.6rem;
	}

    .alt {
        align-items: flex-end;
    }

	h3 {
		color: var(--primary-black);
		font-weight: 500;
		font-family: var(--body-font);
		letter-spacing: 2px;
		text-transform: uppercase;
	}

    .alt h3 {
        margin-right: 2.5rem;
    }

	p {
		padding-left: 0.5rem;
		max-width: 16rem;
		color: var(--primary-black);
		font-weight: 300;
		font-family: var(--body-font);
		letter-spacing: 1px;
	}

	article > a {
		position: relative;
		padding-left: 0.5rem;
		color: var(--primary-black);
		font-weight: 500;
		font-size: 1.1rem;
		font-family: var(--title-font);
		text-decoration: underline;
		text-transform: uppercase;
	}

    .alt a {
        padding-right: 0.5rem;
    }

	article > a::before {
		position: absolute;
		bottom: 50%;
		left: -3rem;
		transform: translateY(-50%);
		animation: pulse 3s ease-in-out infinite;
		background: var(--primary-black);
		width: 50px;
		height: 1px;
		content: '';
	}

    .alt a::before {
        left: unset;
        right: -3rem;
    }

    .page-link {
        position: absolute;
        right: 3.5rem;
        bottom: 3rem;
		padding-left: 0.5rem;
		color: var(--primary-black);
		font-weight: 500;
		font-size: 1.4rem;
		font-family: var(--title-font);
		text-decoration: underline;
		text-transform: uppercase;
        letter-spacing: 1px;
    }

    .page-link::before {
        position: absolute;
        bottom: 50%;
        right: -3.5rem;
        transform: translateY(-50%);
        animation: pulse 3s ease-in-out infinite;
        background: var(--primary-black);
        width: 50px;
        height: 1px;
        content: '';
    }
</style>
