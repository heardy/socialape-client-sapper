<script>
  export let scream = {};
</script>

<style>
  .card {
    /* height: 100px; */
    margin-bottom: 20px;
  }

  .card-img {
    height: 142px;
    min-width: 200px;
    object-fit: cover;
  }
</style>

{#if Object.keys(scream).length > 0}
<div class="card mb-4">
  <div class="row no-gutters">
    <div class="col-md-4">
      <img src="{scream.userImage}" class="card-img" title="Profile image" alt="profile image" />
    </div>
    <div class="col-md-8">
      <div class="card-body">
        <h5 class="card-title">
          <a href="{`/users/${scream.userHandle}`}">{scream.userHandle}</a>
        </h5>
        <p class="card-text">{scream.createdAt}</p>
        <p class="card-text">{scream.body}</p>
      </div>
    </div>
  </div>
</div>
{/if}
