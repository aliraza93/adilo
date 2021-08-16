<template>
  <div id="app">
    <navbar></navbar>
    <div class="container">
      <div class="row">
        <new-orders></new-orders>
        <in-progress></in-progress>
        <waiting-buyer></waiting-buyer>
        <completed></completed>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import NewOrders from './components/NewOrders.vue'
import InProgress from './components/InProgress.vue'
import WaitingBuyer from './components/WaitingBuyer.vue'
import Completed from './components/Completed.vue'
export default {
  components: { Navbar, NewOrders, InProgress, WaitingBuyer, Completed },
  name: 'App',
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.container {
  margin-top: -0.8%;
  background-color: #fafcfe;
  height:90vh;
}

.row::after {
  content: "";
  clear: both;
  display: table;
}

.row {
  margin: 0px 5% 5% 5%;
}

[class*="col-"] {
  float: left;
  padding: 15px;
  border-radius: 5%;
  background-color: #f4f6f8;
  height: 75vh;
}

.col-3 {
  margin-top: 5%;
  margin-right: 2%;
  width: 20%;
}
.column-6 {
  width: 50%;
  margin: 10% 10% 13% 10%;
}

.column-6 img {
  width: 100%;
  height: 100%;
  border-radius: 10%;
}

.column-6 .badge {
  font-size: 12px;
  background-color: #d6bc9f;
  border-radius: 15%;
  padding: 5px;
  border: none;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin-bottom: 4px;
}

.column-6 .delivery {
  font-size: 12px;
  color: gray;
}

.column-6 .time {
  font-size: 12px;
  color: gray;
  margin: 4px 3px 4px 0;
}

.column-6 .budget {
  font-size: 12px;
  color: black;
  margin-left: 3px;
  margin: 4px 0 4px 3px;
  font-weight: 600;
}

.card {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  max-width: 300px;
  height: 33vh;
  max-height: 100%;
  background-color: white;
  font-family: arial;
  position: relative;
  display: inline-block;
}


.main-content {
  display: flex;
  position: relative;
}


.menu span {
  margin-top: 3px;
  margin-left: 3px;
  cursor: pointer;
}

/* The container <div> - needed to position the dropup content */
.dropup {
  position: relative;
  display: inline-block;
}

/* Dropup content (Hidden by Default) */
.menu-content {
  display: none;
  position: absolute;
  bottom: 3px;
  background-color: #f1f1f1;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

/* Links inside the dropup */
.menu-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

/* Change color of dropup links on hover */
.menu-content a:hover {background-color: #ddd}

/* Show the dropup menu on hover */
.dropup:hover .menu-content {
  display: block;
}


</style>
