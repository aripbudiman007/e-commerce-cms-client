<template>
    <header class="header bg-light">
        <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="/">Agreculture</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav pull-right">
                <li class="nav-item">
                <router-link to="/signup" class="nav-link active" aria-current="page" >Daftar</router-link>
                </li>
                <li class="nav-item">
                <router-link to="/login" class="nav-link" aria-current="page" >Login</router-link>
                </li>
            </ul>
            <ul class="navbar-nav pull-right">
                <li class="nav-item">
                    <router-link to="/product" class="nav-link active" aria-current="page" >Product</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/category" class="nav-link" aria-current="page" >Category</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/video" class="nav-link" aria-current="page" >Video</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/cart" class="nav-link" aria-current="page" >Cart ({{total}})</router-link>
                </li>
            </ul>
            </div>
        </div>
        </nav>
        </div>
    </header>
</template>

<script>
export default {
  name: 'Navbar',
  computed: {
    total () {
      const total = this.$store.state.shoppingCart
      return total.length
    }
  },
  created () {
    this.$store.dispatch('fetchShoppingCart')
  }
}
</script>

<style scoped>

</style>
