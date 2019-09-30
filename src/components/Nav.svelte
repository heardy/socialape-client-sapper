<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	.selected {
		position: relative;
		display: inline-block;
	}

	.selected::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>

<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarTogglerDemo01" aria-controls="navbarTogglerDemo01" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
    <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
      <li class="nav-item {segment === 'login' ? 'active' : ''}">
        <a class="nav-link" href="login">Login</a>
      </li>
      <li class="nav-item {segment === undefined ? 'active' : ''}">
        <a class="nav-link" href=".">Home <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item {segment === 'signup' ? 'active' : ''}">
        <a class="nav-link" href="signup">Signup</a>
      </li>
    </ul>
  </div>
</nav>

<!-- <nav class="navbar fixed-top navbar-dark bg-primary">
	<ul class="navbar-nav">
	  <li class="nav-item">
        <a class="nav-link active" href="home">home</a>
      </li>
	  <li class="nav-item">
        <a class="nav-link" href="#">Link</a>
      </li>
	  <li class="nav-item">
        <a class="nav-link" href="#">Link</a>
      </li>
	</ul>

	<div class="collapse navbar-collapse" id="navbarNavDropdown">
    <ul class="navbar-nav">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Features</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Pricing</a>
      </li>
      <li class="nav-item dropdown">
        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          Dropdown link
        </a>
        <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
          <a class="dropdown-item" href="#">Action</a>
          <a class="dropdown-item" href="#">Another action</a>
          <a class="dropdown-item" href="#">Something else here</a>
        </div>
      </li>
    </ul>
</nav>

<nav>
	<ul>
		<li><a class='{segment === undefined ? "selected" : ""}' href='.'>home</a></li>
		<li><a class='{segment === "login" ? "selected" : ""}' href='login'>login</a></li>
		<li><a class='{segment === "signup" ? "selected" : ""}' href='signup'>signup</a></li>
	</ul>
</nav> -->
