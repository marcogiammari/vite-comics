<script>
  export default {
    name: 'AppHeader',
    data() {
        return {
            navbarLinks: [
              'Characters',
              'Comics',
              'Movies',
              'Tv',
              'Games',
              'Collectible',
              'Videos',
              'Fans',
              'News',
              'Shop'
            ]
        }
    } 
  }

</script>


<template>
  <header class="bg-light">
    <div class="container">
      <div class="row">
        <div class="col-5 d-flex align-items-center">
          <a href="#"><img id="header-logo" class="img-fluid" src="../assets/img/dc-logo.png" alt="DC Logo"></a>
        </div>
        <div class="col-7 d-none d-lg-flex justify-content-end align-items-center">
          <ul class="d-flex m-0">
            <li v-for="link in navbarLinks" class="d-flex flex-column">
              <a href="#">{{link.toUpperCase()}}</a>
              <div></div>
            </li>  
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>

$primarycolor: #0C7CEC;

  div, ul {
    height: 100%;
  }

  header {
    height: 100px;
  }

  #header-logo {
    height: 65%;
  }

  ul {
    list-style-type: none;
  }

  li {
    margin: 0 1rem;
    font-weight: 600;
    font-size: .875rem;
    height: 100%;
  }

  li > div {
    background-color: $primarycolor;
    height: .5rem;
    display: none;
  }

  li:hover div {
    display: block;
  }

  a {
    text-decoration: none;
    height: 100%;
    color: rgb(70, 70, 70);
    margin-top: 2.5rem;

    &:hover {
    color: $primarycolor;
    }
  }

</style>
