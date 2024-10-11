<script>
export let title = "Simulation. This Is How The Covid-19 Can Spread In Public Transport."
export let image = "https://resizer.glanacion.com/resizer/wsH9qhqEmYUDAbfMZo3pgMNQyM8=/1200x746/filters:format(webp):quality(80)/cloudfront-us-east-1.images.arcpublishing.com/lanacionar/4VT6FVWGRJEMZNGRDOFAWME4GA.gif"
export let alt = "simulacion_particulas_colectivo_gif"
export let link = "https://www.lanacion.com.ar/sociedad/simulacion-asi-se-puede-propagar-el-virus-en-el-transporte-nid11042021/"
export let published = "La Nacion"
export let roles = ["Reporting"]
</script>

<article>
	<a href={link} target="_blank">
		<figure>
			<img src={image} {alt} />
		</figure>
		<h4 class="texto_project">{ title }</h4>
		<h5 class="publisher">{published}</h5>
	
		<div class="rolesContainer">
			{#each roles as r}
				<p class="roles">{r}</p>
			{/each}
		</div>
	</a>
</article>

<style>
	article a {
		text-decoration: none;
		width: 100%;
		height: 100%;
		display: flex;
		flex-direction: column;
	}
	
	.publisher {
		margin: 0;
		padding: 0.5rem;
		text-transform: uppercase;
		font-weight: 500;
		color: #000000;
		font-size: 0.85rem;
		margin-top: auto;
	}
	.projects {
		margin: 10px auto;
		width: 90%;
	}
	
	.projects h3 {
		font-size: 1.1rem;
		font-weight: 500;
		text-transform: uppercase;
		color: #2b2424;
		margin-bottom: 40px;
		padding-bottom: 5px;
		border-bottom: 2px solid black;
	}
	
	.container {
		display: grid;
		grid-template-columns: 1fr;
		grid-column-gap: 20px;
		grid-row-gap: 50px;
		margin: auto;
		padding-bottom: 0.5rem;
	}
	
	.container article {
		border: 1px solid #e2e6e7;
		display: flex;
		align-items: center;
		/*height: 350px;*/
		/*box-shadow: 0px 0px 5px 0px #38383873;*/
	}
	
	article::after {
		content: "";
		position: absolute;
		width: 100%;
		transform: scaleX(0);
		height: 3px;
		bottom: 0;
		left: 0;
		background-color: #000000;
		transform-origin: bottom right;
		transition: transform 0.15s ease-out;
	}
	
	article:hover:after {
		transform: scaleX(1);
		transform-origin: bottom left;
	}
	.container article img,
	.container article video {
		width: 100%;
		height: 100%;
		border-bottom: 1px solid #e2e6e7;
	}
	
	.container article video {
		background-color: black;
	}
	
	.container article .texto_project {
		padding: 0.5rem;
		font-weight: 200;
		font-size: 0.9rem;
		margin: 10px 0;
		line-height: 1.5;
		color: #000000;
	}
	
	.container article p {
		font-size: 0.8rem;
		font-weight: 100;
		padding-left: 0.5rem;
	}
	
	button {
		border: 1px solid #5e5e5e82;
		background-color: transparent;
		border-radius: 2px;
		background-color: #f7f7f7;
		margin: 0 0 0.8rem 0.5rem;
		padding: 0.3rem 0.5rem;
	}
	
	button a {
		color: black;
		text-decoration: none;
		text-transform: uppercase;
		font-weight: 300;
		font-size: 12px;
		font-family: "Hind", sans-serif;
	}
	
	button a:hover {
		color: black;
		opacity: 0.7;
	}
	
	.rolesContainer {
		display: flex;
		flex-direction: row;
		padding-bottom: 20px;
	}
	
	.roles {
		border: 1px solid #00000087;
		border-radius: 3px;
		padding: 2px 10px;
		color: #000;
		margin-left: 7px;
		font-size: 12px !important;
		pointer-events: none;
		font-weight: 200 !important;
		text-transform: lowercase;
	}
	
	@media screen and (min-width: 500px) {
		.container {
			grid-template-columns: repeat(2, 1fr);
		}
	}
	
	@media screen and (max-width: 780px) {
		article figure {
			width: auto;
		}
	}
	
	@media screen and (min-width: 1000px) {
		.container article .texto_project {
			padding: 0 0.5rem;
			font-size: 0.85rem;
		}
		.container {
			grid-template-columns: repeat(3, 1fr);
		}
	
		.container article figure,
		.container article video {
			/* height: 250px; */
			margin: 0;
		}
	
		.projects {
			max-width: 1100px;
			margin: 2rem auto;
		}
	}
	</style>
	
