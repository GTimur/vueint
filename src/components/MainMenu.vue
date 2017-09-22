<template>
    <div class="mainmenu">
        <b-nav links class="bg roundborder">
            <b-nav-item>
                <router-link to="/">
                    <span v-on:click="currentpath = 'Hello'">
                        Главная</span>
                </router-link>
            </b-nav-item>
            <b-nav-item  active>
                <router-link to="/about">
                    <span v-on:click="currentpath = 'About'">
                        Вторая</span>
                </router-link>
            </b-nav-item>
            <b-nav-item>
                <router-link to="/folio">
                    <span v-on:click="currentpath = 'Folio'">
                        Третья</span>
                </router-link>
            </b-nav-item>
            <b-nav-item>
                <router-link to="/notes">
                    <span v-on:click="currentpath = 'Notes'">
                        Четвертая</span>
                </router-link>
            </b-nav-item>
            <b-nav-item>
                <router-link to="/download">
                    <span v-on:click="currentpath = 'Download'">
                        test
                    </span>
                </router-link>
            </b-nav-item>
        </b-nav>
    </div>
</template>

<script>
export default {
  name: 'mainmenu',
  data: function () {
    return {
      currentpath: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
    font-weight: normal;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

a {
    color: #FFFFFF;
    /*#42b983;*/
}

.lpad {
    padding-left: 10em;
    padding-right: 10em;
}

.bg {
    background-color: #A9A9A9;
    font-size: 16px;
}

.bg2 {
    background-color: #FFFFF0;
}

.roundborder {
    -moz-border-radius: 4px;
    -khtml-border-radius: 4px;
    -webkit-border-radius: 4px;
    border-radius: 4px;
    /*border:1px solid white;*/
}



/* xs - устройства (до 576px) */


/* CSS для ширины, которая меньше 575px (включительно) */


/* sm-устройства (больше или равно 576px) */

@media (min-width: 576px) {
    /* CSS для: 576px <= ширины <= 767px */
    .lpad {
        padding-left: 0em;
        padding-right: 0em;
    }
}



/* md-устройства (больше или равно 768px) */

@media (min-width: 768px) {
    /* CSS для: 768px <= ширины <= 991px */
    .lpad {
        padding-left: 2em;
        padding-right: 2em;
    }
}



/* lg-устройства (больше или равно 992px) */

@media (min-width: 992px) {
    /* CSS для: 992px <= ширины <= 1119px */
    .lpad {
        padding-left: 5em;
        padding-right: 5em;
    }
}



/* xl-устройства (больше или равно 1200px) */

@media (min-width: 1200px) {
    /* CSS для: ширины >= 1200px */
    .lpad {
        padding-left: 10em;
        padding-right: 10em;
    }
}
</style>
