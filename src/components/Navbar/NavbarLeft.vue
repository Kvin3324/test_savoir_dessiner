<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container-fluid">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <a class="nav-link active" aria-current="page" href="#">L'atelier online</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Les RDV coaching</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">La box</a>
          </li>
          <li class="nav-item d-flex">
            <a class="nav-link">A propos</a>
            <img src="../../assets/arrow_down.svg" alt="arrow-down">
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'navbar-left',
}
</script>

<style lang="scss" scoped>
nav {
  div {
    #navbarNav {
      ul {
        li {
          a {
            color: black;
            text-decoration: none;
            font-weight: bold;
          }
        }
      }
    }
  }
}
</style>