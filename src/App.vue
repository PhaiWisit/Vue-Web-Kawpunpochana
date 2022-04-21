<template>
  <div id="nav" class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
      <a class="navbar-brand" href="/">ข้าวปุ้นโภชนา</a>
      <router-link to="/">หน้าแรก</router-link>
      <router-link to="/food">อาหารตามสั่ง</router-link>
      <router-link to="/yum">เมนูยำ</router-link>
      <router-link to="/noodle">เมนูเส้น</router-link>
      <router-link to="/drink">เมนูเครื่องดื่ม</router-link>
      <form class="d-flex">
        <input
          class="form-control me-2"
          type="search"
          placeholder="Search"
          aria-label="Search"
        />
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
      

      <!-- <li class="nav-item dropdown">
        <a
          class="nav-link dropdown-toggle"
          id="navbarDropdownMenuLink"
          role="button"
          data-bs-toggle="dropdown"
          aria-expanded="false"
        >
          Dropdown link
        </a>
        <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
          <li><a class="dropdown-item" href="#">Action</a></li>
          <li><a class="dropdown-item" href="#">Another action</a></li>
          <li><a class="dropdown-item" href="#">Something else here</a></li>
        </ul>
      </li> -->


    </div>
  </div>
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  font-size: 25px;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
  font-size: 30px;
}
</style>
