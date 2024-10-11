<script>
  import ArticleContainer from "./ArticleContainer.svelte";
  import welcome from "$lib/images/svelte-welcome.webp";
  import welcome_fallback from "$lib/images/svelte-welcome.png";
  import { proyectos } from "../stores";
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>

  <h1>Juana Copello</h1>


  <p>¡Hola!</p>
  <p>I am a journalist specialized in Data Visualization and Visual Storytelling from Buenos Aires, Argentina</p>
  <p>Since 2019, I have been working at the Visual Storytelling and Graphics Team at La Nación. Since 2022, I have been an Assistant Professor at the Data Visualization and Design-Oriented Programming courses from the Universidad Torcuato Di Tella's Design School</p>
  <p>I hold a Bachelor's Degree in Communications and Journalism from the Universidad Católica Argentina</p>
  <p>I am always open for collaborations :) If you want to reach out, you can email me or find me on twitter and linkedin</p>
  <p>You can view my full resume here</p>


</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex: 0.6;
  }

  h1 {
    width: 100%;
  }

  .welcome {
    display: block;
    position: relative;
    width: 100%;
    height: 0;
    padding: 0 0 calc(100% * 495 / 2048) 0;
  }

  .welcome img {
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    display: block;
  }
</style>
