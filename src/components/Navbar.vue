<template>
  <nav class="navbar">
    <a href="#/"><img class="navbar-image" :src="logo" alt="Lido Panciteria"></a>
    <div class="navbar-items">
      <div v-for="link in links" :key="link.text" class="navbar-item">
        <a :href="link.url">{{ link.text }}</a>
      </div>
    </div>
  </nav>
</template>

<script>
import logo from '../images/lidoLogo.jpg'

export default {
  name: 'Navbar',
  data () {
    return {
      logo: logo, // Assign the imported logo to the 'logo' data property
      links: [
        { text: 'About', url: '#/about' },
        { text: 'Services', url: '#/services' },
        { text: 'Contact', url: '#/contact' }
      ]
    }
  }
}
</script>

<style scoped>
  .navbar {
    position: sticky; /* Make the navbar sticky */
    top: 0; /* Stick to the top of the viewport */
    background-color: #ffffff;
    padding: 20px 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    display: flex;
    align-items: center;
    justify-content: flex-start; /* Center items horizontally */
    z-index: 1000; /* Ensure it's above other content */
  }
  .navbar-image {
    width: 20rem;
  }
  .navbar-items {
    display: flex;
    margin-left: 1rem;
    justify-content: space-around; /* Distribute items evenly */
    width: 100%; /* Full width of the parent container */
    max-width: 20rem; /* Limit maximum width */
  }
  .navbar-item {
    text-align: center;
    margin-left: 1rem;
  }
  .navbar a {
    color: #333333;
    text-decoration: none;
    font-weight: 500;
    border-radius: 4px;
    transition: background-color 0.3s, color 0.3s;
  }
  .navbar a:hover {
    /*background-color: #f0f0f0;*/
    color: #b8b8b8;
  }
</style>
