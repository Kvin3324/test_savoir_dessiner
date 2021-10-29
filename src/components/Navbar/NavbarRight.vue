<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container-fluid">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item shop-item">
            <a class="nav-link active" aria-current="page" href="#">Le shop</a>
          </li>
          <li class="nav-item basket-item d-flex">
            <img src="../../assets/basket_icon.svg" alt="basket-icon">
            <a class="nav-link" href="#">Mon panier</a>
          </li>
          <li class="nav-item login-item d-flex">
            <a class="nav-link" href="#">Se connecter</a>
            <img src="../../assets/right_arrow.svg" alt="right-arrow">
          </li>
          <li class="nav-item started-btn-item">
            <button type="button" class="btn">Commencer</button>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'navbar-right',
}
</script>

<style lang="scss" scoped>
  nav {
    div {
      #navbarNav {
        ul {
          align-items: center;
          li {
            padding: 0 20px;
            a {
              text-decoration: none;
            }
          }
          .shop-item {
            a {
              color: #717171;
            }
          }
          .basket-item {
            align-items: center;
            a {
              color: black;
              font-size: 14px;
              white-space: nowrap;
            }
          }
          .login-item {
            a {
              color: black;
              font-size: 16px;
              white-space: nowrap;
              font-weight: bold;
            }
          }
          .started-btn-item {
            button {
              background-color: #FFE401;
              color: black;
              font-weight: bold;
              padding: 10px;
              border-radius: 10px;
            }
          }
        }
      }
    }
  }

  

 

  .shop-item, .basket-item{
    border-right:1px solid #E8E8E8;
  }
</style>