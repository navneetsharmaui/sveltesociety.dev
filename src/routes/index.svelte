<script>
	// import Link from '../lib/components/_SocialLinks/Link.svelte';
	import Link from '$layout/Link.svelte';
	import { page } from '$app/stores';
	import metatags from '$lib/stores/metatags';

	metatags.title('Svelte Society - a community for Svelte users around the world.');
	metatags.desc('Svelte Society is a community-driven effort to organise and promote SvelteJS.');
	metatags.url($page.host + $page.path);
</script>

<svelte:head>
	<title>Home - Svelte Society</title>
</svelte:head>

<article class="container">
  <h1 class="text-center">Welcome to Svelte Society!</h1>
	<section>
		<p>
			We are a volunteer global network of Svelte fans that strive to promote Svelte and its
			ecosystem. As a service to the community, this site is a central index of <a href="/events"
				>events</a
			>, a <a href="/components">components directory</a>, as well as <a href="/recipes">recipes</a>
			and other useful resources. Join us or help us out!
		</p>
		<p>
			If you want to reach out to us or find like-minded people from around the world you can check
			out the resources below:
		</p>
	</section>
	<ul>
		<Link path="https://discord.gg/svelte">
			<img src="images/discord.svg" alt="" />
			Discord
		</Link>
		<Link path="https://youtube.com/SvelteSociety">
			<img src="images/youtube.svg" alt="" />
			YouTube
		</Link>
		<Link path="https://twitter.com/sveltesociety">
			<img src="images/twitter.svg" alt="" />
			Twitter
		</Link>
	</ul>
	<ul>
		<Link path="https://svelte.substack.com/">
			<img src="images/newsletter.svg" alt="" />
			Newsletter
		</Link>
		<Link path="https://www.reddit.com/r/sveltejs/">
			<img src="images/reddit.svg" alt="" />
			Reddit
		</Link>
		<Link path="https://www.svelteradio.com/">
			<img src="images/radio.svg" alt="" />
			Podcast
		</Link>
	</ul>
	<p class="text-center">
		We also run the <a href="https://sveltesummit.com/">Svelte Summit</a> conference.
	</p>
</article>

  <style>
    article{
      max-width: 1024px;
      display: grid;
      gap: var(--s-20);
    }
    h1 {
      margin: 0;
    }
    section {
      display: grid;
      gap: var(--s-5);
    }
    ul {
      display: flex;
      flex-wrap: wrap;
      column-gap: var(--s-20);
      row-gap: var(--s-5);
      justify-content: space-around;
      text-align: center;
    }
    img {
      width: 128px;
    }
  </style>