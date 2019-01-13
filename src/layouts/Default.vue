<template>
  
  <div class="layout">
    <div class="header-color">
      <header class="header">
      <nav class="nav">
        <ul>
         <li> <g-link class="nav__link" :to="{ name: 'home' }">Home</g-link> </li>
          <li> <g-link class="nav__link" :to="{ name: 'about' }">About</g-link> </li>
        </ul>
        </nav>
      </header>
    </div>
    <div class="slot-div">
      <slot/>
    </div>
  </div>
  
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
  background-color: rgb(246, 247, 248);
  font-size:1.2em;
  text-decoration: none;
}


.layout {
  
  margin: 0 auto;
  padding-left: 0px;
  padding-right: 0px;
}

.header-color{
  background-color: #E0C3FC; 
}
.header {
  max-width: 760px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;

}

.slot-div{
  max-width: 760px;
   margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
  text-decoration: none;
}
.nav ul {
   display: flex;
  justify-content: space-between;
  padding: 0;
}

.nav ul li {
  list-style: none;
  
}

.nav__link {
  margin-right: 20px;
  text-decoration: none;
  transition: 0.3s;
}
.nav__link:hover{
  font-size: 150%;
}
</style>
