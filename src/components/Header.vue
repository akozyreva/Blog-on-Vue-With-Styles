<template>
    <div>
    	<nav class="navbar navbar-expand-lg navbar-light fixed-top" id="mainNav">
      <div class="container">
        <router-link to="/" tag="a" class="navbar-brand"><a>BLOG</a></router-link>
        <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
          Menu
          <i class="fa fa-bars"></i>
        </button>
         <router-link to="/create" tag="a" active-class="active" class="btn btn-primary "><a>Create article</a></router-link>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="navbar-nav ml-auto">
          	<!-- ROUTING -->
            <router-link to="/" tag="li" class="nav-item" active-class="active" exact><a class="nav-link">Home</a></router-link>
            <router-link to="/about" tag="li" class="nav-item"  active-class="active"><a class="nav-link">About me</a></router-link>
            <router-link to="/articles" tag="li" class="nav-item"  active-class="active"><a class="nav-link" >Articles</a></router-link>
          </ul>
        </div>
      </div>
    </nav>
    </div>
</template>