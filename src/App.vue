<template>
  <div>
    <section id="header">
      <a href="#">
        <img
          class="logo"
          src="https://marcas-logos.net/wp-content/uploads/2019/11/Nike-Logo.png"
          alt=""
        />
      </a>
      <nav>
        <div>
          <ul id="navbar">
            <li>
              <a href=""><router-link to="/">Home</router-link></a>
            </li>
            <li>
              <a href=""><router-link to="/">Shop</router-link></a>
            </li>
            <li>
              <a href=""><router-link to="/">Blog</router-link></a>
            </li>
            <li>
              <a href=""><router-link to="/">About</router-link></a>
            </li>
            <li>
              <a href=""><router-link to="/">Contact</router-link></a>
            </li>
            <li>
              <a href=""><router-link to="/">Cart</router-link></a>
            </li>
            <li>
              <router-link to="/signin"
                ><a href=""
                  ><img
                    class="profile"
                    src="https://www.nicepng.com/png/full/933-9332131_profile-picture-default-png.png" /></a
              ></router-link>
            </li>
          </ul>
        </div>
      </nav>
    </section>
    <router-view />
    <Product></Product>
    <Footer></Footer>
  </div>
</template>
<script>
import Product from "./components/MyProduct.vue";
import Footer from "./components/MyFooter.vue";
export default {
  name: "App",
  components: {
    Product,
    Footer,
  },
};
</script>

<style scoped>
/* nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
} */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

/* .section-p1 {
  padding: 40px 80px;
} */

/* .section-m1 {
  margin: 40px 0;
}

body {
  width: 100%;
} */

#header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 80px;
  background: #e3e6f3;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.06);
  z-index: 999;
  position: sticky;
  top: 0;
  left: 0;
}

img,
.logo {
  width: 70px;
  height: 40px;
}

#navbar {
  display: flex;
  align-items: center;
  justify-content: center;
}

#navbar li {
  list-style: none;
  padding: 0 20px;
  position: relative;
}

#navbar li a {
  text-decoration: none;
  font-size: 16px;
  font-weight: 600;
  color: #1a1a1a;
  transition: 0.3s ease;
}

#navbar li a:hover,
#navbar li a.active {
  color: #088178;
}

#navbar li a.active::after,
#navbar li a:hover::after {
  content: "";
  width: 30%;
  height: 2px;
  background: #088178;
  position: absolute;
  bottom: -4px;
  left: 20px;
}

.profile {
  width: 40px;
  height: 40px;
}
</style>
