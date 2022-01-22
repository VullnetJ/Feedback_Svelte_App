<script>
import FeedbackForm from './components/FeedbackForm.svelte';
import FeedbackList from './components/FeedbackList.svelte'
import FeedbackStats from './components/FeedbackStats.svelte';
  


	// const addFeedback = (e) => {
	// 	const newFeedback = e.detail
	// 	feedback = [newFeedback, ...feedback]
	// }
//   const deleteFeedback = (e) => {
// 	  const itemId = e.detail
// 	  feedback = feedback.filter((item) => item.id != itemId )
// 	  text = ""
//   }
</script>

<main class="container">
	<FeedbackForm />
	<FeedbackStats />
  <FeedbackList />
</main>


<!-- on:delete-feedback = {deleteFeedback} -->
<!-- main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #e75f31;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	} -->
<!-- 
	//  to change first name just do: firstName = 'John'
	<h1 style="color: {color}">Hello {name}</h1>
	{#if showText}
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	{:else} 
		<p>No text</p>
	{/if}
	
	<button on:click={toggle}>Click</button>
	
	{#each users as user (user.id)}
	<h3>{user.id}: {user.name}</h3>
	
	{/each}
 -->

<!-- let firstName=  'John';
	let lastName=  'Doe';
	$: name = firstName + ' ' + lastName
	let color = 'orange'
	let showText = false
	const toggle = () => {
		color = color ==='orange'? 'purple': 'orange'
		showText = !showText
		users = [...users, {id: 4, name:'Ola'}]
	}
	let users = [
		{
			id: '1',
			name: 'John',
		},
		{
			id: '2',
			name: 'Elsa',
		},
		{
			id: '3',
			name: 'Bob',
		},
	]
 -->

<style>
</style>
