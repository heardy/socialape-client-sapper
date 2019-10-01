<script>
  import { onMount } from 'svelte';
  import axios from 'axios';

  import Scream from '../components/Scream.svelte';

  let screams = [];

  onMount(() => {
	  axios.get('https://asia-east2-socialape-bdca8.cloudfunctions.net/api/screams')
	    .then(res => {
			screams = res.data;
		})
		.catch(err => console.log(err));
  });
</script>

<style>

</style>

<div class="container">
  <div class="row">
    <div class="col col-xs-12 col-sm-8">
      {#each screams as scream}
	  <Scream {scream} />
	  {:else}
	  <p>Loading...</p>
	  {/each}
    </div>
    <div class="col col-xs-12 col-sm-4">
      <p>Profile...</p>
    </div>
  </div>
</div>

<div>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
	<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsum, cupiditate ex vitae et fuga consectetur natus possimus unde maiores! Quidem nihil eligendi ipsum dolorem est vel optio enim error! Blanditiis!</p>
</div>