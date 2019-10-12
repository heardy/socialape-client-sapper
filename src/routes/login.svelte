<script>
  import * as sapper from '@sapper/app';
  import axios from 'axios';

  let email = '';
  let password = '';
  let isLoading = false;
  let errors = {};

  function handleSubmit(event) {
    event.preventDefault();

    isLoading = true;

    const userData = {
      email,
      password
    };

    axios.post('https://asia-east2-socialape-bdca8.cloudfunctions.net/api/login', userData)
      .then(res => {
        console.log(res);
        sapper.goto('/');
      })
		  .catch(err => {
        if (err.response) errors = err.response.data;
        else console.log(err);
      })
      .finally(() => {
        isLoading = false;
      });
  }
</script>

<style>
  .container {
    display: flex;
    flex-direction: column;
    align-items: center
  }

  img {
    margin: 20px auto;
  }

  form {
    display: flex;
    flex-direction: column;
    align-content: center;
    min-width: 250px;
  }
</style>

<div class="container">
  <img src="icon.png" alt="monkey" />
  <h1>Login</h1>
  <form on:submit="{handleSubmit}">
    <div class="form-group">
      <input type="email" class="form-control form-control-sm" placeholder="Email" bind:value={email}>
      {#if errors.email}
        <small class="form-text text-muted">{errors.email}</small>
      {/if}
    </div>
    <div class="form-group">
      <input type="password" class="form-control form-control-sm" placeholder="Password" bind:value={password}>
      {#if errors.password}
        <small class="form-text text-muted">{errors.password}</small>
      {/if}
    </div>
    {#if errors.general}
      <p>{errors.general}</p>
    {/if}
    <button type="submit" class="btn btn-primary" disabled="{isLoading}">
      {#if isLoading}
      <span class="spinner-border spinner-border-sm" role="status" aria-hidden="true"></span>
      {/if}
      Login
    </button>
  </form>
</div>
