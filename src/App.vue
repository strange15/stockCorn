<template>
  <div id="app">
    <div class="row">
      <div class="col-sm-3">
        <!-- <ul class="nav flex-column">
          <li class="nav-item">
            <a class="nav-link active" href="#">Active</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled" href="#">Disabled</a>
          </li>
        </ul> -->
        <ul class="cbp-vimenu">
          <li>
            <a href="#" class="icon-logo">Logo</a>
          </li>
          <li>
            <a href="#" class="icon-archive">Archive</a>
          </li>
          <li>
            <a href="#" class="icon-search">Search</a>
          </li>
          <li class="cbp-vicurrent">
            <a href="#" class="icon-pencil">Pencil</a>
          </li>
          <li>
            <a href="#" class="icon-location">Location</a>
          </li>
          <li>
            <a href="#" class="icon-images">Images</a>
          </li>
          <li>
            <a href="#" class="icon-download">Download</a>
          </li>
        </ul>
      </div>
      <div class="col-sm-6">
        One of three columns
      </div>
      <div class="col-sm-3">
        One of three columns
      </div>
    </div>

    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}

$(document).ready(function() {
  // console.log('ready!')
})
</script>

<style>

.cbp-vimenu {
  /* position: fixed; */
  overflow: hidden;
  top: 0;
  left: 0;
  height: 100%;
  list-style-type: none;
  margin: 0;
  padding: 0;
  background: #f7f7f7;
}

.cbp-vimenu li a {
  display: block;
  text-indent: -500em;
  height: 5em;
  width: 5em;
  line-height: 5em;
  text-align: center;
  color: #999;
  position: relative;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
  -webkit-transition: background 0.1s ease-in-out;
  -moz-transition: background 0.1s ease-in-out;
  transition: background 0.1s ease-in-out;
}

.cbp-vimenu li a:hover,
.cbp-vimenu li:first-child a {
  background: #47a3da;
  color: #fff;
}

/* class for current item */
.cbp-vimenu li.cbp-vicurrent a {
  background: #fff;
  color: #47a3da;
}

.cbp-vimenu li a:before {
  font-family: 'ecoico';
  speak: none;
  font-style: normal;
  font-weight: normal;
  text-indent: 0em;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  font-size: 1.4em;
  -webkit-font-smoothing: antialiased;
}

.cbp-vimenu li a.icon-logo:before {
  content: 'C';
  font-weight: 700;
  font-size: 300%;
  font-family: 'Lato', Calibri, Arial, sans-serif;
}


.icon-archive:before {
  content: 'Hello';
}

.icon-download:before {
  content: '\e006';
}

.icon-location:before {
  content: '\e007';
}

.icon-images:before {
  content: '\e009';
}

.icon-pencil:before {
  content: '\e008';
}

/* Example for media query (depends on total height of menu) */
@media screen and (max-height: 34.9375em) {
  .cbp-vimenu {
    font-size: 70%;
  }
}
</style>
