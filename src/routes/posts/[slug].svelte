<script context="module">
	export async function load({ params }) {
		try {
			const Post = await import(`../../posts/${params.slug}.md`);
			const { title, date, author } = Post.metadata;

			return {
				props: {
					Post: Post.default,
					title,
					date,
					author
				}
			};
		} catch (e) {
			return {
				status: 404,
				error: 'Womp. Womp. Post not found.'
				// redirect: '/posts'
			};
		}
	}
</script>

<script>
	export let Post, title, date, author;
</script>

<h3>{title}</h3>
<h5>{date}</h5>
<h5>{author}</h5>
<article>
	<svelte:component this={Post} />
</article>
